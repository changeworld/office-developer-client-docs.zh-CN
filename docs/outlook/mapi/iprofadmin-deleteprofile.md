---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776013"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="35496-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="35496-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="35496-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="35496-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35496-105">删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="35496-106">参数</span><span class="sxs-lookup"><span data-stu-id="35496-106">Parameters</span></span>

 <span data-ttu-id="35496-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="35496-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="35496-108">[in]指针，指向要删除的配置文件的名称。</span><span class="sxs-lookup"><span data-stu-id="35496-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="35496-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35496-109">_ulFlags_</span></span>
  
> <span data-ttu-id="35496-110">[in]始终为 NULL。</span><span class="sxs-lookup"><span data-stu-id="35496-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35496-111">返回值</span><span class="sxs-lookup"><span data-stu-id="35496-111">Return value</span></span>

<span data-ttu-id="35496-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="35496-112">S_OK</span></span> 
  
> <span data-ttu-id="35496-113">已成功删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="35496-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="35496-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="35496-115">指定的配置文件不存在。</span><span class="sxs-lookup"><span data-stu-id="35496-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35496-116">说明</span><span class="sxs-lookup"><span data-stu-id="35496-116">Remarks</span></span>

<span data-ttu-id="35496-117">**IProfAdmin::DeleteProfile**方法删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="35496-118">如果要删除的配置文件正在使用中，调用**DeleteProfile**时， **DeleteProfile** ，则返回 S_OK，但不会立即删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="35496-119">相反， **DeleteProfile**标记为删除的配置文件并将不再正在时使用它，所有其活动会话结束后将其删除。</span><span class="sxs-lookup"><span data-stu-id="35496-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="35496-120">使用_ulContext_参数中设置的 MSG_SERVICE_DELETE 值调用入口点函数的配置文件中的每个邮件服务。</span><span class="sxs-lookup"><span data-stu-id="35496-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="35496-121">首先，此函数删除该服务，，然后它删除该服务的配置文件一节。</span><span class="sxs-lookup"><span data-stu-id="35496-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="35496-122">删除服务后邮件服务入口点函数不再次调用。</span><span class="sxs-lookup"><span data-stu-id="35496-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="35496-123">不需要密码删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="35496-124">MFCMAPI 参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="35496-124">MFCMAPI reference</span></span>

<span data-ttu-id="35496-125">MFCMAPI 示例代码，请参阅下表。</span><span class="sxs-lookup"><span data-stu-id="35496-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="35496-126">**文件**</span><span class="sxs-lookup"><span data-stu-id="35496-126">**File**</span></span>|<span data-ttu-id="35496-127">**函数**</span><span class="sxs-lookup"><span data-stu-id="35496-127">**Function**</span></span>|<span data-ttu-id="35496-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="35496-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35496-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="35496-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="35496-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="35496-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="35496-131">MFCMAPI 使用**IProfAdmin::DeleteProfile**方法删除选定的配置文件。</span><span class="sxs-lookup"><span data-stu-id="35496-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35496-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35496-132">See also</span></span>



[<span data-ttu-id="35496-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="35496-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="35496-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="35496-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="35496-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35496-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="35496-136">MFCMAPI 代码示例</span><span class="sxs-lookup"><span data-stu-id="35496-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
