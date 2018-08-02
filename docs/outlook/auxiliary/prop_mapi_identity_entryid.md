---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: 检索或设置的帐户的地址簿条目 ID。
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19774437"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="ada76-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ada76-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="ada76-104">检索或设置的帐户的地址簿条目 ID。</span><span class="sxs-lookup"><span data-stu-id="ada76-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ada76-105">快速信息</span><span class="sxs-lookup"><span data-stu-id="ada76-105">Quick info</span></span>

<span data-ttu-id="ada76-106">See [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ada76-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ada76-107">标识符:</span><span class="sxs-lookup"><span data-stu-id="ada76-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ada76-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="ada76-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="ada76-109">属性类型</span><span class="sxs-lookup"><span data-stu-id="ada76-109">Property type:</span></span>  <br/> |<span data-ttu-id="ada76-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ada76-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ada76-111">属性标记：</span><span class="sxs-lookup"><span data-stu-id="ada76-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ada76-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="ada76-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="ada76-113">访问权限</span><span class="sxs-lookup"><span data-stu-id="ada76-113">Access:</span></span>  <br/> |<span data-ttu-id="ada76-114">读/写</span><span class="sxs-lookup"><span data-stu-id="ada76-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ada76-115">备注</span><span class="sxs-lookup"><span data-stu-id="ada76-115">Remarks</span></span>

 <span data-ttu-id="ada76-116">**属性\_MAPI\_IDENTITY\_ENTRYID**不应存在于每个帐户上。</span><span class="sxs-lookup"><span data-stu-id="ada76-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="ada76-117">例如，可以有一个 Exchange 帐户**属性\_MAPI\_IDENTITY\_ENTRYID**设置，而不[属性\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)，而 SMTP/POP3 帐户的情况下将被颠倒。</span><span class="sxs-lookup"><span data-stu-id="ada76-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="ada76-118">**属性\_MAPI_IDENTITY_ENTRYID**返回类似于_lppEntryID_ [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)中返回的值的条目 ID。</span><span class="sxs-lookup"><span data-stu-id="ada76-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ada76-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ada76-119">See also</span></span>

- [<span data-ttu-id="ada76-120">有关帐户管理 API</span><span class="sxs-lookup"><span data-stu-id="ada76-120">About the Account Management API</span></span>](about-the-account-management-api.md)
