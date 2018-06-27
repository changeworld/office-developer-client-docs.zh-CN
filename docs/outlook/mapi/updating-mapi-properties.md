---
title: 更新 MAPI 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779031"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="72927-103">更新 MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="72927-103">Updating MAPI properties</span></span>

<span data-ttu-id="72927-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="72927-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72927-105">客户端和服务提供商可以通过调用更新的属性值：</span><span class="sxs-lookup"><span data-stu-id="72927-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="72927-106">若要更新的一个或多个对象的属性值的对象的[IMAPIProp::SetProps](imapiprop-setprops.md)方法。</span><span class="sxs-lookup"><span data-stu-id="72927-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="72927-107">用于更新一次只有一个属性的[HrSetOneProp](hrsetoneprop.md)函数。</span><span class="sxs-lookup"><span data-stu-id="72927-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="72927-108">仅在本地; 目标对象是否使用**HrSetOneProp**此函数可能会导致与远程对象一起使用时的性能下降。</span><span class="sxs-lookup"><span data-stu-id="72927-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="72927-109">下面的过程说明如何使用**SetProps**更新的邮件类或 PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 属性，一条消息。</span><span class="sxs-lookup"><span data-stu-id="72927-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="72927-110">若要更新的邮件的邮件类</span><span class="sxs-lookup"><span data-stu-id="72927-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="72927-111">为邮件类分配[SPropValue](spropvalue.md)结构，并根据需要设置及其成员。</span><span class="sxs-lookup"><span data-stu-id="72927-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="72927-112">调用消息的**IMAPIProp::SetProps**方法，以设置新的邮件类。</span><span class="sxs-lookup"><span data-stu-id="72927-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="72927-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="72927-113">See also</span></span>

- [<span data-ttu-id="72927-114">MAPI 属性概述</span><span class="sxs-lookup"><span data-stu-id="72927-114">MAPI Property Overview</span></span>](mapi-property-overview.md)
