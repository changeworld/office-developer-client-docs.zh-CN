---
title: PidTagUserX509Certificate 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778534"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="7021f-103">PidTagUserX509Certificate 规范属性</span><span class="sxs-lookup"><span data-stu-id="7021f-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="7021f-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="7021f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7021f-105">包含消息的用户的 X.509 版本 3 安全证书。</span><span class="sxs-lookup"><span data-stu-id="7021f-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7021f-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="7021f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7021f-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="7021f-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="7021f-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="7021f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7021f-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="7021f-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="7021f-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="7021f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7021f-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="7021f-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="7021f-112">区域：</span><span class="sxs-lookup"><span data-stu-id="7021f-112">Area:</span></span>  <br/> |<span data-ttu-id="7021f-113">MAPI 邮件用户</span><span class="sxs-lookup"><span data-stu-id="7021f-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7021f-114">说明</span><span class="sxs-lookup"><span data-stu-id="7021f-114">Remarks</span></span>

<span data-ttu-id="7021f-115">利用公钥安全的应用程序使用此属性。</span><span class="sxs-lookup"><span data-stu-id="7021f-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="7021f-116">它包含一个或多个 X.509 版本 3 安全证书的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="7021f-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="7021f-117">对于自己的安全证书，各种应用程序和客户端可以使用此属性。</span><span class="sxs-lookup"><span data-stu-id="7021f-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="7021f-118">X.509 数据的二进制格式可以因供应商。</span><span class="sxs-lookup"><span data-stu-id="7021f-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7021f-119">相关资源</span><span class="sxs-lookup"><span data-stu-id="7021f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7021f-120">协议规范</span><span class="sxs-lookup"><span data-stu-id="7021f-120">Protocol specifications</span></span>

<span data-ttu-id="7021f-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7021f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7021f-122">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="7021f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7021f-123">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7021f-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7021f-124">指定的属性和用户、 联系人、 组和资源的操作列表。</span><span class="sxs-lookup"><span data-stu-id="7021f-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7021f-125">头文件</span><span class="sxs-lookup"><span data-stu-id="7021f-125">Header files</span></span>

<span data-ttu-id="7021f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7021f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7021f-127">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="7021f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7021f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7021f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7021f-129">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="7021f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7021f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7021f-130">See also</span></span>



[<span data-ttu-id="7021f-131">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="7021f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7021f-132">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="7021f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7021f-133">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="7021f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7021f-134">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="7021f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
