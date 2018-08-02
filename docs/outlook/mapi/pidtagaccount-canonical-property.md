---
title: PidTagAccount 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777296"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="71b09-103">PidTagAccount 规范属性</span><span class="sxs-lookup"><span data-stu-id="71b09-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="71b09-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="71b09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71b09-105">包含收件人的帐户名称。</span><span class="sxs-lookup"><span data-stu-id="71b09-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71b09-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="71b09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71b09-107">PR_ACCOUNT，PR_ACCOUNT_A，PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="71b09-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="71b09-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="71b09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71b09-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="71b09-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="71b09-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="71b09-110">Data type:</span></span>  <br/> |<span data-ttu-id="71b09-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71b09-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="71b09-112">区域：</span><span class="sxs-lookup"><span data-stu-id="71b09-112">Area:</span></span>  <br/> |<span data-ttu-id="71b09-113">通讯簿</span><span class="sxs-lookup"><span data-stu-id="71b09-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71b09-114">说明</span><span class="sxs-lookup"><span data-stu-id="71b09-114">Remarks</span></span>

<span data-ttu-id="71b09-115">这些属性提供标识和访问收件人的信息。</span><span class="sxs-lookup"><span data-stu-id="71b09-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="71b09-116">它们是按收件人和组织定义的。</span><span class="sxs-lookup"><span data-stu-id="71b09-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="71b09-117">这些属性通常包含收件人的电子邮件名，即，唯一标识本地组织中的收件人的电子邮件地址的最后一个组件。</span><span class="sxs-lookup"><span data-stu-id="71b09-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="71b09-118">电子邮件名称对应于 X.400 可分辨名称，这意味着要一定要为特定邮件的域中唯一的短名称。</span><span class="sxs-lookup"><span data-stu-id="71b09-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71b09-119">相关资源</span><span class="sxs-lookup"><span data-stu-id="71b09-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71b09-120">协议规范</span><span class="sxs-lookup"><span data-stu-id="71b09-120">Protocol specifications</span></span>

<span data-ttu-id="71b09-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71b09-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71b09-122">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="71b09-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71b09-123">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71b09-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71b09-124">指定的属性和操作所允许的联系人和个人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="71b09-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="71b09-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71b09-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71b09-126">指定的属性和用户、 联系人、 组和资源的操作列表。</span><span class="sxs-lookup"><span data-stu-id="71b09-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71b09-127">头文件</span><span class="sxs-lookup"><span data-stu-id="71b09-127">Header files</span></span>

<span data-ttu-id="71b09-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71b09-128">mapitags.h</span></span>
  
> <span data-ttu-id="71b09-129">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="71b09-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="71b09-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71b09-130">mapidefs.h</span></span>
  
> <span data-ttu-id="71b09-131">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="71b09-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71b09-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71b09-132">See also</span></span>



[<span data-ttu-id="71b09-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="71b09-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="71b09-134">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="71b09-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71b09-135">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="71b09-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71b09-136">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="71b09-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
