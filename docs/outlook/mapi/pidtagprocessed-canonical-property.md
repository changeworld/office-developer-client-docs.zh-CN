---
title: PidTagProcessed 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 0918f079769a70aa11e4f26551ec232308e5eef0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778056"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="b8306-103">PidTagProcessed 规范属性</span><span class="sxs-lookup"><span data-stu-id="b8306-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="b8306-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b8306-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b8306-105">已处理的会议请求时，设置为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="b8306-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8306-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="b8306-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8306-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="b8306-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="b8306-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="b8306-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8306-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="b8306-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="b8306-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="b8306-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8306-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b8306-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b8306-112">区域：</span><span class="sxs-lookup"><span data-stu-id="b8306-112">Area:</span></span>  <br/> |<span data-ttu-id="b8306-113">日历</span><span class="sxs-lookup"><span data-stu-id="b8306-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8306-114">说明</span><span class="sxs-lookup"><span data-stu-id="b8306-114">Remarks</span></span>

<span data-ttu-id="b8306-115">此属性可确保会议请求获取处理一次。</span><span class="sxs-lookup"><span data-stu-id="b8306-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="b8306-116">请求的创建者应将此属性设置为 FALSE，接收方应将其设置为 TRUE 后请求在日历中。</span><span class="sxs-lookup"><span data-stu-id="b8306-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b8306-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="b8306-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8306-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="b8306-118">Protocol specifications</span></span>

<span data-ttu-id="b8306-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8306-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8306-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="b8306-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8306-121">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8306-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8306-122">指定的属性和约会、 会议请求和响应消息的操作。</span><span class="sxs-lookup"><span data-stu-id="b8306-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="b8306-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8306-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8306-124">指定的属性和允许的联系人和个人通讯组列表对象的操作。</span><span class="sxs-lookup"><span data-stu-id="b8306-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8306-125">头文件</span><span class="sxs-lookup"><span data-stu-id="b8306-125">Header files</span></span>

<span data-ttu-id="b8306-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8306-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8306-127">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="b8306-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8306-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8306-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b8306-129">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="b8306-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8306-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8306-130">See also</span></span>



[<span data-ttu-id="b8306-131">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="b8306-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8306-132">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="b8306-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8306-133">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="b8306-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8306-134">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b8306-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
