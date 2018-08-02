---
title: PidTagOriginatorDeliveryReportRequested 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777995"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="67021-103">PidTagOriginatorDeliveryReportRequested 规范属性</span><span class="sxs-lookup"><span data-stu-id="67021-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="67021-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="67021-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67021-105">如果邮件发件人请求特定收件人从邮件系统的送达报告之前消息置于消息存储库中，包含 TRUE。</span><span class="sxs-lookup"><span data-stu-id="67021-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67021-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="67021-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67021-107">邮件已被阅读</span><span class="sxs-lookup"><span data-stu-id="67021-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="67021-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="67021-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67021-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="67021-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="67021-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="67021-110">Data type:</span></span>  <br/> |<span data-ttu-id="67021-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="67021-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="67021-112">区域：</span><span class="sxs-lookup"><span data-stu-id="67021-112">Area:</span></span>  <br/> |<span data-ttu-id="67021-113">MIME</span><span class="sxs-lookup"><span data-stu-id="67021-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67021-114">说明</span><span class="sxs-lookup"><span data-stu-id="67021-114">Remarks</span></span>

<span data-ttu-id="67021-115">此属性用于直接在邮件系统中处理已发送的邮件。</span><span class="sxs-lookup"><span data-stu-id="67021-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="67021-116">在这种情况下，邮件还必须提供**PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) 属性设置为 FALSE。</span><span class="sxs-lookup"><span data-stu-id="67021-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="67021-117">上一条消息设置的**邮件已被阅读**属性是一种方法传递状态报告请求的所有收件人。</span><span class="sxs-lookup"><span data-stu-id="67021-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="67021-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="67021-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67021-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="67021-119">Protocol specifications</span></span>

<span data-ttu-id="67021-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67021-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67021-121">指定的属性和操作所允许的电子邮件消息对象。</span><span class="sxs-lookup"><span data-stu-id="67021-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67021-122">头文件</span><span class="sxs-lookup"><span data-stu-id="67021-122">Header files</span></span>

<span data-ttu-id="67021-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67021-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="67021-124">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="67021-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="67021-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67021-125">Mapitags.h</span></span>
  
> <span data-ttu-id="67021-126">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="67021-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67021-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67021-127">See also</span></span>



[<span data-ttu-id="67021-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="67021-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67021-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="67021-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67021-130">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="67021-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67021-131">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="67021-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
