---
title: PidTagReadReceiptEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778103"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="3be5c-103">PidTagReadReceiptEntryId 规范属性</span><span class="sxs-lookup"><span data-stu-id="3be5c-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3be5c-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="3be5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3be5c-105">包含消息用户其中邮件系统应直接读取此消息的报表的项标识符。</span><span class="sxs-lookup"><span data-stu-id="3be5c-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3be5c-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="3be5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3be5c-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3be5c-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3be5c-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="3be5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3be5c-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="3be5c-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="3be5c-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="3be5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3be5c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3be5c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3be5c-112">区域：</span><span class="sxs-lookup"><span data-stu-id="3be5c-112">Area:</span></span>  <br/> |<span data-ttu-id="3be5c-113">MAPI 信封</span><span class="sxs-lookup"><span data-stu-id="3be5c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3be5c-114">说明</span><span class="sxs-lookup"><span data-stu-id="3be5c-114">Remarks</span></span>

<span data-ttu-id="3be5c-115">除非**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) 属性设置为 TRUE，则忽略此属性。</span><span class="sxs-lookup"><span data-stu-id="3be5c-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="3be5c-116">如果希望接收客户端应用程序读取报告本身，它可以将此属性未设置，或将其设置为消息提交次**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) 属性中包含的项标识符。</span><span class="sxs-lookup"><span data-stu-id="3be5c-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3be5c-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="3be5c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3be5c-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="3be5c-118">Protocol specifications</span></span>

<span data-ttu-id="3be5c-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3be5c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3be5c-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="3be5c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3be5c-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3be5c-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3be5c-122">指定的属性和电子邮件消息对象在允许的操作。</span><span class="sxs-lookup"><span data-stu-id="3be5c-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3be5c-123">头文件</span><span class="sxs-lookup"><span data-stu-id="3be5c-123">Header files</span></span>

<span data-ttu-id="3be5c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3be5c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3be5c-125">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="3be5c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3be5c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3be5c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3be5c-127">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="3be5c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3be5c-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3be5c-128">See also</span></span>



[<span data-ttu-id="3be5c-129">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="3be5c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3be5c-130">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="3be5c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3be5c-131">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="3be5c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3be5c-132">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="3be5c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
