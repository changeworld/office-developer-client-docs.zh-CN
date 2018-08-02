---
title: PidTagContentReturnRequested 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentReturnRequested
api_type:
- HeaderDef
ms.assetid: f86f7c59-42ab-4ac0-80fe-c985103e6bd6
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: b4aaf05cdd8c85736215bd0d0f3a8c5c9dafecf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777488"
---
# <a name="pidtagcontentreturnrequested-canonical-property"></a><span data-ttu-id="af736-103">PidTagContentReturnRequested 规范属性</span><span class="sxs-lookup"><span data-stu-id="af736-103">PidTagContentReturnRequested Canonical Property</span></span>

  
  
<span data-ttu-id="af736-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="af736-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af736-105">包含 TRUE，则应与原件报告返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="af736-105">Contains TRUE if a message should be returned with a nondelivery report.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af736-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="af736-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af736-107">PR_CONTENT_RETURN_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="af736-107">PR_CONTENT_RETURN_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="af736-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="af736-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af736-109">0x000A</span><span class="sxs-lookup"><span data-stu-id="af736-109">0x000A</span></span>  <br/> |
|<span data-ttu-id="af736-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="af736-110">Data type:</span></span>  <br/> |<span data-ttu-id="af736-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="af736-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="af736-112">区域：</span><span class="sxs-lookup"><span data-stu-id="af736-112">Area:</span></span>  <br/> |<span data-ttu-id="af736-113">Report</span><span class="sxs-lookup"><span data-stu-id="af736-113">Report</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af736-114">注解</span><span class="sxs-lookup"><span data-stu-id="af736-114">Remarks</span></span>

<span data-ttu-id="af736-115">如果未设置此属性，MAPI 会将其视为 TRUE 值。</span><span class="sxs-lookup"><span data-stu-id="af736-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af736-116">相关资源</span><span class="sxs-lookup"><span data-stu-id="af736-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="af736-117">头文件</span><span class="sxs-lookup"><span data-stu-id="af736-117">Header files</span></span>

<span data-ttu-id="af736-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af736-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="af736-119">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="af736-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="af736-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af736-120">Mapitags.h</span></span>
  
> <span data-ttu-id="af736-121">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="af736-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af736-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af736-122">See also</span></span>



[<span data-ttu-id="af736-123">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="af736-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af736-124">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="af736-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af736-125">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="af736-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af736-126">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="af736-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
