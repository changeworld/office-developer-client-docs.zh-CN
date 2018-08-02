---
title: 获取和设置多个属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775035"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="38b35-103">获取和设置多个属性</span><span class="sxs-lookup"><span data-stu-id="38b35-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="38b35-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="38b35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38b35-105">获取和设置尽可能使用最少的多个属性的呼叫，远程 curtailed 活动并减少了开销涉及与每个属性数。</span><span class="sxs-lookup"><span data-stu-id="38b35-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="38b35-106">尽管服务提供商尝试进行远程过程调用的检索或修改之前收集属性，您可以通过首先请求多个属性来优化这项成果。</span><span class="sxs-lookup"><span data-stu-id="38b35-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="38b35-107">例如，如果您使用路由描述将来收件人属于特定的属性集的命名属性的列表，可处理所有的收件人的两个通话。</span><span class="sxs-lookup"><span data-stu-id="38b35-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="38b35-108">一次调用[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)用于检索所有收件人的属性和其他调用[IMAPIProp::GetProps](imapiprop-getprops.md)以检索的所有值的标识符。</span><span class="sxs-lookup"><span data-stu-id="38b35-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="38b35-109">或者，对于每个收件人后, 跟**GetProps**调用**GetIDsFromNames**调用是效率显著降低。</span><span class="sxs-lookup"><span data-stu-id="38b35-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  
