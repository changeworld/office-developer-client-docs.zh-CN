---
title: PidTagResourceMethods 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778211"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="f757b-103">PidTagResourceMethods 规范属性</span><span class="sxs-lookup"><span data-stu-id="f757b-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="f757b-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="f757b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f757b-105">包含这些标志指示**IMAPIStatus**接口中支持的状态对象的方法的位掩码。</span><span class="sxs-lookup"><span data-stu-id="f757b-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f757b-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="f757b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f757b-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="f757b-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="f757b-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="f757b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f757b-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="f757b-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="f757b-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="f757b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f757b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f757b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f757b-112">区域：</span><span class="sxs-lookup"><span data-stu-id="f757b-112">Area:</span></span>  <br/> |<span data-ttu-id="f757b-113">MAPI 状态</span><span class="sxs-lookup"><span data-stu-id="f757b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f757b-114">备注</span><span class="sxs-lookup"><span data-stu-id="f757b-114">Remarks</span></span>

<span data-ttu-id="f757b-115">此属性指示支持哪种中**IMAPIStatus**状态对象实现的方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="f757b-116">允许从不受支持方法返回 MAPI_E_NO_SUPPORT 状态对象。</span><span class="sxs-lookup"><span data-stu-id="f757b-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="f757b-117">客户端使用状态对象的**PR_RESOURCE_METHODS**属性可避免对不受支持的方法的调用。</span><span class="sxs-lookup"><span data-stu-id="f757b-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="f757b-118">如果设置对应于特定方法的标志，此方法存在且可调用它。</span><span class="sxs-lookup"><span data-stu-id="f757b-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="f757b-119">如果清除该标志，则不应调用方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="f757b-120">状态对象实现 MAPI 支持以下方法：</span><span class="sxs-lookup"><span data-stu-id="f757b-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="f757b-121">**状态对象**</span><span class="sxs-lookup"><span data-stu-id="f757b-121">**Status object**</span></span>|<span data-ttu-id="f757b-122">**受支持的方法**</span><span class="sxs-lookup"><span data-stu-id="f757b-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f757b-123">MAPI 子系统</span><span class="sxs-lookup"><span data-stu-id="f757b-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="f757b-124">仅**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="f757b-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="f757b-125">MAPI 通讯簿</span><span class="sxs-lookup"><span data-stu-id="f757b-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="f757b-126">仅**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="f757b-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="f757b-127">MAPI 后台处理程序</span><span class="sxs-lookup"><span data-stu-id="f757b-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="f757b-128">**ValidateState**和**FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="f757b-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="f757b-129">一个或多个以下标志可以**PR_RESOURCE_METHODS**设置：</span><span class="sxs-lookup"><span data-stu-id="f757b-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="f757b-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="f757b-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="f757b-131">表示支持[IMAPIStatus::ChangePassword](imapistatus-changepassword.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="f757b-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="f757b-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="f757b-133">表示支持[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="f757b-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f757b-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="f757b-135">表示支持[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="f757b-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="f757b-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="f757b-137">表示支持[IMAPIStatus::ValidateState](imapistatus-validatestate.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f757b-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="f757b-138">相关资源</span><span class="sxs-lookup"><span data-stu-id="f757b-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f757b-139">头文件</span><span class="sxs-lookup"><span data-stu-id="f757b-139">Header files</span></span>

<span data-ttu-id="f757b-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f757b-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="f757b-141">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="f757b-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="f757b-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f757b-142">Mapitags.h</span></span>
  
> <span data-ttu-id="f757b-143">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="f757b-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f757b-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f757b-144">See also</span></span>



[<span data-ttu-id="f757b-145">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="f757b-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f757b-146">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="f757b-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f757b-147">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="f757b-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f757b-148">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="f757b-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
