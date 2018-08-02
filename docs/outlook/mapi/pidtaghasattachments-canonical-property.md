---
title: PidTagHasAttachments 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 3b618e5a79c3b7e3810ea541aa9b905dfa4188a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777669"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="ff8a5-103">PidTagHasAttachments 规范属性</span><span class="sxs-lookup"><span data-stu-id="ff8a5-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="ff8a5-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="ff8a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff8a5-105">如果邮件包含至少一个附件，包含 TRUE。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff8a5-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="ff8a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff8a5-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="ff8a5-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="ff8a5-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="ff8a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff8a5-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="ff8a5-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="ff8a5-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="ff8a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff8a5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ff8a5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ff8a5-112">区域：</span><span class="sxs-lookup"><span data-stu-id="ff8a5-112">Area:</span></span>  <br/> |<span data-ttu-id="ff8a5-113">邮件附件</span><span class="sxs-lookup"><span data-stu-id="ff8a5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff8a5-114">说明</span><span class="sxs-lookup"><span data-stu-id="ff8a5-114">Remarks</span></span>

<span data-ttu-id="ff8a5-115">消息存储从**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) 属性的**MSGFLAG_HASATTACH**标志复制此属性。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="ff8a5-116">然后，客户端应用程序可以使用**PR_HASATTACH**排序所依据邮件查看器中的邮件附件。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="ff8a5-117">使用[IMAPIProp::SaveChanges](imapiprop-savechanges.md)方法都会更新此属性的值。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff8a5-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="ff8a5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff8a5-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="ff8a5-119">Protocol specifications</span></span>

<span data-ttu-id="ff8a5-120">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff8a5-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff8a5-121">指定的属性和操作所允许的电子邮件消息对象。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff8a5-122">头文件</span><span class="sxs-lookup"><span data-stu-id="ff8a5-122">Header files</span></span>

<span data-ttu-id="ff8a5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff8a5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff8a5-124">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff8a5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff8a5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ff8a5-126">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="ff8a5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff8a5-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff8a5-127">See also</span></span>



[<span data-ttu-id="ff8a5-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="ff8a5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff8a5-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="ff8a5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff8a5-130">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="ff8a5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff8a5-131">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="ff8a5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
