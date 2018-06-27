---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778893"
---
# <a name="stnefproblem"></a><span data-ttu-id="6707d-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="6707d-103">STnefProblem</span></span>

  
  
<span data-ttu-id="6707d-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="6707d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6707d-105">包含有关编码或解码传输中性封装格式 (TNEF) 流的过程中发生的属性或特性的处理问题的信息。</span><span class="sxs-lookup"><span data-stu-id="6707d-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6707d-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="6707d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6707d-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="6707d-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="6707d-108">成员</span><span class="sxs-lookup"><span data-stu-id="6707d-108">Members</span></span>

 <span data-ttu-id="6707d-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="6707d-109">**ulComponent**</span></span>
  
> <span data-ttu-id="6707d-110">处理出现此问题的类型。</span><span class="sxs-lookup"><span data-stu-id="6707d-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="6707d-111">如果在消息处理过程中出现此问题， **ulComponent**成员设置为零。</span><span class="sxs-lookup"><span data-stu-id="6707d-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="6707d-112">如果附件处理期间出现此问题， **ulComponent**设置等于相应的附件的**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 值。</span><span class="sxs-lookup"><span data-stu-id="6707d-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="6707d-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="6707d-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="6707d-114">与属性关联的属性指示由**ulPropTag**成员中，或者 TNEF 处理问题出现时，当解码封装阻止，下列值之一：</span><span class="sxs-lookup"><span data-stu-id="6707d-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="6707d-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="6707d-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="6707d-116">消息级别</span><span class="sxs-lookup"><span data-stu-id="6707d-116">Message level</span></span>
    
 <span data-ttu-id="6707d-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="6707d-117">_attAttachment_</span></span>
  
> <span data-ttu-id="6707d-118">附件级别</span><span class="sxs-lookup"><span data-stu-id="6707d-118">Attachment level</span></span>
    
 <span data-ttu-id="6707d-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="6707d-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="6707d-120">属性标记的问题的原因 TNEF 处理，除时解码封装块中，设置为零的案例**ulPropTag**时出现问题的属性。</span><span class="sxs-lookup"><span data-stu-id="6707d-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="6707d-121">**scode**</span><span class="sxs-lookup"><span data-stu-id="6707d-121">**scode**</span></span>
  
> <span data-ttu-id="6707d-122">错误值，该值指示处理过程中遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="6707d-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6707d-123">备注</span><span class="sxs-lookup"><span data-stu-id="6707d-123">Remarks</span></span>

<span data-ttu-id="6707d-124">如果属性或属性的处理过程中未生成**STnefProblem**结构，应用程序可以继续处理属性或属性的成功假定下。</span><span class="sxs-lookup"><span data-stu-id="6707d-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="6707d-125">解码封装块的过程中出现问题时，发生此事件唯一的例外。</span><span class="sxs-lookup"><span data-stu-id="6707d-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="6707d-126">在这种情况下，解码阻止到相应的组件已停止，解码继续使用在另一个组件。</span><span class="sxs-lookup"><span data-stu-id="6707d-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6707d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6707d-127">See also</span></span>



[<span data-ttu-id="6707d-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="6707d-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="6707d-129">PidTagAttachNumber 规范属性</span><span class="sxs-lookup"><span data-stu-id="6707d-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="6707d-130">MAPI 结构</span><span class="sxs-lookup"><span data-stu-id="6707d-130">MAPI Structures</span></span>](mapi-structures.md)
