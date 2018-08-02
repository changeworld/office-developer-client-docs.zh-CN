---
title: PidTagDeliveryPoint 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777556"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="99246-103">PidTagDeliveryPoint 规范属性</span><span class="sxs-lookup"><span data-stu-id="99246-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="99246-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="99246-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99246-105">指定一条消息已通过其或已传递给收件人功能实体的特性。</span><span class="sxs-lookup"><span data-stu-id="99246-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99246-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="99246-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99246-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="99246-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="99246-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="99246-108">Identifier:</span></span>  <br/> |<span data-ttu-id="99246-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="99246-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="99246-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="99246-110">Data type:</span></span>  <br/> |<span data-ttu-id="99246-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="99246-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="99246-112">区域：</span><span class="sxs-lookup"><span data-stu-id="99246-112">Area:</span></span>  <br/> |<span data-ttu-id="99246-113">MAPI 收件人</span><span class="sxs-lookup"><span data-stu-id="99246-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99246-114">说明</span><span class="sxs-lookup"><span data-stu-id="99246-114">Remarks</span></span>

<span data-ttu-id="99246-115">此属性可以具有完全下列值之一：</span><span class="sxs-lookup"><span data-stu-id="99246-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="99246-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="99246-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="99246-117">传递给通讯组列表，收信人地址的反过来可能分发很多个收件人的邮件。</span><span class="sxs-lookup"><span data-stu-id="99246-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="99246-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="99246-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="99246-119">传递给而不是直接向收件人的消息存储。</span><span class="sxs-lookup"><span data-stu-id="99246-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="99246-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="99246-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="99246-121">物理传递访问单位 (PDAU)，如传真系统之外送达访问单元 (AU)。</span><span class="sxs-lookup"><span data-stu-id="99246-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="99246-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="99246-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="99246-123">发送到物理传递访问单位，如 human 邮政运营商。</span><span class="sxs-lookup"><span data-stu-id="99246-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="99246-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="99246-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="99246-125">发送到物理传递系统记录，如传统的邮政邮箱。</span><span class="sxs-lookup"><span data-stu-id="99246-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="99246-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="99246-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="99246-127">例如，内部邮件系统中的客户端送达专用用户代理 (UA)。</span><span class="sxs-lookup"><span data-stu-id="99246-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="99246-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="99246-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="99246-129">传递到公共用户代理或公共服务提供商。</span><span class="sxs-lookup"><span data-stu-id="99246-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="99246-130">默认值是 MAPI_MH_DP_PRIVATE_UA，即，MAPI 客户端。</span><span class="sxs-lookup"><span data-stu-id="99246-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99246-131">相关资源</span><span class="sxs-lookup"><span data-stu-id="99246-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="99246-132">头文件</span><span class="sxs-lookup"><span data-stu-id="99246-132">Header files</span></span>

<span data-ttu-id="99246-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99246-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="99246-134">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="99246-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="99246-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="99246-135">Mapitags.h</span></span>
  
> <span data-ttu-id="99246-136">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="99246-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99246-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99246-137">See also</span></span>



[<span data-ttu-id="99246-138">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="99246-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99246-139">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="99246-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99246-140">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="99246-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99246-141">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="99246-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
