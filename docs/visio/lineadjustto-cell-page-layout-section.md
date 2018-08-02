---
title: LineAdjustTo 单元格（“Page Layout”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: 确定哪些动态连接线要彼此重叠。
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780570"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="b02c2-103">LineAdjustTo 单元格（“Page Layout”部分）</span><span class="sxs-lookup"><span data-stu-id="b02c2-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="b02c2-104">确定哪些动态连接线要彼此重叠。</span><span class="sxs-lookup"><span data-stu-id="b02c2-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="b02c2-105">**值**</span><span class="sxs-lookup"><span data-stu-id="b02c2-105">**Value**</span></span>|<span data-ttu-id="b02c2-106">**调整**</span><span class="sxs-lookup"><span data-stu-id="b02c2-106">**Adjustment**</span></span>|<span data-ttu-id="b02c2-107">**自动常量**</span><span class="sxs-lookup"><span data-stu-id="b02c2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b02c2-108">0</span><span class="sxs-lookup"><span data-stu-id="b02c2-108">0</span></span>  <br/> |<span data-ttu-id="b02c2-109">默认的排列样式</span><span class="sxs-lookup"><span data-stu-id="b02c2-109">Routing style default</span></span>  <br/> |<span data-ttu-id="b02c2-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="b02c2-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="b02c2-111">1</span><span class="sxs-lookup"><span data-stu-id="b02c2-111">1</span></span>  <br/> |<span data-ttu-id="b02c2-112">彼此紧邻的线条</span><span class="sxs-lookup"><span data-stu-id="b02c2-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="b02c2-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="b02c2-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="b02c2-114">2</span><span class="sxs-lookup"><span data-stu-id="b02c2-114">2</span></span>  <br/> |<span data-ttu-id="b02c2-115">无线条</span><span class="sxs-lookup"><span data-stu-id="b02c2-115">No lines</span></span>  <br/> |<span data-ttu-id="b02c2-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="b02c2-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="b02c2-117">3</span><span class="sxs-lookup"><span data-stu-id="b02c2-117">3</span></span>  <br/> |<span data-ttu-id="b02c2-118">相关线条</span><span class="sxs-lookup"><span data-stu-id="b02c2-118">Related lines</span></span>  <br/> |<span data-ttu-id="b02c2-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="b02c2-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b02c2-120">说明</span><span class="sxs-lookup"><span data-stu-id="b02c2-120">Remarks</span></span>

<span data-ttu-id="b02c2-121">还可以在 **“页面设置”** 对话框中的 **“布局与排列”** 选项卡（在 **“设计”** 选项卡上，单击 **“页面设置”** 箭头，然后单击 **“布局与排列”**）上设置此单元格的值。</span><span class="sxs-lookup"><span data-stu-id="b02c2-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b02c2-122">若要从另一个公式或使用 **CellsU** 属性从某个程序按名称获取对 LineAdjustTo 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="b02c2-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b02c2-123">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="b02c2-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b02c2-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="b02c2-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="b02c2-125">若要从某个程序按索引获取对 LineAdjustTo 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="b02c2-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b02c2-126">内容索引：</span><span class="sxs-lookup"><span data-stu-id="b02c2-126">Section index:</span></span>  <br/> |<span data-ttu-id="b02c2-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b02c2-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b02c2-128">行索引：</span><span class="sxs-lookup"><span data-stu-id="b02c2-128">Row index:</span></span>  <br/> |<span data-ttu-id="b02c2-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b02c2-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b02c2-130">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="b02c2-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b02c2-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="b02c2-131">**visPLOLineAdjustTo**</span></span> <br/> |
   
