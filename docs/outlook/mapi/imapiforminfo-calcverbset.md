---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775409"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="790e0-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="790e0-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="790e0-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="790e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="790e0-105">到谓词窗体所使用的完整集合中返回的指针。</span><span class="sxs-lookup"><span data-stu-id="790e0-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="790e0-106">参数</span><span class="sxs-lookup"><span data-stu-id="790e0-106">Parameters</span></span>

 <span data-ttu-id="790e0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="790e0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="790e0-108">[in]返回控制的字符串类型的标志位掩码。</span><span class="sxs-lookup"><span data-stu-id="790e0-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="790e0-109">可以设置以下标记：</span><span class="sxs-lookup"><span data-stu-id="790e0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="790e0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="790e0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="790e0-111">返回的字符串采用 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="790e0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="790e0-112">如果未设置 MAPI_UNICODE 标志的字符串是以 ANSI 格式。</span><span class="sxs-lookup"><span data-stu-id="790e0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="790e0-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="790e0-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="790e0-114">[输出]指向包含窗体的谓词返回[SMAPIVerbArray](smapiverbarray.md)结构的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="790e0-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="790e0-115">返回值</span><span class="sxs-lookup"><span data-stu-id="790e0-115">Return value</span></span>

<span data-ttu-id="790e0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="790e0-116">S_OK</span></span> 
  
> <span data-ttu-id="790e0-117">呼叫成功或多个预期值返回。</span><span class="sxs-lookup"><span data-stu-id="790e0-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="790e0-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="790e0-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="790e0-119">既设置了 MAPI_UNICODE 标志实现不支持 Unicode，或未设置 MAPI_UNICODE 并实现支持仅 Unicode。</span><span class="sxs-lookup"><span data-stu-id="790e0-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="790e0-120">说明</span><span class="sxs-lookup"><span data-stu-id="790e0-120">Remarks</span></span>

<span data-ttu-id="790e0-121">客户端应用程序调用**IMAPIFormInfo::CalcVerbSet**方法以获取指向由窗体的动作设置。</span><span class="sxs-lookup"><span data-stu-id="790e0-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="790e0-122">在**SMAPIVerbArray**结构中返回_ppMAPIVerbArray_参数中，返回动词顺序的索引号;每个动作索引是其**lVerb**成员中找到的。</span><span class="sxs-lookup"><span data-stu-id="790e0-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="790e0-123">客户端应用程序可以使用动词数组动态生成菜单、 隐藏或显示按钮，等等。</span><span class="sxs-lookup"><span data-stu-id="790e0-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="790e0-124">MFCMAPI 参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="790e0-124">MFCMAPI reference</span></span>

<span data-ttu-id="790e0-125">MFCMAPI 示例代码，请参阅下表。</span><span class="sxs-lookup"><span data-stu-id="790e0-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="790e0-126">**文件**</span><span class="sxs-lookup"><span data-stu-id="790e0-126">**File**</span></span>|<span data-ttu-id="790e0-127">**函数**</span><span class="sxs-lookup"><span data-stu-id="790e0-127">**Function**</span></span>|<span data-ttu-id="790e0-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="790e0-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="790e0-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="790e0-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="790e0-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="790e0-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="790e0-131">MFCMAPI 编写窗体信息对象的调试输出时使用**IMAPIFormInfo::CalcVerbSet**方法。</span><span class="sxs-lookup"><span data-stu-id="790e0-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="790e0-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="790e0-132">See also</span></span>



[<span data-ttu-id="790e0-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="790e0-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="790e0-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="790e0-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="790e0-135">MFCMAPI 代码示例</span><span class="sxs-lookup"><span data-stu-id="790e0-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
