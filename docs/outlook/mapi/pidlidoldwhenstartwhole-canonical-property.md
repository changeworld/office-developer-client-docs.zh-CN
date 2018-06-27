---
title: PidLidOldWhenStartWhole 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOldWhenStartWhole
api_type:
- COM
ms.assetid: 73064a22-68bf-4d3f-91f5-1eec807debf8
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 2dfc6859b596d74af9337ff462e357c95f2ec591
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776944"
---
# <a name="pidlidoldwhenstartwhole-canonical-property"></a><span data-ttu-id="603d9-103">PidLidOldWhenStartWhole 规范属性</span><span class="sxs-lookup"><span data-stu-id="603d9-103">PidLidOldWhenStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="603d9-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="603d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="603d9-105">指示会议更新之前的**dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) 属性的原始值。</span><span class="sxs-lookup"><span data-stu-id="603d9-105">Indicates the original value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property before a meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="603d9-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="603d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="603d9-107">dispidOldWhenStartWhole</span><span class="sxs-lookup"><span data-stu-id="603d9-107">dispidOldWhenStartWhole</span></span>  <br/> |
|<span data-ttu-id="603d9-108">属性进行设置：</span><span class="sxs-lookup"><span data-stu-id="603d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="603d9-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="603d9-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="603d9-110">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="603d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="603d9-111">0x00000029</span><span class="sxs-lookup"><span data-stu-id="603d9-111">0x00000029</span></span>  <br/> |
|<span data-ttu-id="603d9-112">数据类型：</span><span class="sxs-lookup"><span data-stu-id="603d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="603d9-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="603d9-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="603d9-114">区域：</span><span class="sxs-lookup"><span data-stu-id="603d9-114">Area:</span></span>  <br/> |<span data-ttu-id="603d9-115">会议</span><span class="sxs-lookup"><span data-stu-id="603d9-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="603d9-116">备注</span><span class="sxs-lookup"><span data-stu-id="603d9-116">Remarks</span></span>

<span data-ttu-id="603d9-117">此属性不是必需的。</span><span class="sxs-lookup"><span data-stu-id="603d9-117">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="603d9-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="603d9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="603d9-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="603d9-119">Protocol specifications</span></span>

<span data-ttu-id="603d9-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="603d9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="603d9-121">提供属性集定义和相关的 Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="603d9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="603d9-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="603d9-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="603d9-123">指定的属性和约会、 会议请求和响应消息的操作。</span><span class="sxs-lookup"><span data-stu-id="603d9-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="603d9-124">头文件</span><span class="sxs-lookup"><span data-stu-id="603d9-124">Header files</span></span>

<span data-ttu-id="603d9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="603d9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="603d9-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="603d9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="603d9-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="603d9-127">See also</span></span>



[<span data-ttu-id="603d9-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="603d9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="603d9-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="603d9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="603d9-130">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="603d9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="603d9-131">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="603d9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
