---
title: 支持格式化的文本消息存储职责
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778895"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a><span data-ttu-id="c42f5-103">支持的格式文本： 消息存储职责</span><span class="sxs-lookup"><span data-stu-id="c42f5-103">Supporting Formatted Text: Message Store Responsibilities</span></span>

  
  
<span data-ttu-id="c42f5-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="c42f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c42f5-105">消息存储提供程序使用**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) 属性可发布是否能够处理富文本格式 (RTF)、 HTML 文本和 RTF 感知时是否它们存储中的格式化的文本压缩或未压缩格式。</span><span class="sxs-lookup"><span data-stu-id="c42f5-105">Message store providers use the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to publish whether or not they can handle Rich Text Format (RTF), HTML text and, if they are RTF-aware, whether they store the formatted text in a compressed or uncompressed format.</span></span> <span data-ttu-id="c42f5-106">消息存储提供程序指示它们是 RTF 感知通过设置 STORE_RTF_OK 位以及它们存储格式化的文本未压缩窗体中通过设置 STORE_UNCOMPRESSED_RTF 位。</span><span class="sxs-lookup"><span data-stu-id="c42f5-106">Message store providers indicate that they are RTF-aware by setting the STORE_RTF_OK bit and that they store the formatted text in an uncompressed form by setting the STORE_UNCOMPRESSED_RTF bit.</span></span> <span data-ttu-id="c42f5-107">消息存储提供程序表明它们是 HTML 感知通过设置 STORE_HTML_OK 位。</span><span class="sxs-lookup"><span data-stu-id="c42f5-107">Message store providers indicate they are HTML-aware by setting the STORE_HTML_OK bit.</span></span>
  
<span data-ttu-id="c42f5-108">重要要检查的位以确定的消息存储支持 RTF STORE_RTF_OK RTF 感知客户端时，就不需要对客户端关心 RTF 感知存储格式化文本的格式。</span><span class="sxs-lookup"><span data-stu-id="c42f5-108">While it is important for an RTF-aware client to check for the STORE_RTF_OK bit to determine whether or not a message store supports RTF, it is not necessary for a client to be concerned with the format of an RTF-aware store's formatted text.</span></span> 
  
<span data-ttu-id="c42f5-109">所有邮件存储必须都支持非 RTF 感知客户端。</span><span class="sxs-lookup"><span data-stu-id="c42f5-109">All message stores must support non-RTF-aware clients.</span></span> <span data-ttu-id="c42f5-110">非 RTF 注意消息存储必须消息的[IMAPIProp::SaveChanges](imapiprop-savechanges.md)方法在呼叫过程中删除**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) 属性，如果客户端已而不更改**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))更新**PR_RTF_IN_SYNC**或**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="c42f5-110">A non-RTF-aware message store must delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property during a call to the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method if a client has changed **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) without updating either **PR_RTF_IN_SYNC** or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="c42f5-111">删除**PR_RTF_IN_SYNC**使重新计算**PR_BODY**属性中的下次 RTF 感知客户端调用[RTFSync](rtfsync.md) **PR_RTF_COMPRESSED**属性。</span><span class="sxs-lookup"><span data-stu-id="c42f5-111">Deleting **PR_RTF_IN_SYNC** causes the **PR_RTF_COMPRESSED** property to be recomputed from the **PR_BODY** property the next time an RTF-aware client calls [RTFSync](rtfsync.md).</span></span> 
  
<span data-ttu-id="c42f5-112">大多数 RTF 感知的消息存储由客户端; 不是授予消息文本它必须请求计算。</span><span class="sxs-lookup"><span data-stu-id="c42f5-112">Most RTF-aware message stores are not given the message text by clients; it must be computed on request.</span></span> <span data-ttu-id="c42f5-113">因为此计算非常耗时且成本低，客户端应使用**PR_RTF_COMPRESSED**尽可能。</span><span class="sxs-lookup"><span data-stu-id="c42f5-113">Because this computation is time consuming and expensive, clients should use **PR_RTF_COMPRESSED** whenever possible.</span></span> <span data-ttu-id="c42f5-114">若要计算的**PR_BODY**属性，消息存储提供程序必须解压缩**PR_RTF_COMPRESSED**属性的内容并删除格式文本格式。</span><span class="sxs-lookup"><span data-stu-id="c42f5-114">To compute the **PR_BODY** property, the message store provider must uncompress the contents of the **PR_RTF_COMPRESSED** property and remove the rich text formatting.</span></span> <span data-ttu-id="c42f5-115">不支持**PR_RTF_COMPRESSED**属性的客户端需要对每个消息执行此计算。</span><span class="sxs-lookup"><span data-stu-id="c42f5-115">Clients that do not support the **PR_RTF_COMPRESSED** property require this computation to take place for every message.</span></span> 
  
<span data-ttu-id="c42f5-116">当复制邮件，消息存储提供程序不使用运行的与任何内容创建一条消息，如果其实现排除**PR_BODY**风险**IMAPISupport::DoCopyProps**或**IMAPISupport::DoCopyTo**方法属性和依赖于**PR_RTF_COMPRESSED**。</span><span class="sxs-lookup"><span data-stu-id="c42f5-116">When copying messages, message store providers that do not use the **IMAPISupport::DoCopyProps** or **IMAPISupport::DoCopyTo** methods run the risk of creating a message with no content if their implementation excludes the **PR_BODY** property and relies on **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="c42f5-117">很可能已损坏的**PR_RTF_COMPRESSED**属性中的数据。</span><span class="sxs-lookup"><span data-stu-id="c42f5-117">It is possible for the data in the **PR_RTF_COMPRESSED** property to be corrupt.</span></span> <span data-ttu-id="c42f5-118">之前不包括复制操作这些消息内容属性之一，检查已损坏，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c42f5-118">Before excluding either of these message content properties in the copy operation, check for corruption as follows:</span></span> 
  
