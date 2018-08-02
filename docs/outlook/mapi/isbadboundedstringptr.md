---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776071"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="58f60-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="58f60-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="58f60-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="58f60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58f60-105">验证调用进程具有读取访问权限指定范围的内存。</span><span class="sxs-lookup"><span data-stu-id="58f60-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58f60-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="58f60-106">Header file:</span></span>  <br/> |<span data-ttu-id="58f60-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="58f60-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="58f60-108">通过实现：</span><span class="sxs-lookup"><span data-stu-id="58f60-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="58f60-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="58f60-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="58f60-110">调用：</span><span class="sxs-lookup"><span data-stu-id="58f60-110">Called by:</span></span>  <br/> |<span data-ttu-id="58f60-111">客户端应用程序和服务提供商。</span><span class="sxs-lookup"><span data-stu-id="58f60-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="58f60-112">参数</span><span class="sxs-lookup"><span data-stu-id="58f60-112">Parameters</span></span>

 <span data-ttu-id="58f60-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="58f60-113">_lpsz_</span></span>
  
> <span data-ttu-id="58f60-114">[in]以 null 结尾的 ASCII 字符串的指针。</span><span class="sxs-lookup"><span data-stu-id="58f60-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="58f60-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="58f60-115">_cchMax_</span></span>
  
> <span data-ttu-id="58f60-116">[in]字符串，以字符为单位的最大大小。</span><span class="sxs-lookup"><span data-stu-id="58f60-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="58f60-117">该函数检查的字符串的 null 终止符之前的所有字符中的读取访问或最多为此参数所指定的字符数，两者中较小。</span><span class="sxs-lookup"><span data-stu-id="58f60-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="58f60-118">如果此参数为零，则返回的值为零。</span><span class="sxs-lookup"><span data-stu-id="58f60-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58f60-119">返回值</span><span class="sxs-lookup"><span data-stu-id="58f60-119">Return value</span></span>

<span data-ttu-id="58f60-120">调用进程具有读取访问权限之前字符串的 null 终止符的所有字符或最_cchMax_由指定的字符数多的读取访问权限时，返回值为零。</span><span class="sxs-lookup"><span data-stu-id="58f60-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="58f60-121">调用进程不具有对所有字符，最多为字符串的 null 终止符的读取权限或最_cchMax_由指定的字符数多的读取访问权限时，返回的值将为非零。</span><span class="sxs-lookup"><span data-stu-id="58f60-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58f60-122">说明</span><span class="sxs-lookup"><span data-stu-id="58f60-122">Remarks</span></span>

<span data-ttu-id="58f60-123">**IsBadBoundedStringPtr**函数等效于使用**IsBadStringPtr**。</span><span class="sxs-lookup"><span data-stu-id="58f60-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58f60-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58f60-124">See also</span></span>



[<span data-ttu-id="58f60-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="58f60-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)
