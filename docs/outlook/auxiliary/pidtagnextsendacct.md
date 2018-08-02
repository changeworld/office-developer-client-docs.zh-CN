---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: 指定辅助 accountsendstamp 的邮件。
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19774429"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="96150-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="96150-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="96150-104">指定的第二帐户"发送"戳的邮件。</span><span class="sxs-lookup"><span data-stu-id="96150-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96150-105">快速信息</span><span class="sxs-lookup"><span data-stu-id="96150-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96150-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="96150-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96150-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="96150-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="96150-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="96150-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96150-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="96150-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="96150-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="96150-110">Data type:</span></span>  <br/> |<span data-ttu-id="96150-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96150-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="96150-112">区域：</span><span class="sxs-lookup"><span data-stu-id="96150-112">Area:</span></span>  <br/> |<span data-ttu-id="96150-113">Outlook 应用程序</span><span class="sxs-lookup"><span data-stu-id="96150-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96150-114">说明</span><span class="sxs-lookup"><span data-stu-id="96150-114">Remarks</span></span>

<span data-ttu-id="96150-115">此属性适用于 MAPI message 对象。</span><span class="sxs-lookup"><span data-stu-id="96150-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="96150-116">收到的邮件，辅助帐户"发送"戳指示转发或答复应发送，使用的帐户，如果不能转发或答复发送与主帐户。</span><span class="sxs-lookup"><span data-stu-id="96150-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="96150-117">对于传出消息，辅助帐户"发送"戳确定使用哪些帐户发送邮件，如果无法与主帐户发送邮件。</span><span class="sxs-lookup"><span data-stu-id="96150-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="96150-118">其值是帐户的用于发送邮件的[IOlkAccount](iolkaccount.md)接口的[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)值。</span><span class="sxs-lookup"><span data-stu-id="96150-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96150-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96150-119">See also</span></span>

- [<span data-ttu-id="96150-120">常量 （帐户管理 API）</span><span class="sxs-lookup"><span data-stu-id="96150-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="96150-121">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="96150-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="96150-122">PidTagNextSendAcct 规范属性</span><span class="sxs-lookup"><span data-stu-id="96150-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)
