---
title: 状态对象实现
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 379378f2092f7b119a40ac44cbdcfa03f254b448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778888"
---
# <a name="status-object-implementation"></a><span data-ttu-id="ac917-103">状态对象实现</span><span class="sxs-lookup"><span data-stu-id="ac917-103">Status object implementation</span></span>

<span data-ttu-id="ac917-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="ac917-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac917-105">所有服务提供程序必须实现状态对象，并提供了该属性设置为会话状态表。</span><span class="sxs-lookup"><span data-stu-id="ac917-105">All service providers must implement a status object and furnish properties from it to the session status table.</span></span> <span data-ttu-id="ac917-106">在状态表中，具体取决于您控制的资源数可以包括一个或多个行。</span><span class="sxs-lookup"><span data-stu-id="ac917-106">You can include one or more rows in the status table, depending on the number of resources that you control.</span></span> <span data-ttu-id="ac917-107">传输提供程序，例如，应创建行状态表中管理每个消息队列。</span><span class="sxs-lookup"><span data-stu-id="ac917-107">A transport provider, for example, should create a row in the status table for each message queue it manages.</span></span> <span data-ttu-id="ac917-108">更改时，必须更新相应的状态表格行。</span><span class="sxs-lookup"><span data-stu-id="ac917-108">When changes occur, the appropriate status table row must be updated.</span></span> <span data-ttu-id="ac917-109">状态对象被实现提供访问状态表中包含的信息，不包含表中的其他信息。</span><span class="sxs-lookup"><span data-stu-id="ac917-109">Status objects are implemented to provide access both to the information included in the status table and to additional information not included in the table.</span></span>
  
### <a name="to-implement-a-status-object"></a><span data-ttu-id="ac917-110">若要实现状态对象</span><span class="sxs-lookup"><span data-stu-id="ac917-110">To implement a status object</span></span>

