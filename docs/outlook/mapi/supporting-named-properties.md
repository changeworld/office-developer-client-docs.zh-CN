---
title: 支持命名的属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778917"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="fae59-103">支持命名的属性</span><span class="sxs-lookup"><span data-stu-id="fae59-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="fae59-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="fae59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fae59-105">实现任何对象[IMAPIProp: IUnknown](imapipropiunknown.md)接口可支持命名的属性。</span><span class="sxs-lookup"><span data-stu-id="fae59-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="fae59-106">支持的命名属性是必需的：</span><span class="sxs-lookup"><span data-stu-id="fae59-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="fae59-107">通讯簿提供程序，以允许从其他提供程序复制到其容器的条目。</span><span class="sxs-lookup"><span data-stu-id="fae59-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="fae59-108">消息存储提供程序可用于创建任意消息类型。</span><span class="sxs-lookup"><span data-stu-id="fae59-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="fae59-109">对于所有其他服务提供程序是可选的命名的属性支持。</span><span class="sxs-lookup"><span data-stu-id="fae59-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="fae59-110">服务提供商支持的命名属性必须实现的[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)和[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)方法中的名称为标识符映射。</span><span class="sxs-lookup"><span data-stu-id="fae59-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="fae59-111">客户端呼叫**GetNamesFromIDs**检索转移 0x8000 范围中的一个或多个属性标识符的相应名称和**GetIDsFromNames**创建或检索一个或多个名称的标识符。</span><span class="sxs-lookup"><span data-stu-id="fae59-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="fae59-112">服务提供程序不支持的命名属性必须：</span><span class="sxs-lookup"><span data-stu-id="fae59-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="fae59-113">无法对[IMAPIProp::SetProps](imapiprop-setprops.md)调用，以通过[SPropProblem](spropproblem.md)数组中返回 MAPI_E_UNEXPECTED_ID 设置与标识符的 0x8000 或更高版本的属性。</span><span class="sxs-lookup"><span data-stu-id="fae59-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="fae59-114">从[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)和[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)方法的调用返回 MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="fae59-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    
