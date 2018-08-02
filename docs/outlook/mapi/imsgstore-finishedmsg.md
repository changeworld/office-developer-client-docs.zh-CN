---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 9da9a13f87eac097fba078da1f1d6c3f78f69c0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775883"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="c60ae-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="c60ae-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="c60ae-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="c60ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c60ae-105">启用对已发送的邮件执行处理的消息存储提供程序。</span><span class="sxs-lookup"><span data-stu-id="c60ae-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="c60ae-106">只能通过 MAPI 后台处理程序调用此方法。</span><span class="sxs-lookup"><span data-stu-id="c60ae-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="c60ae-107">参数</span><span class="sxs-lookup"><span data-stu-id="c60ae-107">Parameters</span></span>

 <span data-ttu-id="c60ae-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c60ae-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c60ae-109">[in]保留;必须为零。</span><span class="sxs-lookup"><span data-stu-id="c60ae-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c60ae-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c60ae-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="c60ae-111">[in]在_lpEntryID_参数指向的项标识符的字节数。</span><span class="sxs-lookup"><span data-stu-id="c60ae-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c60ae-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c60ae-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="c60ae-113">[in]指向要处理的消息的项标识符的指针。</span><span class="sxs-lookup"><span data-stu-id="c60ae-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c60ae-114">返回值</span><span class="sxs-lookup"><span data-stu-id="c60ae-114">Return value</span></span>

<span data-ttu-id="c60ae-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c60ae-115">S_OK</span></span> 
  
> <span data-ttu-id="c60ae-116">在已发送的邮件处理成功。</span><span class="sxs-lookup"><span data-stu-id="c60ae-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="c60ae-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c60ae-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c60ae-118">消息存储提供程序不支持已发送的邮件处理。</span><span class="sxs-lookup"><span data-stu-id="c60ae-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="c60ae-119">如果呼叫者不是 MAPI 后台处理程序，则返回此错误值。</span><span class="sxs-lookup"><span data-stu-id="c60ae-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c60ae-120">说明</span><span class="sxs-lookup"><span data-stu-id="c60ae-120">Remarks</span></span>

<span data-ttu-id="c60ae-121">**IMsgStore::FinishedMsg**方法对已发送的邮件执行处理。</span><span class="sxs-lookup"><span data-stu-id="c60ae-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="c60ae-122">此过程可涉及删除邮件，并将其移动到另一个文件夹或两种操作。</span><span class="sxs-lookup"><span data-stu-id="c60ae-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="c60ae-123">处理的类型取决于是否设置**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 和**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 属性。</span><span class="sxs-lookup"><span data-stu-id="c60ae-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c60ae-124">针对实施者的注释</span><span class="sxs-lookup"><span data-stu-id="c60ae-124">Notes to implementers</span></span>

<span data-ttu-id="c60ae-125">**FinishedMsg**在实现，解除锁定邮件由_lpEntryID_标识，并执行相应的处理。</span><span class="sxs-lookup"><span data-stu-id="c60ae-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="c60ae-126">目标邮件总是被锁定;MAPI 后台处理程序永远不会将解除锁定的消息的项标识符传递给**FinishedMsg**。</span><span class="sxs-lookup"><span data-stu-id="c60ae-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="c60ae-127">很可能，既不设置**PR_DELETE_AFTER_SUBMIT**或**PR_SENTMAIL_ENTRYID** 、 两者都设置，或设置一个或另一个。</span><span class="sxs-lookup"><span data-stu-id="c60ae-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="c60ae-128">下表介绍您应执行的操作基于在设置:</span><span class="sxs-lookup"><span data-stu-id="c60ae-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c60ae-129">如果既属性设置：</span><span class="sxs-lookup"><span data-stu-id="c60ae-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="c60ae-130">将邮件保留从中发送 （通常发件箱） 的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="c60ae-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="c60ae-131">如果设置两个属性：</span><span class="sxs-lookup"><span data-stu-id="c60ae-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="c60ae-132">将邮件移动到指定的文件夹中，如果需要，并将其删除。</span><span class="sxs-lookup"><span data-stu-id="c60ae-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="c60ae-133">如果设置 PR_SENTMAIL_ENTRYID:</span><span class="sxs-lookup"><span data-stu-id="c60ae-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="c60ae-134">将邮件移动到指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="c60ae-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="c60ae-135">如果设置 PR_DELETE_AFTER_SUBMIT:</span><span class="sxs-lookup"><span data-stu-id="c60ae-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="c60ae-136">删除邮件。</span><span class="sxs-lookup"><span data-stu-id="c60ae-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="c60ae-137">您已采取任何操作适合后，调用[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c60ae-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c60ae-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c60ae-138">See also</span></span>



[<span data-ttu-id="c60ae-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="c60ae-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="c60ae-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c60ae-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
