---
title: PidTagRoamingXmlStream 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingXmlStream
api_type:
- COM
ms.assetid: ce55b50e-3dbf-4690-9102-c08f35ada82e
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: b64467db112932848129b88969e4084343629c86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778226"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="8a976-103">PidTagRoamingXmlStream 规范属性</span><span class="sxs-lookup"><span data-stu-id="8a976-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="8a976-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="8a976-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a976-105">包含任意 XML 流。</span><span class="sxs-lookup"><span data-stu-id="8a976-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a976-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="8a976-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a976-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="8a976-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="8a976-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="8a976-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a976-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="8a976-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="8a976-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="8a976-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a976-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a976-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a976-112">区域：</span><span class="sxs-lookup"><span data-stu-id="8a976-112">Area:</span></span>  <br/> |<span data-ttu-id="8a976-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="8a976-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a976-114">备注</span><span class="sxs-lookup"><span data-stu-id="8a976-114">Remarks</span></span>

<span data-ttu-id="8a976-115">此属性包含任意 XML 数据的流。</span><span class="sxs-lookup"><span data-stu-id="8a976-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="8a976-116">在邮件中的其他属性可能意味着要使用此属性中的特定架构。</span><span class="sxs-lookup"><span data-stu-id="8a976-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a976-117">相关资源</span><span class="sxs-lookup"><span data-stu-id="8a976-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a976-118">协议规范</span><span class="sxs-lookup"><span data-stu-id="8a976-118">Protocol specifications</span></span>

<span data-ttu-id="8a976-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a976-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a976-120">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="8a976-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a976-121">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a976-121">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a976-122">指定的位置和客户端和服务器配置数据，如共享的类别列表和工作时间的属性。</span><span class="sxs-lookup"><span data-stu-id="8a976-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a976-123">头文件</span><span class="sxs-lookup"><span data-stu-id="8a976-123">Header files</span></span>

<span data-ttu-id="8a976-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a976-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a976-125">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="8a976-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a976-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a976-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8a976-127">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="8a976-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a976-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a976-128">See also</span></span>



[<span data-ttu-id="8a976-129">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="8a976-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a976-130">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="8a976-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a976-131">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="8a976-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a976-132">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="8a976-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
