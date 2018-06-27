---
title: PidLidContactLinkName 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkName
api_type:
- COM
ms.assetid: 7b9be1cd-e81e-42f3-b391-036afa2ae1b4
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 13c10a84383c9c2f775a7579485536bfd63f9a93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776729"
---
# <a name="pidlidcontactlinkname-canonical-property"></a><span data-ttu-id="c8672-103">PidLidContactLinkName 规范属性</span><span class="sxs-lookup"><span data-stu-id="c8672-103">PidLidContactLinkName Canonical Property</span></span>

  
  
<span data-ttu-id="c8672-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="c8672-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8672-105">包含**dispidContacts** ([PidLidContacts](pidlidcontacts-canonical-property.md)) 属性的元素。</span><span class="sxs-lookup"><span data-stu-id="c8672-105">Contains the elements of the **dispidContacts** ([PidLidContacts](pidlidcontacts-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8672-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="c8672-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8672-107">dispidContactLinkName</span><span class="sxs-lookup"><span data-stu-id="c8672-107">dispidContactLinkName</span></span>  <br/> |
|<span data-ttu-id="c8672-108">属性进行设置：</span><span class="sxs-lookup"><span data-stu-id="c8672-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8672-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c8672-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c8672-110">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="c8672-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c8672-111">0x00008586</span><span class="sxs-lookup"><span data-stu-id="c8672-111">0x00008586</span></span>  <br/> |
|<span data-ttu-id="c8672-112">数据类型：</span><span class="sxs-lookup"><span data-stu-id="c8672-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8672-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8672-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c8672-114">区域：</span><span class="sxs-lookup"><span data-stu-id="c8672-114">Area:</span></span>  <br/> |<span data-ttu-id="c8672-115">联系人</span><span class="sxs-lookup"><span data-stu-id="c8672-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8672-116">备注</span><span class="sxs-lookup"><span data-stu-id="c8672-116">Remarks</span></span>

<span data-ttu-id="c8672-117">由分号和空格分隔**dispidContactLinkName**属性中的元素 （";"）。</span><span class="sxs-lookup"><span data-stu-id="c8672-117">The elements in the **dispidContactLinkName** property are separated by a semicolon and a space ("; ").</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c8672-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="c8672-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8672-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="c8672-119">Protocol specifications</span></span>

<span data-ttu-id="c8672-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8672-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8672-121">提供属性集定义和相关的 Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="c8672-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8672-122">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8672-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8672-123">处理邮件和附件的对象。</span><span class="sxs-lookup"><span data-stu-id="c8672-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8672-124">头文件</span><span class="sxs-lookup"><span data-stu-id="c8672-124">Header files</span></span>

<span data-ttu-id="c8672-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8672-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8672-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="c8672-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8672-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8672-127">See also</span></span>



[<span data-ttu-id="c8672-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="c8672-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8672-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="c8672-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8672-130">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="c8672-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8672-131">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="c8672-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
