---
title: PidTagCorrelateMtsid 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777522"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="14fca-103">PidTagCorrelateMtsid 规范属性</span><span class="sxs-lookup"><span data-stu-id="14fca-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="14fca-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="14fca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14fca-105">包含用于将报告与已发送邮件关联的邮件传输系统 (MTS) 标识符。</span><span class="sxs-lookup"><span data-stu-id="14fca-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14fca-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="14fca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14fca-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="14fca-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="14fca-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="14fca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14fca-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="14fca-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="14fca-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="14fca-110">Data type:</span></span>  <br/> |<span data-ttu-id="14fca-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="14fca-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="14fca-112">区域：</span><span class="sxs-lookup"><span data-stu-id="14fca-112">Area:</span></span>  <br/> |<span data-ttu-id="14fca-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="14fca-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14fca-114">备注</span><span class="sxs-lookup"><span data-stu-id="14fca-114">Remarks</span></span>

<span data-ttu-id="14fca-115">当传输提供程序遇到该属性设置为 TRUE 已提交的邮件时，它将此属性设置为该消息的 MTS 标识符。</span><span class="sxs-lookup"><span data-stu-id="14fca-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="14fca-116">以下传输，此属性与人际邮件 (IPM) 发送邮件文件夹中的消息存储。</span><span class="sxs-lookup"><span data-stu-id="14fca-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="14fca-117">通过 MTS 标识符，如 X.400，支持相关的邮件系统保留的传输信封的原始邮件以及任何响应其生成报告的一部分的标识符。</span><span class="sxs-lookup"><span data-stu-id="14fca-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="14fca-118">从系统消息传递报表，传输提供程序将该属性与原始 MTS 标识符设置从报表的传输信封。</span><span class="sxs-lookup"><span data-stu-id="14fca-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="14fca-119">此属性与报表然后存储。</span><span class="sxs-lookup"><span data-stu-id="14fca-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="14fca-120">客户端应用程序可以维护搜索结果文件夹具有此属性的所有消息。</span><span class="sxs-lookup"><span data-stu-id="14fca-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="14fca-121">当报表时，此类邮件时，客户端可以限制应用于的搜索结果文件夹、 查找邮件的原始版本和关联的新信息的原始消息信息。</span><span class="sxs-lookup"><span data-stu-id="14fca-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14fca-122">相关资源</span><span class="sxs-lookup"><span data-stu-id="14fca-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="14fca-123">头文件</span><span class="sxs-lookup"><span data-stu-id="14fca-123">Header files</span></span>

<span data-ttu-id="14fca-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14fca-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="14fca-125">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="14fca-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="14fca-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14fca-126">Mapitags.h</span></span>
  
> <span data-ttu-id="14fca-127">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="14fca-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14fca-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14fca-128">See also</span></span>



[<span data-ttu-id="14fca-129">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="14fca-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14fca-130">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="14fca-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14fca-131">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="14fca-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14fca-132">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="14fca-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
