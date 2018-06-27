---
title: PidTagConversationKey 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 4aec52497e02e99423fa50f378cd35dbf366c37c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777502"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="f5329-103">PidTagConversationKey 规范属性</span><span class="sxs-lookup"><span data-stu-id="f5329-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="f5329-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="f5329-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5329-105">包含查找**IPM 时仅在 Microsoft Outlook 中使用的会话密钥。MessageManager**邮件，例如包含邮局协议 (POP3) 帐户的下载历史记录的邮件。</span><span class="sxs-lookup"><span data-stu-id="f5329-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="f5329-106">Microsoft Exchange Server 中已弃用此属性。</span><span class="sxs-lookup"><span data-stu-id="f5329-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5329-107">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="f5329-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5329-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="f5329-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="f5329-109">标识符:</span><span class="sxs-lookup"><span data-stu-id="f5329-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f5329-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="f5329-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="f5329-111">数据类型：</span><span class="sxs-lookup"><span data-stu-id="f5329-111">Data type:</span></span>  <br/> |<span data-ttu-id="f5329-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f5329-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f5329-113">区域：</span><span class="sxs-lookup"><span data-stu-id="f5329-113">Area:</span></span>  <br/> |<span data-ttu-id="f5329-114">常规消息</span><span class="sxs-lookup"><span data-stu-id="f5329-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5329-115">备注</span><span class="sxs-lookup"><span data-stu-id="f5329-115">Remarks</span></span>

<span data-ttu-id="f5329-116">为对话并将其转换为[传输中性封装格式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)邮件属性访问电子邮件时, 不使用此属性;而是使用[PidTagConversationIndex](pidtagconversationindex-canonical-property.md)和[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)规范属性。</span><span class="sxs-lookup"><span data-stu-id="f5329-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5329-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="f5329-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5329-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="f5329-118">Protocol specifications</span></span>

<span data-ttu-id="f5329-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5329-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5329-120">提供了相关的 Microsoft Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="f5329-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5329-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5329-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5329-122">指定的属性和电子邮件消息对象在允许的操作。</span><span class="sxs-lookup"><span data-stu-id="f5329-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="f5329-123">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5329-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5329-124">进行编码和解码为有效的流表示形式的消息和附件对象。</span><span class="sxs-lookup"><span data-stu-id="f5329-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5329-125">头文件</span><span class="sxs-lookup"><span data-stu-id="f5329-125">Header files</span></span>

<span data-ttu-id="f5329-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5329-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5329-127">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="f5329-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5329-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5329-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f5329-129">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="f5329-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5329-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5329-130">See also</span></span>



[<span data-ttu-id="f5329-131">IPM 子树</span><span class="sxs-lookup"><span data-stu-id="f5329-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="f5329-132">MAPI 特殊文件夹</span><span class="sxs-lookup"><span data-stu-id="f5329-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="f5329-133">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="f5329-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5329-134">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="f5329-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5329-135">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="f5329-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5329-136">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="f5329-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
