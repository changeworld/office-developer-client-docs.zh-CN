---
title: PidTagExtendedRuleSizeLimit 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777611"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="a1bed-103">PidTagExtendedRuleSizeLimit 规范属性</span><span class="sxs-lookup"><span data-stu-id="a1bed-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="a1bed-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="a1bed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1bed-105">包含的最大大小，以字节为单位，允许用户进行累加为一个"扩展"规则。</span><span class="sxs-lookup"><span data-stu-id="a1bed-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1bed-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="a1bed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1bed-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="a1bed-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="a1bed-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="a1bed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1bed-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="a1bed-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="a1bed-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="a1bed-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1bed-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a1bed-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a1bed-112">区域：</span><span class="sxs-lookup"><span data-stu-id="a1bed-112">Area:</span></span>  <br/> |<span data-ttu-id="a1bed-113">规则</span><span class="sxs-lookup"><span data-stu-id="a1bed-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1bed-114">说明</span><span class="sxs-lookup"><span data-stu-id="a1bed-114">Remarks</span></span>

<span data-ttu-id="a1bed-115">如果登录对象上设置此属性，则客户端应保留下指定此属性的值的**PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) 属性的大小。</span><span class="sxs-lookup"><span data-stu-id="a1bed-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="a1bed-116">相反，如果客户端执行尝试设置太大二进制属性服务器应返回错误。</span><span class="sxs-lookup"><span data-stu-id="a1bed-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="a1bed-117">有关扩展规则的信息，请参阅[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a1bed-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1bed-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="a1bed-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1bed-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="a1bed-119">Protocol specifications</span></span>

<span data-ttu-id="a1bed-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1bed-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1bed-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="a1bed-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1bed-122">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1bed-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1bed-123">指定允许的操作的核心消息存储对象。</span><span class="sxs-lookup"><span data-stu-id="a1bed-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1bed-124">头文件</span><span class="sxs-lookup"><span data-stu-id="a1bed-124">Header files</span></span>

<span data-ttu-id="a1bed-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1bed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1bed-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="a1bed-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1bed-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1bed-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a1bed-128">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="a1bed-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1bed-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1bed-129">See also</span></span>



[<span data-ttu-id="a1bed-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="a1bed-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1bed-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="a1bed-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1bed-132">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="a1bed-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1bed-133">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="a1bed-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