1. <span data-ttu-id="c42f5-119">如果不大于压缩 RTF **PR_RTF_COMPRESSED**的值，该属性已损坏。</span><span class="sxs-lookup"><span data-stu-id="c42f5-119">If the value of **PR_RTF_COMPRESSED** is not larger than the compressed RTF, the property is corrupt.</span></span> 
    
2. <span data-ttu-id="c42f5-120">如果在 RTF 标题魔术值不是_dwMagicCompressedRTF_或_dwMagicUncompressedRTF_，该属性已损坏。</span><span class="sxs-lookup"><span data-stu-id="c42f5-120">If the magic value in the RTF header is not  _dwMagicCompressedRTF_ or  _dwMagicUncompressedRTF_, the property is corrupt.</span></span>
    
<span data-ttu-id="c42f5-121">消息存储提供程序使用方法需要不考虑实现**PR_RTF_COMPRESSED**损坏; 检查的支持MAPI 确保的相应属性存在，且有效。</span><span class="sxs-lookup"><span data-stu-id="c42f5-121">Message store providers using the support methods need not be concerned with implementing a check for **PR_RTF_COMPRESSED** corruption; MAPI ensures that the appropriate properties exist and are valid.</span></span> 
  
<span data-ttu-id="c42f5-122">有三个不同级别的消息存储提供程序可以实现; RTF 支持MAPI 建议 RTF 感知消息存储提供程序实施他们的支持在中间或最高级别。</span><span class="sxs-lookup"><span data-stu-id="c42f5-122">There are three different levels of RTF support that message store providers can implement; MAPI recommends that RTF-aware message store providers implement their support at the middle or highest level.</span></span> <span data-ttu-id="c42f5-123">所有 RTF 感知消息存储提供程序的传出邮件**PR_RTF_COMPRESSED**中包括的数据从生成**PR_BODY**和**RTFSync**调用同步文本和传入消息的格式。</span><span class="sxs-lookup"><span data-stu-id="c42f5-123">All RTF-aware message store providers take care of generating **PR_BODY** from the data included in **PR_RTF_COMPRESSED** on outgoing messages and make a call to **RTFSync** to synchronize text and formatting on incoming messages.</span></span> 
  
<span data-ttu-id="c42f5-124">以下三个级别之间的差异如下表所述。</span><span class="sxs-lookup"><span data-stu-id="c42f5-124">The differences between these three levels are described in the following table.</span></span> 
  
|<span data-ttu-id="c42f5-125">**支持级别**</span><span class="sxs-lookup"><span data-stu-id="c42f5-125">**Level of support**</span></span>|<span data-ttu-id="c42f5-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="c42f5-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c42f5-127">Low</span><span class="sxs-lookup"><span data-stu-id="c42f5-127">Low</span></span>  <br/> |<span data-ttu-id="c42f5-128">消息存储提供程序调用**RTFSync** ，只要更改将保存到一条消息，并从**PR_RTF_COMPRESSED**而不是要求客户端将其设置为提取**PR_BODY**属性的数据。</span><span class="sxs-lookup"><span data-stu-id="c42f5-128">Message store provider calls **RTFSync** whenever changes are saved to a message and extracts the data for the **PR_BODY** property from **PR_RTF_COMPRESSED** rather than requiring clients to set it.</span></span> <span data-ttu-id="c42f5-129">**PR_BODY**和**PR_RTF_COMPRESSED**存储。</span><span class="sxs-lookup"><span data-stu-id="c42f5-129">Both **PR_BODY** and **PR_RTF_COMPRESSED** are stored.</span></span>  <br/> |
|<span data-ttu-id="c42f5-130">居中</span><span class="sxs-lookup"><span data-stu-id="c42f5-130">Middle</span></span>  <br/> |<span data-ttu-id="c42f5-131">消息存储提供程序存储仅**PR_RTF_COMPRESSED**属性，计算**PR_BODY**在必要时。</span><span class="sxs-lookup"><span data-stu-id="c42f5-131">Message store provider stores only the **PR_RTF_COMPRESSED** property, computing **PR_BODY** when necessary.</span></span>  <br/> |
|<span data-ttu-id="c42f5-132">High</span><span class="sxs-lookup"><span data-stu-id="c42f5-132">High</span></span>  <br/> |<span data-ttu-id="c42f5-133">消息存储提供程序存储区，既未**PR_BODY**或辅助 RTF 属性。</span><span class="sxs-lookup"><span data-stu-id="c42f5-133">Message store provider stores neither **PR_BODY** or the auxiliary RTF properties.</span></span> <span data-ttu-id="c42f5-134">**RTFSync**称为已更改消息文本和格式保持不变时或下载新邮件时由传输提供程序。</span><span class="sxs-lookup"><span data-stu-id="c42f5-134">**RTFSync** is called when the message text has changed and the formatting remains unchanged or when a new message is downloaded by a transport provider.</span></span>  <br/> |
   
