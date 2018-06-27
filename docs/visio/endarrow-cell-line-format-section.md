---
title: EndArrow 单元格（“Line Format”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: 指出线条末端是箭头还是其他线端格式。
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780176"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="703b9-103">EndArrow 单元格（“Line Format”内容）</span><span class="sxs-lookup"><span data-stu-id="703b9-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="703b9-104">指出线条末端是箭头还是其他线端格式。</span><span class="sxs-lookup"><span data-stu-id="703b9-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="703b9-105">**值**</span><span class="sxs-lookup"><span data-stu-id="703b9-105">**Value**</span></span>|<span data-ttu-id="703b9-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="703b9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="703b9-107">0</span><span class="sxs-lookup"><span data-stu-id="703b9-107">0</span></span>  <br/> |<span data-ttu-id="703b9-108">无箭头。</span><span class="sxs-lookup"><span data-stu-id="703b9-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="703b9-109">1-45</span><span class="sxs-lookup"><span data-stu-id="703b9-109">1 - 45</span></span>  <br/> |<span data-ttu-id="703b9-110">与**线条**对话框中的索引项相对应的各种类型的箭头样式。</span><span class="sxs-lookup"><span data-stu-id="703b9-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="703b9-111">备注</span><span class="sxs-lookup"><span data-stu-id="703b9-111">Remarks</span></span>

<span data-ttu-id="703b9-112">您还可以在**线条**对话框来设置此值 （**主页**选项卡，在**形状**组中，单击**线条**，指向**箭头**，然后单击**其他箭头**）。</span><span class="sxs-lookup"><span data-stu-id="703b9-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="703b9-113">EndArrowSize 单元格中设置箭头的大小。</span><span class="sxs-lookup"><span data-stu-id="703b9-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="703b9-114">您可以使用 USE 函数在此单元格中指定自定义线端。</span><span class="sxs-lookup"><span data-stu-id="703b9-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="703b9-115">要从另一个公式或使用**CellsU**属性从某个程序按名称获取对 EndArrow 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="703b9-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="703b9-116">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="703b9-116">Cell name:</span></span>  <br/> |<span data-ttu-id="703b9-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="703b9-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="703b9-118">若要从某个程序按索引获取对 EndArrow 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="703b9-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="703b9-119">内容索引：</span><span class="sxs-lookup"><span data-stu-id="703b9-119">Section index:</span></span>  <br/> |<span data-ttu-id="703b9-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="703b9-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="703b9-121">行索引：</span><span class="sxs-lookup"><span data-stu-id="703b9-121">Row index:</span></span>  <br/> |<span data-ttu-id="703b9-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="703b9-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="703b9-123">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="703b9-123">Cell index:</span></span>  <br/> |<span data-ttu-id="703b9-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="703b9-124">**visLineEndArrow**</span></span> <br/> |
   
