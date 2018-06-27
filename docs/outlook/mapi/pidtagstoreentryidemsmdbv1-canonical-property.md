---
title: PidTagStoreEntryIdEmsmdbV1 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778460"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="7c1fb-103">PidTagStoreEntryIdEmsmdbV1 规范属性</span><span class="sxs-lookup"><span data-stu-id="7c1fb-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="7c1fb-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="7c1fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c1fb-105">包含 Microsoft Exchange Server 2010 或 Exchange Server 2013 的消息存储的项标识符的旧样式 （Microsoft Outlook 2002 和更早版本）。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c1fb-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="7c1fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c1fb-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="7c1fb-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="7c1fb-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="7c1fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c1fb-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="7c1fb-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="7c1fb-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="7c1fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c1fb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7c1fb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7c1fb-112">区域：</span><span class="sxs-lookup"><span data-stu-id="7c1fb-112">Area:</span></span>  <br/> |<span data-ttu-id="7c1fb-113">ID 属性</span><span class="sxs-lookup"><span data-stu-id="7c1fb-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c1fb-114">备注</span><span class="sxs-lookup"><span data-stu-id="7c1fb-114">Remarks</span></span>

<span data-ttu-id="7c1fb-115">启动与 Microsoft Outlook 2003 的服务器 Fqdn 已集成到条目 Id，从而避免其他 Rpc 的引用。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="7c1fb-116">但是，这使得条目 Id 更长时间，并介绍了其中的**CompareEntryIDs**方法必须用于确定是否两个条目 Id 是等效的更多方案。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="7c1fb-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) 属性访问由 Microsoft Outlook 2002 (Microsoft Office XP) 和早期版本的 Exchange Server 条目 ID 的旧格式。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="7c1fb-118">这可以节省空间并还可以减少所需确定何时条目 Id 是等效的**CompareEntryIDs**呼叫的数目。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="7c1fb-119">请注意，使用旧条目 Id 打开邮箱可能会引发一些其他的 Rpc 是否需要引用。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="7c1fb-120">若要访问在缓存模式下的 PR_STORE_ENTRYID_EMSMDB_V1 属性，必须绕过缓存与[IMAPIProp::GetProps](imapiprop-getprops.md)方法使用 MAPI_NO_CACHE 标志。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="7c1fb-121">如果**PR_STORE_ENTRYID_EMSMDB_V1**不可用，则代码应回退到 PR_STORE_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="7c1fb-122">仅 Outlook 2003 通过 Microsoft Outlook 2013 支持 PR_STORE_ENTRYID_EMSMDB_V1 属性。</span><span class="sxs-lookup"><span data-stu-id="7c1fb-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c1fb-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c1fb-123">See also</span></span>



[<span data-ttu-id="7c1fb-124">PidTagStoreEntryId 规范属性</span><span class="sxs-lookup"><span data-stu-id="7c1fb-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="7c1fb-125">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="7c1fb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c1fb-126">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="7c1fb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c1fb-127">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="7c1fb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c1fb-128">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="7c1fb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
