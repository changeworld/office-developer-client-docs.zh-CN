---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778553"
---
# <a name="proptype"></a><span data-ttu-id="2c7f4-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="2c7f4-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="2c7f4-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="2c7f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c7f4-105">返回指定的属性标记的属性类型。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c7f4-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="2c7f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="2c7f4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c7f4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2c7f4-108">相关的结构：</span><span class="sxs-lookup"><span data-stu-id="2c7f4-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="2c7f4-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2c7f4-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="2c7f4-110">参数</span><span class="sxs-lookup"><span data-stu-id="2c7f4-110">Parameters</span></span>

 <span data-ttu-id="2c7f4-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2c7f4-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="2c7f4-112">包含要返回的属性类型的属性标记。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c7f4-113">备注</span><span class="sxs-lookup"><span data-stu-id="2c7f4-113">Remarks</span></span>

<span data-ttu-id="2c7f4-114">**PROP_TYPE**宏可以用于确定属性的类型。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="2c7f4-115">例如，调用 PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) 结果中 PT_BINARY 要返回的值。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="2c7f4-116">每个属性标记包含低序位 word （0 到 15 位） 中的属性类型和高顺序单词 （通过 31 16 位） 中的属性标识符。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="2c7f4-117">**PROP_TYPE**宏提取的属性类型，并将其放入位 0 到 15 的整数要返回。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="2c7f4-118">返回值的剩余的位设置为零。</span><span class="sxs-lookup"><span data-stu-id="2c7f4-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c7f4-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c7f4-119">See also</span></span>



[<span data-ttu-id="2c7f4-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2c7f4-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2c7f4-121">与结构相关的宏</span><span class="sxs-lookup"><span data-stu-id="2c7f4-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)