1. <span data-ttu-id="ac917-111">实现登录对象的**OpenStatusEntry**方法。</span><span class="sxs-lookup"><span data-stu-id="ac917-111">Implement the **OpenStatusEntry** method of your logon object.</span></span> <span data-ttu-id="ac917-112">当客户端想要打开状态对象时，它们会调用[IMAPISession::OpenEntry](imapisession-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="ac917-112">When clients want to open your status object, they call [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="ac917-113">MAPI 履行打开请求通过调用您的提供商**OpenStatusEntry**方法，导致您的提供商，以打开其状态对象并返回到客户端指向其**IMAPIStatus**实现的指针。</span><span class="sxs-lookup"><span data-stu-id="ac917-113">MAPI fulfills the open request by calling your provider's **OpenStatusEntry** method, causing your provider to open its status object and return to the client a pointer to its **IMAPIStatus** implementation.</span></span> <span data-ttu-id="ac917-114">在**OpenStatusEntry**实现中，完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="ac917-114">In your **OpenStatusEntry** implementation, complete the following steps:</span></span> 
    
   1. <span data-ttu-id="ac917-115">如果您的登录对象尚未创建状态对象，请执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="ac917-115">Perform the following tasks if your logon object has not yet created a status object:</span></span>
    
      1. <span data-ttu-id="ac917-116">调用支持对象的[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)方法，以访问提供程序的配置文件一节。</span><span class="sxs-lookup"><span data-stu-id="ac917-116">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your provider's profile section.</span></span> 
          
      2. <span data-ttu-id="ac917-117">创建新的状态对象。</span><span class="sxs-lookup"><span data-stu-id="ac917-117">Create a new status object.</span></span>
          
      3. <span data-ttu-id="ac917-118">存储提供程序的状态对象中的配置文件部分的引用，并调用配置文件部分的[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)方法，以增加引用计数。</span><span class="sxs-lookup"><span data-stu-id="ac917-118">Store a reference to the profile section in your provider's status object and call the profile section's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count.</span></span> 
          
      4. <span data-ttu-id="ac917-119">存储提供程序的状态对象中的登录对象的引用，并调用登录对象的**IUnknown::AddRef**方法，以增加引用计数。</span><span class="sxs-lookup"><span data-stu-id="ac917-119">Store a reference to the logon object in your provider's status object and call the logon object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
          
      5. <span data-ttu-id="ac917-120">存储提供程序的登录对象中的状态对象的引用。</span><span class="sxs-lookup"><span data-stu-id="ac917-120">Store a reference to the status object in your provider's logon object.</span></span>
    
   2. <span data-ttu-id="ac917-121">调用状态对象的**IUnknown::AddRef**方法，以增加引用计数登录对象中。</span><span class="sxs-lookup"><span data-stu-id="ac917-121">Call the status object's **IUnknown::AddRef** method to increment its reference count in the logon object.</span></span> 
    
   3. <span data-ttu-id="ac917-122">将状态对象的**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 属性设置为 MAPI_STATUS。</span><span class="sxs-lookup"><span data-stu-id="ac917-122">Set the status object's **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property to MAPI_STATUS.</span></span>
    
   4. <span data-ttu-id="ac917-123">设置以指向状态的对象，并返回_lppMAPIStatus_输出参数。</span><span class="sxs-lookup"><span data-stu-id="ac917-123">Set the  _lppMAPIStatus_ output parameter to point to the status object, and return.</span></span> 
    
   5. <span data-ttu-id="ac917-124">检查_ulFlags_输入的参数。</span><span class="sxs-lookup"><span data-stu-id="ac917-124">Check the  _ulFlags_ input parameter.</span></span> <span data-ttu-id="ac917-125">如果您的提供商支持对其状态对象的读/写访问其设置为 MAPI_MODIFY，返回一个可写对象。</span><span class="sxs-lookup"><span data-stu-id="ac917-125">If it is set to MAPI_MODIFY and your provider supports read/write access to its status object, return a writeable object.</span></span> <span data-ttu-id="ac917-126">但是，如果您的提供程序不支持对其状态对象的读/写访问，不会失败。</span><span class="sxs-lookup"><span data-stu-id="ac917-126">However, if your provider does not support read/write access to its status object, do not fail.</span></span> <span data-ttu-id="ac917-127">返回一个状态对象，是只读的。</span><span class="sxs-lookup"><span data-stu-id="ac917-127">Return a status object that is read-only.</span></span> <span data-ttu-id="ac917-128">希望接收读/写状态对象的客户端应验证尝试进行任何更改之前已被授予了读/写权限。</span><span class="sxs-lookup"><span data-stu-id="ac917-128">Clients that expect to receive read/write status objects should verify that read/write permission has been granted before attempting to make any changes.</span></span> 
    
2. <span data-ttu-id="ac917-129">设置所需的状态的所有对象和状态表属性。</span><span class="sxs-lookup"><span data-stu-id="ac917-129">Set all of the required status object and status table properties.</span></span> <span data-ttu-id="ac917-130">您在您的状态表格行中包含的属性应为可通过状态对象，通过 MAPI 计算属性除外。</span><span class="sxs-lookup"><span data-stu-id="ac917-130">The properties that you include in your status table row should be available through your status object, except for the properties calculated by MAPI.</span></span> <span data-ttu-id="ac917-131">必需的属性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ac917-131">The required properties are as follows:</span></span>
    
   - <span data-ttu-id="ac917-132">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-133">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-133">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-134">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-135">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-135">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-136">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-136">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-137">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-137">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>
    
   - <span data-ttu-id="ac917-138">**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac917-138">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>
    
3. <span data-ttu-id="ac917-139">实现[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)适合您的提供商的方法。</span><span class="sxs-lookup"><span data-stu-id="ac917-139">Implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) methods that are appropriate for your provider.</span></span> <span data-ttu-id="ac917-140">根据您的提供商，不需要在**IMAPIStatus**中实现的所有四个方法。</span><span class="sxs-lookup"><span data-stu-id="ac917-140">Depending on your provider, you do not need to implement all of the four methods in **IMAPIStatus**.</span></span> <span data-ttu-id="ac917-141">每个提供程序应实现的方法的只读版本[IMAPIProp: IUnknown](imapipropiunknown.md)接口和[IMAPIStatus::ValidateState](imapistatus-validatestate.md)方法。</span><span class="sxs-lookup"><span data-stu-id="ac917-141">Every provider should implement a read-only version of the methods of the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 

   <span data-ttu-id="ac917-142">传输提供程序还应实现[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)，和所有提供程序应支持[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)。</span><span class="sxs-lookup"><span data-stu-id="ac917-142">Transport providers should also implement [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md), and all providers should support [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md).</span></span> <span data-ttu-id="ac917-143">但是，支持[IMAPIStatus::ChangePassword](imapistatus-changepassword.md)是可选的。</span><span class="sxs-lookup"><span data-stu-id="ac917-143">However, support for [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) is optional.</span></span> <span data-ttu-id="ac917-144">仅服务提供程序要求密码，并且想要允许用户以编程方式更改它们需要实现此方法。</span><span class="sxs-lookup"><span data-stu-id="ac917-144">Only service providers that require passwords and want to allow users to change them programmatically need to implement this method.</span></span> <span data-ttu-id="ac917-145">对于每个支持的方法， **PR_RESOURCE_METHODS**属性中设置相应的位。</span><span class="sxs-lookup"><span data-stu-id="ac917-145">For every method that you support, set the corresponding bit in the **PR_RESOURCE_METHODS** property.</span></span> <span data-ttu-id="ac917-146">例如，如果仅支持**ValidateState**和**留待**，设置为**PR_RESOURCE_METHODS** :</span><span class="sxs-lookup"><span data-stu-id="ac917-146">For example, if you support **ValidateState** and **SettingsDialog** only, set **PR_RESOURCE_METHODS** to the following:</span></span> 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   <span data-ttu-id="ac917-147">客户端应尝试呼叫您状态的对象之前检查**PR_RESOURCE_METHODS**的值。</span><span class="sxs-lookup"><span data-stu-id="ac917-147">Clients should check the value of **PR_RESOURCE_METHODS** before attempting to call your status object.</span></span> <span data-ttu-id="ac917-148">返回 MAPI_E_NO_SUPPORT 通过以下方式处理对任何您不受支持的方法调用。</span><span class="sxs-lookup"><span data-stu-id="ac917-148">Handle calls to any of your unsupported methods by returning MAPI_E_NO_SUPPORT.</span></span> 
    
4. <span data-ttu-id="ac917-149">若要将您一行或多行添加到状态表的登录过程中调用[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) 。</span><span class="sxs-lookup"><span data-stu-id="ac917-149">Call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) during logon to add your row or rows to the status table.</span></span> <span data-ttu-id="ac917-150">传递包含行的列信息和 0 _ulFlags_参数的属性值数组。</span><span class="sxs-lookup"><span data-stu-id="ac917-150">Pass a property value array that contains the column information for the row and 0 for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="ac917-151">如果会话更高版本中的某个时刻提供商的状态更改和其变得更新列信息所需的**ModifyStatusRow**再次调用设置了 STATUSROW_UPDATE 标志。</span><span class="sxs-lookup"><span data-stu-id="ac917-151">If at some point later in the session your provider's status changes and it becomes necessary to update the column information, call **ModifyStatusRow** again with the STATUSROW_UPDATE flag set.</span></span> 
    
<span data-ttu-id="ac917-152">有关状态的对象的详细信息，请参阅[MAPI 状态对象](mapi-status-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ac917-152">For more information about status objects, see [MAPI Status Objects](mapi-status-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac917-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac917-153">See also</span></span>

- [<span data-ttu-id="ac917-154">MAPI 服务提供商</span><span class="sxs-lookup"><span data-stu-id="ac917-154">MAPI Service Providers</span></span>](mapi-service-providers.md)
