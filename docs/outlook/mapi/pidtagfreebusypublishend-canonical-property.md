---
title: PidTagFreeBusyPublishEnd 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 1f7f439b211b60f7acad3a9dd19c50a21923c1cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777655"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="71004-103">PidTagFreeBusyPublishEnd 规范属性</span><span class="sxs-lookup"><span data-stu-id="71004-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="71004-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="71004-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71004-105">包含发布范围的结束时间。</span><span class="sxs-lookup"><span data-stu-id="71004-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71004-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="71004-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71004-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="71004-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="71004-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="71004-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71004-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="71004-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="71004-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="71004-110">Data type:</span></span>  <br/> |<span data-ttu-id="71004-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="71004-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="71004-112">区域：</span><span class="sxs-lookup"><span data-stu-id="71004-112">Area:</span></span>  <br/> |<span data-ttu-id="71004-113">忙/闲</span><span class="sxs-lookup"><span data-stu-id="71004-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71004-114">备注</span><span class="sxs-lookup"><span data-stu-id="71004-114">Remarks</span></span>

<span data-ttu-id="71004-115">此属性的值为发布的范围的开始日期计算通过添加**PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) 的值。</span><span class="sxs-lookup"><span data-stu-id="71004-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="71004-116">此值表示为午夜，采用协调世界时 (UTC) 1601 年 1 月 1 日的分钟数。</span><span class="sxs-lookup"><span data-stu-id="71004-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71004-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="71004-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71004-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="71004-118">Protocol specifications</span></span>

<span data-ttu-id="71004-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71004-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71004-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="71004-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71004-121">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71004-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71004-122">发布的用户或资源的可用性。</span><span class="sxs-lookup"><span data-stu-id="71004-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71004-123">头文件</span><span class="sxs-lookup"><span data-stu-id="71004-123">Header files</span></span>

<span data-ttu-id="71004-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71004-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="71004-125">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="71004-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="71004-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71004-126">Mapitags.h</span></span>
  
> <span data-ttu-id="71004-127">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="71004-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71004-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71004-128">See also</span></span>



[<span data-ttu-id="71004-129">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="71004-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71004-130">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="71004-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71004-131">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="71004-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71004-132">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="71004-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
