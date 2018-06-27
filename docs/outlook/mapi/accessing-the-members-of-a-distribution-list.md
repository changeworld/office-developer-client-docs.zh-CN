---
title: 访问通讯组列表的成员
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19774504"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="cb69a-103">访问通讯组列表的成员</span><span class="sxs-lookup"><span data-stu-id="cb69a-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="cb69a-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="cb69a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="cb69a-105">**若要获取的通讯组列表成员**</span><span class="sxs-lookup"><span data-stu-id="cb69a-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="cb69a-106">创建具有您想要检索，如**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 和**PR_DISPLAY_TYPE** ([的成员属性的大小的属性标记数组PidTagDisplayType](pidtagdisplaytype-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="cb69a-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="cb69a-107">调用[IAddrBook::OpenEntry](iaddrbook-openentry.md)打开通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="cb69a-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="cb69a-108">调用该通讯组列表**IABContainer::GetContentsTable**方法，以访问其内容表。</span><span class="sxs-lookup"><span data-stu-id="cb69a-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="cb69a-109">调用[HrQueryAllRows](hrqueryallrows.md)检索所有表的行代表通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="cb69a-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    
