---
title: PidLidSharingRemoteUid 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: cb8b4a7c71f3ad81949f3eac6cab230f40c6d487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777039"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="d4e19-103">PidLidSharingRemoteUid 规范属性</span><span class="sxs-lookup"><span data-stu-id="d4e19-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="d4e19-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="d4e19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4e19-105">指定要共享的远程文件夹的条目 ID。</span><span class="sxs-lookup"><span data-stu-id="d4e19-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="d4e19-106">这是邮件的共享的属性。</span><span class="sxs-lookup"><span data-stu-id="d4e19-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4e19-107">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="d4e19-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4e19-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="d4e19-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="d4e19-109">属性进行设置：</span><span class="sxs-lookup"><span data-stu-id="d4e19-109">Property set:</span></span>  <br/> |<span data-ttu-id="d4e19-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d4e19-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d4e19-111">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="d4e19-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4e19-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="d4e19-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="d4e19-113">数据类型：</span><span class="sxs-lookup"><span data-stu-id="d4e19-113">Data type:</span></span>  <br/> |<span data-ttu-id="d4e19-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4e19-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d4e19-115">区域：</span><span class="sxs-lookup"><span data-stu-id="d4e19-115">Area:</span></span>  <br/> |<span data-ttu-id="d4e19-116">共享</span><span class="sxs-lookup"><span data-stu-id="d4e19-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4e19-117">备注</span><span class="sxs-lookup"><span data-stu-id="d4e19-117">Remarks</span></span>

<span data-ttu-id="d4e19-118">此属性必须设置为 PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) 属性的值的十六进制字符串表示形式中，在共享文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d4e19-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="d4e19-119">这是邮件的共享的属性。</span><span class="sxs-lookup"><span data-stu-id="d4e19-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4e19-120">相关资源</span><span class="sxs-lookup"><span data-stu-id="d4e19-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4e19-121">协议规范</span><span class="sxs-lookup"><span data-stu-id="d4e19-121">Protocol specifications</span></span>

<span data-ttu-id="d4e19-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4e19-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4e19-123">提供属性集定义和相关的 Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="d4e19-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4e19-124">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4e19-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4e19-125">共享客户端之间的邮箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="d4e19-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4e19-126">头文件</span><span class="sxs-lookup"><span data-stu-id="d4e19-126">Header files</span></span>

<span data-ttu-id="d4e19-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4e19-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4e19-128">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="d4e19-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4e19-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4e19-129">See also</span></span>



[<span data-ttu-id="d4e19-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="d4e19-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4e19-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="d4e19-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4e19-132">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="d4e19-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4e19-133">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="d4e19-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
