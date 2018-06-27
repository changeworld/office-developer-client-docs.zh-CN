---
title: PidTagCreationTime 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 475c93e7f2c246e0351f3054b0f827fb7ee015a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777512"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="b37d3-103">PidTagCreationTime 规范属性</span><span class="sxs-lookup"><span data-stu-id="b37d3-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="b37d3-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b37d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b37d3-105">包含的创建日期和时间一条消息。</span><span class="sxs-lookup"><span data-stu-id="b37d3-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b37d3-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="b37d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b37d3-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="b37d3-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="b37d3-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="b37d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b37d3-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="b37d3-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="b37d3-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="b37d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b37d3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b37d3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b37d3-112">区域：</span><span class="sxs-lookup"><span data-stu-id="b37d3-112">Area:</span></span>  <br/> |<span data-ttu-id="b37d3-113">消息时间</span><span class="sxs-lookup"><span data-stu-id="b37d3-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b37d3-114">备注</span><span class="sxs-lookup"><span data-stu-id="b37d3-114">Remarks</span></span>

<span data-ttu-id="b37d3-115">消息存储设置此属性为其创建每条消息。</span><span class="sxs-lookup"><span data-stu-id="b37d3-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b37d3-116">相关资源</span><span class="sxs-lookup"><span data-stu-id="b37d3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b37d3-117">协议规范</span><span class="sxs-lookup"><span data-stu-id="b37d3-117">Protocol specifications</span></span>

<span data-ttu-id="b37d3-118">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b37d3-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b37d3-119">处理邮件和附件的对象。</span><span class="sxs-lookup"><span data-stu-id="b37d3-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b37d3-120">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b37d3-120">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b37d3-121">指定的属性和用户、 联系人、 组和资源的操作列表。</span><span class="sxs-lookup"><span data-stu-id="b37d3-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b37d3-122">头文件</span><span class="sxs-lookup"><span data-stu-id="b37d3-122">Header files</span></span>

<span data-ttu-id="b37d3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b37d3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b37d3-124">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="b37d3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b37d3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b37d3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b37d3-126">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="b37d3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b37d3-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b37d3-127">See also</span></span>



[<span data-ttu-id="b37d3-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="b37d3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b37d3-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="b37d3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b37d3-130">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b37d3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b37d3-131">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b37d3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
