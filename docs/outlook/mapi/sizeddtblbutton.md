---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778782"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="787bc-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="787bc-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="787bc-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="787bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="787bc-105">创建一个名为的结构包含用于描述一个按钮和一个指定长度的标签[DTBLBUTTON](dtblbutton.md)结构。</span><span class="sxs-lookup"><span data-stu-id="787bc-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="787bc-106">头文件：</span><span class="sxs-lookup"><span data-stu-id="787bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="787bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="787bc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="787bc-108">相关的结构：</span><span class="sxs-lookup"><span data-stu-id="787bc-108">Related structure:</span></span>  <br/> |<span data-ttu-id="787bc-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="787bc-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="787bc-110">参数</span><span class="sxs-lookup"><span data-stu-id="787bc-110">Parameters</span></span>

 <span data-ttu-id="787bc-111">_n_</span><span class="sxs-lookup"><span data-stu-id="787bc-111">_n_</span></span>
  
> <span data-ttu-id="787bc-112">标签的新结构中包含的长度。</span><span class="sxs-lookup"><span data-stu-id="787bc-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="787bc-113">_u_</span><span class="sxs-lookup"><span data-stu-id="787bc-113">_u_</span></span>
  
> <span data-ttu-id="787bc-114">新结构的的名称。</span><span class="sxs-lookup"><span data-stu-id="787bc-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="787bc-115">备注</span><span class="sxs-lookup"><span data-stu-id="787bc-115">Remarks</span></span>

<span data-ttu-id="787bc-116">使用下列成员来创建新的结构：</span><span class="sxs-lookup"><span data-stu-id="787bc-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="787bc-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="787bc-117">See also</span></span>



[<span data-ttu-id="787bc-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="787bc-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="787bc-119">与结构相关的宏</span><span class="sxs-lookup"><span data-stu-id="787bc-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)
