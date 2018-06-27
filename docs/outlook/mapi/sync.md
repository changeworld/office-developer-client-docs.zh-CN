---
title: 同步
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778936"
---
# <a name="sync"></a><span data-ttu-id="094b2-103">同步</span><span class="sxs-lookup"><span data-stu-id="094b2-103">SYNC</span></span>

  
  
<span data-ttu-id="094b2-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="094b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="094b2-105">用于启动本地存储和服务器之间同步的信息。</span><span class="sxs-lookup"><span data-stu-id="094b2-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="094b2-106">[同步状态](synchronize-state.md)期间使用此信息。</span><span class="sxs-lookup"><span data-stu-id="094b2-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="094b2-107">快速信息</span><span class="sxs-lookup"><span data-stu-id="094b2-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="094b2-108">成员</span><span class="sxs-lookup"><span data-stu-id="094b2-108">Members</span></span>

 <span data-ttu-id="094b2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="094b2-109">_ulFlags_</span></span>
  
- <span data-ttu-id="094b2-110">[out] / [in] 同步过程中修改的行为的以下标志位掩码：</span><span class="sxs-lookup"><span data-stu-id="094b2-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="094b2-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="094b2-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="094b2-112">[in]将仅上载执行客户端。</span><span class="sxs-lookup"><span data-stu-id="094b2-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="094b2-113">Outlook 仅返回本地修改的文件夹。</span><span class="sxs-lookup"><span data-stu-id="094b2-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="094b2-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="094b2-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="094b2-115">[in]将仅下载执行客户端。</span><span class="sxs-lookup"><span data-stu-id="094b2-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="094b2-116">Outlook 不应清除上载二进制文件的文件夹。</span><span class="sxs-lookup"><span data-stu-id="094b2-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="094b2-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="094b2-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="094b2-118">[in]客户端将与提供的条目 Id 同步一组指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="094b2-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="094b2-119">可以使用**UPS_UPLOAD_ONLY**或**UPS_DNLOAD_ONLY**标志组合此标志。</span><span class="sxs-lookup"><span data-stu-id="094b2-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="094b2-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="094b2-120">UPS_OK</span></span>
    
  - <span data-ttu-id="094b2-121">[输出]同步已成功。</span><span class="sxs-lookup"><span data-stu-id="094b2-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="094b2-122">客户端上载之后设置此或完全同步完成。</span><span class="sxs-lookup"><span data-stu-id="094b2-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="094b2-123">即使客户端可以上载或完全同步 （上载然后下载） 文件夹和项目复制 API，客户端使用的复制每次只有一个方向指定*ulFlags* — 任一**UPS_UPLOAD_ONLY**或**UPS_DNLOAD_ONLY**标志。</span><span class="sxs-lookup"><span data-stu-id="094b2-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="094b2-124">对于完全同步，客户首先进行上载与**UPS_UPLOAD_ONLY**标志，然后用**UPS_DNLOAD_ONLY**标志下载。</span><span class="sxs-lookup"><span data-stu-id="094b2-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="094b2-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="094b2-125">_pwzPath_</span></span>
  
- <span data-ttu-id="094b2-126">[输出]本地存储路径。</span><span class="sxs-lookup"><span data-stu-id="094b2-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="094b2-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="094b2-127">_Reserved1_</span></span>
  
- <span data-ttu-id="094b2-128">此成员仅供内部使用的 Outlook，不支持。</span><span class="sxs-lookup"><span data-stu-id="094b2-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="094b2-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="094b2-129">_Reserved2_</span></span>
  
- <span data-ttu-id="094b2-130">此成员仅供内部使用的 Outlook，不支持。</span><span class="sxs-lookup"><span data-stu-id="094b2-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="094b2-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="094b2-131">*pel*</span></span> 
  
- <span data-ttu-id="094b2-132">[in]这是要同步如果**UPS_THESE_FOLDERS**已设置的文件夹的条目 Id 的列表。</span><span class="sxs-lookup"><span data-stu-id="094b2-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="094b2-133">请参阅 mapidefs.h **LPENTRYLIST**的类型定义。</span><span class="sxs-lookup"><span data-stu-id="094b2-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="094b2-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="094b2-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="094b2-135">[in]如果设置了**UPS_THESE_FOLDERS** ，这是一个数组中*pel*对应的文件夹的文件夹选项。</span><span class="sxs-lookup"><span data-stu-id="094b2-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="094b2-136">上载每个[上载文件夹状态](upload-folder-state.md)期间*pel*中列出的文件夹时，将使用这些文件夹选项。</span><span class="sxs-lookup"><span data-stu-id="094b2-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="094b2-137">有关文件夹选项的详细信息，请参阅**[UPFLD](upfld.md)**。</span><span class="sxs-lookup"><span data-stu-id="094b2-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="094b2-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="094b2-138">See also</span></span>



[<span data-ttu-id="094b2-139">有关复制 API</span><span class="sxs-lookup"><span data-stu-id="094b2-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="094b2-140">有关的复制状态机</span><span class="sxs-lookup"><span data-stu-id="094b2-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="094b2-141">MAPI 常量</span><span class="sxs-lookup"><span data-stu-id="094b2-141">MAPI Constants</span></span>](mapi-constants.md)
