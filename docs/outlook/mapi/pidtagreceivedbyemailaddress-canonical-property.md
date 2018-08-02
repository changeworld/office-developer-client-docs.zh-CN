---
title: PidTagReceivedByEmailAddress 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEmailAddress
api_type:
- COM
ms.assetid: 5f9ebe20-b037-422b-9991-69f85122a706
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 6f6718bf63c48dec6d2d19b5931c6e7e81513a2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778119"
---
# <a name="pidtagreceivedbyemailaddress-canonical-property"></a><span data-ttu-id="b7b22-103">PidTagReceivedByEmailAddress 规范属性</span><span class="sxs-lookup"><span data-stu-id="b7b22-103">PidTagReceivedByEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="b7b22-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b7b22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7b22-105">包含消息中接收的消息的用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="b7b22-105">Contains the email address for the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7b22-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="b7b22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7b22-107">PR_RECEIVED_BY_EMAIL_ADDRESS，PR_RECEIVED_BY_EMAIL_ADDRESS_A，PR_RECEIVED_BY_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="b7b22-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="b7b22-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="b7b22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7b22-109">0x0076</span><span class="sxs-lookup"><span data-stu-id="b7b22-109">0x0076</span></span>  <br/> |
|<span data-ttu-id="b7b22-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="b7b22-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7b22-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b7b22-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b7b22-112">区域：</span><span class="sxs-lookup"><span data-stu-id="b7b22-112">Area:</span></span>  <br/> |<span data-ttu-id="b7b22-113">Address</span><span class="sxs-lookup"><span data-stu-id="b7b22-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7b22-114">说明</span><span class="sxs-lookup"><span data-stu-id="b7b22-114">Remarks</span></span>

<span data-ttu-id="b7b22-115">这些属性是收到邮件的邮件用户的地址属性的示例。</span><span class="sxs-lookup"><span data-stu-id="b7b22-115">These properties are examples of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="b7b22-116">它们必须由传入传输提供程序设置。</span><span class="sxs-lookup"><span data-stu-id="b7b22-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7b22-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="b7b22-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7b22-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="b7b22-118">Protocol specifications</span></span>

<span data-ttu-id="b7b22-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="b7b22-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7b22-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-122">指定的属性和操作所允许的电子邮件消息对象。</span><span class="sxs-lookup"><span data-stu-id="b7b22-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b7b22-123">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-124">处理顺序和客户端和服务器之间的数据传输的流。</span><span class="sxs-lookup"><span data-stu-id="b7b22-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b7b22-125">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-126">IETF RFC2445、 RFC2446，和 RFC2447，和约会和会议对象之间进行转换。</span><span class="sxs-lookup"><span data-stu-id="b7b22-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b7b22-127">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-128">指定用于连接到和它们代表另一个用户操作时，作为代理人，以及与邮件和日历的对象交互配置邮箱的方法。</span><span class="sxs-lookup"><span data-stu-id="b7b22-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b7b22-129">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-130">指定的属性和操作所允许的电子邮件消息对象。</span><span class="sxs-lookup"><span data-stu-id="b7b22-130">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b7b22-131">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b22-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b22-132">进行编码和解码为有效的流表示形式的消息和附件对象。</span><span class="sxs-lookup"><span data-stu-id="b7b22-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7b22-133">头文件</span><span class="sxs-lookup"><span data-stu-id="b7b22-133">Header files</span></span>

<span data-ttu-id="b7b22-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7b22-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7b22-135">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="b7b22-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7b22-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7b22-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b7b22-137">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="b7b22-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7b22-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7b22-138">See also</span></span>



[<span data-ttu-id="b7b22-139">PidTagEmailAddress 规范属性</span><span class="sxs-lookup"><span data-stu-id="b7b22-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="b7b22-140">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="b7b22-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7b22-141">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="b7b22-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7b22-142">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="b7b22-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7b22-143">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b7b22-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
