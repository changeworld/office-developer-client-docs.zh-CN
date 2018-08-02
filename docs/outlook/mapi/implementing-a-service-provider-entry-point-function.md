---
title: 实现服务提供程序入口点函数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775789"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="ad77f-103">实现服务提供程序入口点函数</span><span class="sxs-lookup"><span data-stu-id="ad77f-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="ad77f-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="ad77f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad77f-105">每个服务提供商 DLL 有入口点 MAPI 调用以将其加载的函数。</span><span class="sxs-lookup"><span data-stu-id="ad77f-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="ad77f-106">请注意此入口点函数不是[DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx)，Win32 DLL 入口点函数相同。</span><span class="sxs-lookup"><span data-stu-id="ad77f-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="ad77f-107">根据您的提供程序的类型，您的提供程序入口点函数符合不同原型。</span><span class="sxs-lookup"><span data-stu-id="ad77f-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="ad77f-108">MAPI 服务提供程序定义不同的入口点函数原型。</span><span class="sxs-lookup"><span data-stu-id="ad77f-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="ad77f-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="ad77f-109">**Provider**</span></span>|<span data-ttu-id="ad77f-110">**入口点函数原型**</span><span class="sxs-lookup"><span data-stu-id="ad77f-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad77f-111">消息存储提供程序</span><span class="sxs-lookup"><span data-stu-id="ad77f-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="ad77f-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="ad77f-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="ad77f-113">传输提供程序</span><span class="sxs-lookup"><span data-stu-id="ad77f-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="ad77f-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="ad77f-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="ad77f-115">通讯簿提供程序</span><span class="sxs-lookup"><span data-stu-id="ad77f-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="ad77f-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="ad77f-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="ad77f-117">大部分中这些原型是功能的相同的所有服务提供程序类型。</span><span class="sxs-lookup"><span data-stu-id="ad77f-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="ad77f-118">通讯簿、 消息存储和传输提供程序执行其入口点函数中的以下两个主要任务：</span><span class="sxs-lookup"><span data-stu-id="ad77f-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="ad77f-119">检查服务提供程序接口 (SPI) 以确保 MAPI 用版本与服务提供商使用的版本兼容的版本。</span><span class="sxs-lookup"><span data-stu-id="ad77f-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="ad77f-120">使用_lpulMAPIVer_参数，其中包含的 MAPI SPI 版本和_lpulProviderVer_参数，其中包含您 SPI 版本，以执行检查。</span><span class="sxs-lookup"><span data-stu-id="ad77f-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="ad77f-121">这些参数是 32 位无符号的整数三部分组成：</span><span class="sxs-lookup"><span data-stu-id="ad77f-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="ad77f-122">通过 31 的 24 位表示的主要版本。</span><span class="sxs-lookup"><span data-stu-id="ad77f-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="ad77f-123">通过 23 16 位表示的次要版本。</span><span class="sxs-lookup"><span data-stu-id="ad77f-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="ad77f-124">0 到 15 位表示更新标识符。</span><span class="sxs-lookup"><span data-stu-id="ad77f-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="ad77f-125">尽管很少更改的主版本号，次要版本号更改每当发布 MAPI 和 SPI 已更改。</span><span class="sxs-lookup"><span data-stu-id="ad77f-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="ad77f-126">更新标识符是 Microsoft 内部版本号它用于跟踪在开发过程中的更改。</span><span class="sxs-lookup"><span data-stu-id="ad77f-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="ad77f-127">MAPI 定义 CURRENT_SPI_VERSION 常量，记录在 Mapispi.h 标头文件，以指示存在 SPI 版本。</span><span class="sxs-lookup"><span data-stu-id="ad77f-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="ad77f-128">如果使用的版本比使用 MAPI 的版本更新 SPI，失败错误 MAPI_E_VERSION 您检查。</span><span class="sxs-lookup"><span data-stu-id="ad77f-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="ad77f-129">创建提供商对象的实例。</span><span class="sxs-lookup"><span data-stu-id="ad77f-129">Create an instance of a provider object.</span></span> <span data-ttu-id="ad77f-130">因为您的提供商可以启动和初始化多次，应发生这种情况每次创建的新实例。</span><span class="sxs-lookup"><span data-stu-id="ad77f-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="ad77f-131">提供程序已启动多次时显示在一个或多个客户端，同时使用中的多个配置文件或者多次出现一个配置文件中。</span><span class="sxs-lookup"><span data-stu-id="ad77f-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="ad77f-132">仅当入口点函数原型不同，具体取决于您的提供程序的类型，也提供商对象的类型。</span><span class="sxs-lookup"><span data-stu-id="ad77f-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="ad77f-133">如果您正在编写通讯簿提供程序，实现[IABProvider: IUnknown](iabprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="ad77f-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="ad77f-134">如果您正在编写消息存储提供程序，实现[IMSProvider: IUnknown](imsprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="ad77f-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="ad77f-135">有关详细信息，请参阅[加载消息存储提供程序](loading-message-store-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="ad77f-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="ad77f-136">如果您正在编写传输提供程序，实现[IXPProvider: IUnknown](ixpprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="ad77f-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="ad77f-137">有关详细信息，请参阅[初始化传输提供程序](initializing-the-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ad77f-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad77f-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ad77f-138">See also</span></span>



[<span data-ttu-id="ad77f-139">启动服务提供程序</span><span class="sxs-lookup"><span data-stu-id="ad77f-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)
