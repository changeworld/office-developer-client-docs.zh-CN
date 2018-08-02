---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775481"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="d3e24-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d3e24-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="d3e24-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="d3e24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3e24-105">获取为其脱机对象支持回调的条件。</span><span class="sxs-lookup"><span data-stu-id="d3e24-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="d3e24-106">参数</span><span class="sxs-lookup"><span data-stu-id="d3e24-106">Parameters</span></span>

 <span data-ttu-id="d3e24-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="d3e24-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="d3e24-108">[输出]以下功能标志位掩码：</span><span class="sxs-lookup"><span data-stu-id="d3e24-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="d3e24-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d3e24-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="d3e24-110">脱机对象是能够提供脱机通知。</span><span class="sxs-lookup"><span data-stu-id="d3e24-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="d3e24-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d3e24-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="d3e24-112">脱机对象是能够提供联机通知。</span><span class="sxs-lookup"><span data-stu-id="d3e24-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3e24-113">说明</span><span class="sxs-lookup"><span data-stu-id="d3e24-113">Remarks</span></span>

<span data-ttu-id="d3e24-114">在打开时使用**[HrOpenOfflineObj](hropenofflineobj.md)** 脱机对象，客户端可以查询[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)获取指向**IMAPIOffline**接口，并调用**IMAPIOffline::GetCapabilities**以找出回调支持由对象。</span><span class="sxs-lookup"><span data-stu-id="d3e24-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="d3e24-115">客户端然后可以选择使用**IMAPIOfflineMgr**设置回调。</span><span class="sxs-lookup"><span data-stu-id="d3e24-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="d3e24-116">请注意，具体取决于脱机对象的邮件服务器，用于联机支持回调的对象不一定支持回调的脱机。</span><span class="sxs-lookup"><span data-stu-id="d3e24-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="d3e24-117">此外，并脱机对象可能更改之外联机/脱机支持回调，脱机状态 API 支持仅联机/脱机更改，这样的功能必须检查客户端。</span><span class="sxs-lookup"><span data-stu-id="d3e24-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3e24-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d3e24-118">See also</span></span>



[<span data-ttu-id="d3e24-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d3e24-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="d3e24-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d3e24-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="d3e24-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="d3e24-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="d3e24-122">MAPI 常量</span><span class="sxs-lookup"><span data-stu-id="d3e24-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d3e24-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="d3e24-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)
