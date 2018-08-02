---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779069"
---
# <a name="uptble"></a><span data-ttu-id="4bae9-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="4bae9-103">UPTBLE</span></span>

<span data-ttu-id="4bae9-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="4bae9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4bae9-105">扩展的[上载表状态](upload-table-state.md)期间上载文件夹的内容的信息。</span><span class="sxs-lookup"><span data-stu-id="4bae9-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4bae9-106">快速信息</span><span class="sxs-lookup"><span data-stu-id="4bae9-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="4bae9-107">Members</span><span class="sxs-lookup"><span data-stu-id="4bae9-107">Members</span></span>

 <span data-ttu-id="4bae9-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="4bae9-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="4bae9-109">[输出]要跟踪上载新的或修改项的_cEntMod_数目的索引。</span><span class="sxs-lookup"><span data-stu-id="4bae9-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="4bae9-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="4bae9-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="4bae9-111">[输出]新的或修改的文件夹中的项目数。</span><span class="sxs-lookup"><span data-stu-id="4bae9-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="4bae9-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="4bae9-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="4bae9-113">[输出]索引来跟踪上载_cEntRead_读取的项目数。</span><span class="sxs-lookup"><span data-stu-id="4bae9-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="4bae9-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="4bae9-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="4bae9-115">[输出]读取的文件夹中的项目数。</span><span class="sxs-lookup"><span data-stu-id="4bae9-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="4bae9-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="4bae9-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="4bae9-117">[输出]删除项目的索引来跟踪上载_cEntDel_数。</span><span class="sxs-lookup"><span data-stu-id="4bae9-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="4bae9-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="4bae9-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="4bae9-119">[输出]已删除的文件夹中的项目数。</span><span class="sxs-lookup"><span data-stu-id="4bae9-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4bae9-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4bae9-120">See also</span></span>

- [<span data-ttu-id="4bae9-121">关于复制 API</span><span class="sxs-lookup"><span data-stu-id="4bae9-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="4bae9-122">关于复制状态计算机</span><span class="sxs-lookup"><span data-stu-id="4bae9-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4bae9-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="4bae9-123">UPTBL</span></span>](uptbl.md)
