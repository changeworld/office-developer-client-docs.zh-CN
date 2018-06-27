---
title: PidTagRecipientTrackStatusTime 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 0db4efcf1e05536ee7abb3459caa0159f84ef798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778162"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="c2afa-103">PidTagRecipientTrackStatusTime 规范属性</span><span class="sxs-lookup"><span data-stu-id="c2afa-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="c2afa-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="c2afa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2afa-105">包含的日期和时间时与会者响应。</span><span class="sxs-lookup"><span data-stu-id="c2afa-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2afa-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="c2afa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2afa-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="c2afa-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="c2afa-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="c2afa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2afa-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="c2afa-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="c2afa-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="c2afa-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2afa-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c2afa-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c2afa-112">区域：</span><span class="sxs-lookup"><span data-stu-id="c2afa-112">Area:</span></span>  <br/> |<span data-ttu-id="c2afa-113">传输收件人</span><span class="sxs-lookup"><span data-stu-id="c2afa-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2afa-114">备注</span><span class="sxs-lookup"><span data-stu-id="c2afa-114">Remarks</span></span>

<span data-ttu-id="c2afa-115">必须以协调世界时 (UTC) 指定的值。</span><span class="sxs-lookup"><span data-stu-id="c2afa-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2afa-116">相关资源</span><span class="sxs-lookup"><span data-stu-id="c2afa-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2afa-117">协议规范</span><span class="sxs-lookup"><span data-stu-id="c2afa-117">Protocol specifications</span></span>

<span data-ttu-id="c2afa-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2afa-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2afa-119">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="c2afa-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c2afa-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2afa-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2afa-121">指定的属性和约会、 会议请求和响应消息的操作。</span><span class="sxs-lookup"><span data-stu-id="c2afa-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2afa-122">头文件</span><span class="sxs-lookup"><span data-stu-id="c2afa-122">Header files</span></span>

<span data-ttu-id="c2afa-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2afa-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2afa-124">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="c2afa-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2afa-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2afa-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c2afa-126">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="c2afa-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2afa-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2afa-127">See also</span></span>



[<span data-ttu-id="c2afa-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="c2afa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2afa-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="c2afa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2afa-130">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="c2afa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2afa-131">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="c2afa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
