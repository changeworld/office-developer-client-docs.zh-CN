---
title: PidTagOriginalSenderName 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: ae0ae8536f4f088bae4561e123afce716b623414
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777952"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="0f863-103">PidTagOriginalSenderName 规范属性</span><span class="sxs-lookup"><span data-stu-id="0f863-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="0f863-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="0f863-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f863-105">包含一条消息，即之前正在转发或答复邮件的第一个版本的发件人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="0f863-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f863-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="0f863-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f863-107">PR_ORIGINAL_SENDER_NAME，PR_ORIGINAL_SENDER_NAME_A，PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0f863-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0f863-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="0f863-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f863-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="0f863-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="0f863-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="0f863-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f863-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f863-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0f863-112">区域：</span><span class="sxs-lookup"><span data-stu-id="0f863-112">Area:</span></span>  <br/> |<span data-ttu-id="0f863-113">常规消息</span><span class="sxs-lookup"><span data-stu-id="0f863-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f863-114">说明</span><span class="sxs-lookup"><span data-stu-id="0f863-114">Remarks</span></span>

<span data-ttu-id="0f863-115">这些属性是一条消息的原始发件人的地址属性的示例。</span><span class="sxs-lookup"><span data-stu-id="0f863-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="0f863-116">在首次提交邮件，客户端应用程序应将这些属性设置为**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) 属性的值。</span><span class="sxs-lookup"><span data-stu-id="0f863-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="0f863-117">当转发或答复邮件永远不会更改它。</span><span class="sxs-lookup"><span data-stu-id="0f863-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f863-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="0f863-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f863-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="0f863-119">Protocol specifications</span></span>

<span data-ttu-id="0f863-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f863-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f863-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="0f863-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f863-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f863-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f863-123">指定的属性和电子邮件消息对象在允许的操作。</span><span class="sxs-lookup"><span data-stu-id="0f863-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f863-124">头文件</span><span class="sxs-lookup"><span data-stu-id="0f863-124">Header files</span></span>

<span data-ttu-id="0f863-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f863-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f863-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="0f863-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f863-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f863-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0f863-128">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="0f863-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f863-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f863-129">See also</span></span>



[<span data-ttu-id="0f863-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="0f863-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f863-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="0f863-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f863-132">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="0f863-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f863-133">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="0f863-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
