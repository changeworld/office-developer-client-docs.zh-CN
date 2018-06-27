---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779037"
---
# <a name="ulrelease"></a><span data-ttu-id="7f1fb-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="7f1fb-103">UlRelease</span></span>

  
  
<span data-ttu-id="7f1fb-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="7f1fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f1fb-105">提供一种方法来调用 OLE 方法**IUnknown::Release**。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f1fb-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="7f1fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f1fb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f1fb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7f1fb-108">通过实现：</span><span class="sxs-lookup"><span data-stu-id="7f1fb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f1fb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f1fb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7f1fb-110">调用：</span><span class="sxs-lookup"><span data-stu-id="7f1fb-110">Called by:</span></span>  <br/> |<span data-ttu-id="7f1fb-111">客户端应用程序和服务提供商</span><span class="sxs-lookup"><span data-stu-id="7f1fb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="7f1fb-112">参数</span><span class="sxs-lookup"><span data-stu-id="7f1fb-112">Parameters</span></span>

 <span data-ttu-id="7f1fb-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="7f1fb-113">_punk_</span></span>
  
> <span data-ttu-id="7f1fb-114">[in]从**IUnknown**接口，换句话说任何 MAPI 接口派生的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f1fb-115">返回值</span><span class="sxs-lookup"><span data-stu-id="7f1fb-115">Return value</span></span>

<span data-ttu-id="7f1fb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f1fb-116">S_OK</span></span> 
  
> <span data-ttu-id="7f1fb-117">呼叫成功或多个预期值返回。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7f1fb-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7f1fb-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7f1fb-119">意外或未知的原点出现错误，无法完成操作。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f1fb-120">备注</span><span class="sxs-lookup"><span data-stu-id="7f1fb-120">Remarks</span></span>

<span data-ttu-id="7f1fb-121">引用计数是现有指向必须释放的对象数。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="7f1fb-122">如果_punk_参数为 NULL，则函数返回立即而无需调用**IUnknown::Release**</span><span class="sxs-lookup"><span data-stu-id="7f1fb-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="7f1fb-123">**UlRelease**返回返回**IUnknown::Release**方法，该数据库可以等于必须释放的对象的引用计数的值。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="7f1fb-124">有关**IUnknown::Release**的详细信息，请参阅[实现 IUnknown 接口](implementing-the-iunknown-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="7f1fb-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  
