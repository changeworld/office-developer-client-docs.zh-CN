---
title: PidLidReferenceEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReferenceEntryId
api_type:
- COM
ms.assetid: 42e7c3ac-1a04-4e3f-bf99-ef3f8fc45892
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 736b4e7354929fa7ba5d6bdfea23bb2169244a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776983"
---
# <a name="pidlidreferenceentryid-canonical-property"></a><span data-ttu-id="6e62b-103">PidLidReferenceEntryId 规范属性</span><span class="sxs-lookup"><span data-stu-id="6e62b-103">PidLidReferenceEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6e62b-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="6e62b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e62b-105">指定联系人的引用[ENTRYID](entryid.md) 。</span><span class="sxs-lookup"><span data-stu-id="6e62b-105">Specifies the reference [ENTRYID](entryid.md) for the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e62b-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="6e62b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e62b-107">dispidReferenceEID</span><span class="sxs-lookup"><span data-stu-id="6e62b-107">dispidReferenceEID</span></span>  <br/> |
|<span data-ttu-id="6e62b-108">属性进行设置：</span><span class="sxs-lookup"><span data-stu-id="6e62b-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e62b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e62b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e62b-110">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="6e62b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e62b-111">0x000085BD</span><span class="sxs-lookup"><span data-stu-id="6e62b-111">0x000085BD</span></span>  <br/> |
|<span data-ttu-id="6e62b-112">数据类型：</span><span class="sxs-lookup"><span data-stu-id="6e62b-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e62b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e62b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e62b-114">区域：</span><span class="sxs-lookup"><span data-stu-id="6e62b-114">Area:</span></span>  <br/> |<span data-ttu-id="6e62b-115">联系人</span><span class="sxs-lookup"><span data-stu-id="6e62b-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e62b-116">说明</span><span class="sxs-lookup"><span data-stu-id="6e62b-116">Remarks</span></span>

<span data-ttu-id="6e62b-117">如果存在此参数，此属性应等于的联系人的**EntryId**的值。</span><span class="sxs-lookup"><span data-stu-id="6e62b-117">If present, this property should be equal to the value of the **EntryId** of the contact.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e62b-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="6e62b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e62b-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="6e62b-119">Protocol specifications</span></span>

<span data-ttu-id="6e62b-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e62b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e62b-121">提供属性集定义和相关的 Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="6e62b-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e62b-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e62b-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e62b-123">指定的属性和操作所允许的联系人和个人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="6e62b-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e62b-124">头文件</span><span class="sxs-lookup"><span data-stu-id="6e62b-124">Header files</span></span>

<span data-ttu-id="6e62b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e62b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e62b-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="6e62b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e62b-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e62b-127">See also</span></span>



[<span data-ttu-id="6e62b-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="6e62b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e62b-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="6e62b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e62b-130">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="6e62b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e62b-131">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="6e62b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
