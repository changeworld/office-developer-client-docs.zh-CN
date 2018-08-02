---
title: PidTagFormHostMap 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777662"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="97fd7-103">PidTagFormHostMap 规范属性</span><span class="sxs-lookup"><span data-stu-id="97fd7-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="97fd7-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="97fd7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97fd7-105">包含主机地图的可用窗体。</span><span class="sxs-lookup"><span data-stu-id="97fd7-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97fd7-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="97fd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97fd7-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="97fd7-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="97fd7-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="97fd7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97fd7-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="97fd7-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="97fd7-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="97fd7-110">Data type:</span></span>  <br/> |<span data-ttu-id="97fd7-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="97fd7-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="97fd7-112">区域：</span><span class="sxs-lookup"><span data-stu-id="97fd7-112">Area:</span></span>  <br/> |<span data-ttu-id="97fd7-113">常见的 MAPI</span><span class="sxs-lookup"><span data-stu-id="97fd7-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97fd7-114">说明</span><span class="sxs-lookup"><span data-stu-id="97fd7-114">Remarks</span></span>

<span data-ttu-id="97fd7-115">更改**IMAPIFormProp**接口的基础结构时，客户端应用程序应更新以及**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 属性，此属性。</span><span class="sxs-lookup"><span data-stu-id="97fd7-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="97fd7-116">相关资源</span><span class="sxs-lookup"><span data-stu-id="97fd7-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="97fd7-117">头文件</span><span class="sxs-lookup"><span data-stu-id="97fd7-117">Header files</span></span>

<span data-ttu-id="97fd7-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97fd7-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="97fd7-119">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="97fd7-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="97fd7-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97fd7-120">Mapitags.h</span></span>
  
> <span data-ttu-id="97fd7-121">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="97fd7-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97fd7-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97fd7-122">See also</span></span>



[<span data-ttu-id="97fd7-123">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="97fd7-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97fd7-124">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="97fd7-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97fd7-125">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="97fd7-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97fd7-126">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="97fd7-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
