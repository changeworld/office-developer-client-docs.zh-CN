---
title: DefaultTabstop 单元格（“Text Block Format”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: 确定默认制表位在文本块中的间隔。
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780083"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="789b5-103">DefaultTabstop 单元格（“Text Block Format”内容）</span><span class="sxs-lookup"><span data-stu-id="789b5-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="789b5-104">确定默认制表位在文本块中的间隔。</span><span class="sxs-lookup"><span data-stu-id="789b5-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="789b5-105">注解</span><span class="sxs-lookup"><span data-stu-id="789b5-105">Remarks</span></span>

<span data-ttu-id="789b5-106">对于以英制单位创建的文档，默认值是 0.5 英寸；对于以公制单位创建的文档，默认值是 1.5 厘米。</span><span class="sxs-lookup"><span data-stu-id="789b5-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="789b5-107">要从另一个公式或使用**CellsU**属性从某个程序按名称获取对 DefaultTabstop 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="789b5-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="789b5-108">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="789b5-108">Cell name:</span></span>  <br/> |<span data-ttu-id="789b5-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="789b5-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="789b5-110">若要从某个程序按索引获取对 DefaultTabstop 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="789b5-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="789b5-111">内容索引：</span><span class="sxs-lookup"><span data-stu-id="789b5-111">Section index:</span></span>  <br/> |<span data-ttu-id="789b5-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="789b5-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="789b5-113">行索引：</span><span class="sxs-lookup"><span data-stu-id="789b5-113">Row index:</span></span>  <br/> |<span data-ttu-id="789b5-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="789b5-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="789b5-115">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="789b5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="789b5-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="789b5-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   
