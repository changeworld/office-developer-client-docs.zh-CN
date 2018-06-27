---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778733"
---
# <a name="screlocprops"></a><span data-ttu-id="68751-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="68751-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="68751-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="68751-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68751-105">数组和其数据被复制或移动到新位置后，请调整[SPropValue](spropvalue.md)数组中的指针。</span><span class="sxs-lookup"><span data-stu-id="68751-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68751-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="68751-106">Header file:</span></span>  <br/> |<span data-ttu-id="68751-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68751-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="68751-108">通过实现：</span><span class="sxs-lookup"><span data-stu-id="68751-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="68751-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="68751-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="68751-110">调用：</span><span class="sxs-lookup"><span data-stu-id="68751-110">Called by:</span></span>  <br/> |<span data-ttu-id="68751-111">客户端应用程序和服务提供商</span><span class="sxs-lookup"><span data-stu-id="68751-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="68751-112">参数</span><span class="sxs-lookup"><span data-stu-id="68751-112">Parameters</span></span>

 <span data-ttu-id="68751-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="68751-113">_cprop_</span></span>
  
> <span data-ttu-id="68751-114">[in]Count 属性数组中的指向_rgprop_参数。</span><span class="sxs-lookup"><span data-stu-id="68751-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="68751-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="68751-115">_rgprop_</span></span>
  
> <span data-ttu-id="68751-116">[in]为数组[SPropValue](spropvalue.md)结构要调整指针的指针。</span><span class="sxs-lookup"><span data-stu-id="68751-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="68751-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="68751-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="68751-118">[in]指向原始基址数组_rgprop_参数指向的指针。</span><span class="sxs-lookup"><span data-stu-id="68751-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="68751-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="68751-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="68751-120">[in]指向新的基址数组_rgprop_参数指向的指针。</span><span class="sxs-lookup"><span data-stu-id="68751-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="68751-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="68751-121">_pcb_</span></span>
  
> <span data-ttu-id="68751-122">[传入、 传出]可选指向的大小，以字节为单位指示_pvBaseNew_参数的数组。</span><span class="sxs-lookup"><span data-stu-id="68751-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="68751-123">如果不为 NULL， _pcb_参数设置为_pvD_参数中存储的字节数。</span><span class="sxs-lookup"><span data-stu-id="68751-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68751-124">返回值</span><span class="sxs-lookup"><span data-stu-id="68751-124">Return value</span></span>

<span data-ttu-id="68751-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="68751-125">S_OK</span></span>
  
> <span data-ttu-id="68751-126">已成功调整指针。</span><span class="sxs-lookup"><span data-stu-id="68751-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="68751-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="68751-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="68751-128">一个或两个参数无效，或遇到未知的属性类型。</span><span class="sxs-lookup"><span data-stu-id="68751-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68751-129">备注</span><span class="sxs-lookup"><span data-stu-id="68751-129">Remarks</span></span>

<span data-ttu-id="68751-130">**ScRelocProps**函数以为，属性值数组指针进行调整为其最初分配的类似于对**ScCopyProps**函数的调用一次调用的操作。</span><span class="sxs-lookup"><span data-stu-id="68751-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="68751-131">如果客户端应用程序或服务提供商使用的内存脱节块建立的属性值，它应使用[ScCopyProps](sccopyprops.md)改为复制属性。</span><span class="sxs-lookup"><span data-stu-id="68751-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="68751-132">**ScRelocProps**用于维护[SPropValue](spropvalue.md)数组中的指针的有效性。</span><span class="sxs-lookup"><span data-stu-id="68751-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="68751-133">若要写入到此类数组和从磁盘中读取时维护指针的有效性，执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="68751-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="68751-134">数组和数据写入磁盘之前, 调用**ScRelocProps**阵列上与指向某些标准的值为零，例如_pvBaseNew_参数。</span><span class="sxs-lookup"><span data-stu-id="68751-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="68751-135">从磁盘读取的数组和数据之后, 调用**ScRelocProps** _pvBaseOld_参数数组等于标准值在步骤 1 中使用的相同。</span><span class="sxs-lookup"><span data-stu-id="68751-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="68751-136">数组和数据必须读入创建一个分配缓冲区。</span><span class="sxs-lookup"><span data-stu-id="68751-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="68751-137">**ScRelocProps** _pcb_参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="68751-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="68751-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="68751-138">See also</span></span>



[<span data-ttu-id="68751-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="68751-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="68751-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="68751-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="68751-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="68751-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="68751-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="68751-142">ScRelocNotifications</span></span>](screlocnotifications.md)
