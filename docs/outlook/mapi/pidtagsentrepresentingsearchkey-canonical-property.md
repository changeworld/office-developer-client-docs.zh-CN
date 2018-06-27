---
title: PidTagSentRepresentingSearchKey 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: d18a595a1019c3bd583ef0c38ee5cbe0d497bf93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778385"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="bf1f7-103">PidTagSentRepresentingSearchKey 规范属性</span><span class="sxs-lookup"><span data-stu-id="bf1f7-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bf1f7-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="bf1f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf1f7-105">包含表示发件人的邮件用户的搜索键。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf1f7-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="bf1f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf1f7-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bf1f7-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bf1f7-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="bf1f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf1f7-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="bf1f7-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="bf1f7-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="bf1f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf1f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bf1f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bf1f7-112">区域：</span><span class="sxs-lookup"><span data-stu-id="bf1f7-112">Area:</span></span>  <br/> |<span data-ttu-id="bf1f7-113">Address</span><span class="sxs-lookup"><span data-stu-id="bf1f7-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf1f7-114">备注</span><span class="sxs-lookup"><span data-stu-id="bf1f7-114">Remarks</span></span>

<span data-ttu-id="bf1f7-115">此属性是一个由发件人的邮件用户的地址属性。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="bf1f7-116">当客户端应用程序发送消息代表另一个客户端时，它应为该客户端的值设置所有表示发件人属性。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="bf1f7-117">通常在其自己的代表发送消息用户离开表示发件人属性未设置。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="bf1f7-118">传出的传输提供程序必须始终保持不变，如果已发送的客户端设置此属性。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="bf1f7-119">如果未设置它，应出站邮件，副本上将其设置为**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) 传输提供程序并将其上的本地副本中保留未设置。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf1f7-120">相关资源</span><span class="sxs-lookup"><span data-stu-id="bf1f7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf1f7-121">协议规范</span><span class="sxs-lookup"><span data-stu-id="bf1f7-121">Protocol specifications</span></span>

<span data-ttu-id="bf1f7-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-123">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf1f7-124">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-125">指定的属性和操作所允许的电子邮件消息对象。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bf1f7-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-127">处理顺序和客户端和服务器之间的数据传输的流。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="bf1f7-128">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-129">IETF RFC2445、 RFC2446，和 RFC2447，和约会和会议对象之间进行转换。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="bf1f7-130">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-131">指定的属性和约会、 会议请求和响应消息的操作。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bf1f7-132">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-133">指定的属性和允许的操作的 post 对象。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="bf1f7-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1f7-135">指定的属性和操作所允许的联系人和个人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf1f7-136">头文件</span><span class="sxs-lookup"><span data-stu-id="bf1f7-136">Header files</span></span>

<span data-ttu-id="bf1f7-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf1f7-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf1f7-138">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf1f7-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf1f7-139">Mapitags.h</span></span>
  
> <span data-ttu-id="bf1f7-140">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="bf1f7-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf1f7-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf1f7-141">See also</span></span>



[<span data-ttu-id="bf1f7-142">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="bf1f7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf1f7-143">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="bf1f7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf1f7-144">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="bf1f7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf1f7-145">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="bf1f7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
