---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 上次修改时间： 2012 年 2 月 20 日
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776511"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="e6b08-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="e6b08-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="e6b08-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="e6b08-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6b08-105">比较两个 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="e6b08-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="e6b08-106">参数</span><span class="sxs-lookup"><span data-stu-id="e6b08-106">Parameters</span></span>

 <span data-ttu-id="e6b08-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="e6b08-107">_lcid_</span></span>
  
> <span data-ttu-id="e6b08-108">[in]区域设置标识符。</span><span class="sxs-lookup"><span data-stu-id="e6b08-108">[in] Locale identifier.</span></span> <span data-ttu-id="e6b08-109">有关详细的定义，请参阅_Locale_参数的[CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e6b08-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="e6b08-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e6b08-110">_dwFlags_</span></span>
  
> <span data-ttu-id="e6b08-111">[in]要忽略大小写和音调符号的标志。</span><span class="sxs-lookup"><span data-stu-id="e6b08-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="e6b08-112">有关详细的定义，请参阅[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)的_dwCmpFlags_参数。</span><span class="sxs-lookup"><span data-stu-id="e6b08-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="e6b08-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="e6b08-113">_pstr1_</span></span>
  
> <span data-ttu-id="e6b08-114">[in]指向要比较的第一个 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="e6b08-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="e6b08-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="e6b08-115">_cch1_</span></span>
  
> <span data-ttu-id="e6b08-116">[in]以字符数计不包括 null 终止符的第一个 Unicode 字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="e6b08-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="e6b08-117">如果 string 是 null 结尾，应用程序可以提供一个负值。</span><span class="sxs-lookup"><span data-stu-id="e6b08-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="e6b08-118">在这种情况下， **MNLS_CompareStringW**函数将自动确定长度。</span><span class="sxs-lookup"><span data-stu-id="e6b08-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="e6b08-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="e6b08-119">_pstr2_</span></span>
  
> <span data-ttu-id="e6b08-120">[in]指向要比较的第二个 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="e6b08-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="e6b08-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="e6b08-121">_cch2_</span></span>
  
> <span data-ttu-id="e6b08-122">[in]在不包括 null 终止符的第二个 Unicode 字符串的字符的长度。</span><span class="sxs-lookup"><span data-stu-id="e6b08-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="e6b08-123">如果 string 是 null 结尾，应用程序可以提供一个负值。</span><span class="sxs-lookup"><span data-stu-id="e6b08-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="e6b08-124">在这种情况下，该函数将自动确定长度。</span><span class="sxs-lookup"><span data-stu-id="e6b08-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6b08-125">返回值</span><span class="sxs-lookup"><span data-stu-id="e6b08-125">Return value</span></span>

<span data-ttu-id="e6b08-126">返回 for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)所述的值。</span><span class="sxs-lookup"><span data-stu-id="e6b08-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6b08-127">说明</span><span class="sxs-lookup"><span data-stu-id="e6b08-127">Remarks</span></span>

<span data-ttu-id="e6b08-128">此函数的换行[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e6b08-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="e6b08-129">**MNLS_CompareStringW**采用相同参数具有[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)相同的行为。</span><span class="sxs-lookup"><span data-stu-id="e6b08-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6b08-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6b08-130">See also</span></span>



[<span data-ttu-id="e6b08-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="e6b08-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="e6b08-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="e6b08-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)
