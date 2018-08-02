---
title: PidTagMessageSize 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777865"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="4e8b9-103">PidTagMessageSize 规范属性</span><span class="sxs-lookup"><span data-stu-id="4e8b9-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="4e8b9-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="4e8b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e8b9-105">包含消息对象上的所有属性的大小的总和，以字节为单位。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e8b9-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="4e8b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e8b9-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="4e8b9-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="4e8b9-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="4e8b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e8b9-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="4e8b9-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="4e8b9-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="4e8b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e8b9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4e8b9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4e8b9-112">区域：</span><span class="sxs-lookup"><span data-stu-id="4e8b9-112">Area:</span></span>  <br/> |<span data-ttu-id="4e8b9-113">常规消息</span><span class="sxs-lookup"><span data-stu-id="4e8b9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e8b9-114">说明</span><span class="sxs-lookup"><span data-stu-id="4e8b9-114">Remarks</span></span>

<span data-ttu-id="4e8b9-115">建议消息对象公开此属性。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="4e8b9-116">邮件大小表示的近似时该消息从一个消息存储库移至另一个被转移的字节数。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="4e8b9-117">正在对消息对象的所有属性的大小的总和，它通常是相当大于单独的消息文本。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="4e8b9-118">大多数消息存储提供程序计算此属性的它们处理的邮件。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="4e8b9-119">但是，某些消息存储提供程序不支持此属性。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="4e8b9-120">在任何情况下，直到[IMAPIProp::SaveChanges](imapiprop-savechanges.md)或[IMessage::SubmitMessage](imessage-submitmessage.md)方法被调用此属性不可用。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e8b9-121">相关资源</span><span class="sxs-lookup"><span data-stu-id="4e8b9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e8b9-122">协议规范</span><span class="sxs-lookup"><span data-stu-id="4e8b9-122">Protocol specifications</span></span>

<span data-ttu-id="4e8b9-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b9-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b9-124">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e8b9-125">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b9-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b9-126">处理邮件和附件的对象。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4e8b9-127">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b9-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b9-128">处理文件夹的操作。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-128">Handles folder operations.</span></span>
    
<span data-ttu-id="4e8b9-129">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b9-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b9-130">指定允许的操作的核心消息存储对象。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e8b9-131">头文件</span><span class="sxs-lookup"><span data-stu-id="4e8b9-131">Header files</span></span>

<span data-ttu-id="4e8b9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e8b9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e8b9-133">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e8b9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e8b9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="4e8b9-135">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="4e8b9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e8b9-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e8b9-136">See also</span></span>



[<span data-ttu-id="4e8b9-137">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="4e8b9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e8b9-138">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="4e8b9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e8b9-139">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="4e8b9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e8b9-140">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="4e8b9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
