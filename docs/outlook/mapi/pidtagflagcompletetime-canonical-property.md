---
title: PidTagFlagCompleteTime 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: efaa8cf84204234697431a190a5cb6745b55ecae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777606"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="e7f80-103">PidTagFlagCompleteTime 规范属性</span><span class="sxs-lookup"><span data-stu-id="e7f80-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="e7f80-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="e7f80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7f80-105">指定以协调世界时 (UTC) 的消息对象已标记为已完成的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e7f80-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7f80-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="e7f80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7f80-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="e7f80-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="e7f80-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="e7f80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7f80-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="e7f80-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="e7f80-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="e7f80-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7f80-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e7f80-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e7f80-112">区域：</span><span class="sxs-lookup"><span data-stu-id="e7f80-112">Area:</span></span>  <br/> |<span data-ttu-id="e7f80-113">其他</span><span class="sxs-lookup"><span data-stu-id="e7f80-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7f80-114">说明</span><span class="sxs-lookup"><span data-stu-id="e7f80-114">Remarks</span></span>

<span data-ttu-id="e7f80-115">如果未标记完成的消息对象中删除此属性。</span><span class="sxs-lookup"><span data-stu-id="e7f80-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="e7f80-116">时间最小分辨率必须的分钟 （值必须是 600000000 的倍数）。</span><span class="sxs-lookup"><span data-stu-id="e7f80-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="e7f80-117">此属性必须存在如果对象是会议相关的对象，并且它应不存在于 task 对象。</span><span class="sxs-lookup"><span data-stu-id="e7f80-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7f80-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="e7f80-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7f80-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="e7f80-119">Protocol specifications</span></span>

<span data-ttu-id="e7f80-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f80-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f80-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="e7f80-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7f80-122">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f80-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f80-123">指定的属性和与标记的操作。</span><span class="sxs-lookup"><span data-stu-id="e7f80-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7f80-124">头文件</span><span class="sxs-lookup"><span data-stu-id="e7f80-124">Header files</span></span>

<span data-ttu-id="e7f80-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7f80-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7f80-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="e7f80-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7f80-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7f80-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e7f80-128">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="e7f80-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7f80-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7f80-129">See also</span></span>



[<span data-ttu-id="e7f80-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="e7f80-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7f80-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="e7f80-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7f80-132">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="e7f80-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7f80-133">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="e7f80-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
