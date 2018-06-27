---
title: PidTagRuleProvider 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 5456e0abffd1ac25983809d32fde88644eaa01cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778291"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="2ef88-103">PidTagRuleProvider 规范属性</span><span class="sxs-lookup"><span data-stu-id="2ef88-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="2ef88-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="2ef88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ef88-105">包含的应用程序设置规则的名称。</span><span class="sxs-lookup"><span data-stu-id="2ef88-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ef88-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="2ef88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ef88-107">PR_RULE_PROVIDER，PR_RULE_PROVIDER_A，PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="2ef88-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="2ef88-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="2ef88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ef88-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="2ef88-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="2ef88-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="2ef88-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ef88-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ef88-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ef88-112">区域：</span><span class="sxs-lookup"><span data-stu-id="2ef88-112">Area:</span></span>  <br/> |<span data-ttu-id="2ef88-113">服务器端规则</span><span class="sxs-lookup"><span data-stu-id="2ef88-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ef88-114">备注</span><span class="sxs-lookup"><span data-stu-id="2ef88-114">Remarks</span></span>

<span data-ttu-id="2ef88-115">延迟操作需要这些属性来标识的代码必须解释和执行规则操作。</span><span class="sxs-lookup"><span data-stu-id="2ef88-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="2ef88-116">规则存储邮箱和文件夹是拥有这些规则提供程序字符串的应用程序相关联。</span><span class="sxs-lookup"><span data-stu-id="2ef88-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="2ef88-117">规则提供程序设置，并处理规则表中的规则。</span><span class="sxs-lookup"><span data-stu-id="2ef88-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="2ef88-118">它还提供了一种如果设置此类规则处理所有延迟的操作。</span><span class="sxs-lookup"><span data-stu-id="2ef88-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="2ef88-119">信息存储隐式创建延迟的操作。</span><span class="sxs-lookup"><span data-stu-id="2ef88-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="2ef88-120">移动或复制到其他存储的操作，如果提供程序设置的延迟的操作规则，它必须提供一个处理程序以执行操作时触发规则并创建延迟的操作。</span><span class="sxs-lookup"><span data-stu-id="2ef88-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ef88-121">相关资源</span><span class="sxs-lookup"><span data-stu-id="2ef88-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ef88-122">协议规范</span><span class="sxs-lookup"><span data-stu-id="2ef88-122">Protocol specifications</span></span>

<span data-ttu-id="2ef88-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ef88-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ef88-124">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="2ef88-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ef88-125">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ef88-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ef88-126">处理传入的电子邮件服务器上。</span><span class="sxs-lookup"><span data-stu-id="2ef88-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ef88-127">头文件</span><span class="sxs-lookup"><span data-stu-id="2ef88-127">Header files</span></span>

<span data-ttu-id="2ef88-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ef88-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ef88-129">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="2ef88-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ef88-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ef88-130">Mapitags.h</span></span>
  
> <span data-ttu-id="2ef88-131">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="2ef88-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ef88-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ef88-132">See also</span></span>



[<span data-ttu-id="2ef88-133">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="2ef88-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ef88-134">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="2ef88-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ef88-135">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="2ef88-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ef88-136">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="2ef88-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
