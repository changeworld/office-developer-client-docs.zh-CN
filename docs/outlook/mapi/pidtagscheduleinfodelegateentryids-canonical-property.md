---
title: PidTagScheduleInfoDelegateEntryIds 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778322"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="6a4e8-103">PidTagScheduleInfoDelegateEntryIds 规范属性</span><span class="sxs-lookup"><span data-stu-id="6a4e8-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="6a4e8-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="6a4e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a4e8-105">包含的代理人的**Entryid** 。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a4e8-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="6a4e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a4e8-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="6a4e8-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="6a4e8-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="6a4e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a4e8-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="6a4e8-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="6a4e8-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="6a4e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a4e8-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a4e8-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="6a4e8-112">区域：</span><span class="sxs-lookup"><span data-stu-id="6a4e8-112">Area:</span></span>  <br/> |<span data-ttu-id="6a4e8-113">忙/闲</span><span class="sxs-lookup"><span data-stu-id="6a4e8-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a4e8-114">备注</span><span class="sxs-lookup"><span data-stu-id="6a4e8-114">Remarks</span></span>

<span data-ttu-id="6a4e8-115">每个条目都必须包含每个代理人的通讯簿条目的**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 属性的值。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="6a4e8-116">此属性必须设置委托信息对象中。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a4e8-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="6a4e8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a4e8-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="6a4e8-118">Protocol specifications</span></span>

<span data-ttu-id="6a4e8-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a4e8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a4e8-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a4e8-121">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a4e8-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a4e8-122">指定用于连接到和它们代表另一个用户操作时，作为代理人，以及与邮件和日历的对象交互配置邮箱的方法。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a4e8-123">头文件</span><span class="sxs-lookup"><span data-stu-id="6a4e8-123">Header files</span></span>

<span data-ttu-id="6a4e8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a4e8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a4e8-125">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a4e8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a4e8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6a4e8-127">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="6a4e8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a4e8-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a4e8-128">See also</span></span>



[<span data-ttu-id="6a4e8-129">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="6a4e8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a4e8-130">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="6a4e8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a4e8-131">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="6a4e8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a4e8-132">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="6a4e8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
