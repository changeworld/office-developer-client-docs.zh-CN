---
title: ShapePlaceFlip 单元格（“Shape Layout”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: 确定可放置形状的垂直翻转、 旋转，或两者上您排放形状时通过使用配置布局对话框 （在设计选项卡上的布局组中，单击重新布局页面，然后单击更多布局选项）。
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781271"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="d733d-103">ShapePlaceFlip 单元格（“Shape Layout”内容）</span><span class="sxs-lookup"><span data-stu-id="d733d-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="d733d-104">确定可放置形状的垂直翻转、 旋转，或两者上您排放形状时通过使用**配置布局**对话框 （在**设计**选项卡上的**布局**组中，单击**Re 布局页**，然后单击**更多布局选项**)。</span><span class="sxs-lookup"><span data-stu-id="d733d-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="d733d-105">**值**</span><span class="sxs-lookup"><span data-stu-id="d733d-105">**Value**</span></span>|<span data-ttu-id="d733d-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="d733d-106">**Description**</span></span>|<span data-ttu-id="d733d-107">**自动化常量**</span><span class="sxs-lookup"><span data-stu-id="d733d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d733d-108">0</span><span class="sxs-lookup"><span data-stu-id="d733d-108">0</span></span>  <br/> |<span data-ttu-id="d733d-109">使用页默认值。</span><span class="sxs-lookup"><span data-stu-id="d733d-109">Use page default.</span></span>  <br/> |<span data-ttu-id="d733d-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="d733d-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="d733d-111">1</span><span class="sxs-lookup"><span data-stu-id="d733d-111">1</span></span>  <br/> |<span data-ttu-id="d733d-112">水平翻转。</span><span class="sxs-lookup"><span data-stu-id="d733d-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="d733d-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="d733d-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="d733d-114">2</span><span class="sxs-lookup"><span data-stu-id="d733d-114">2</span></span>  <br/> |<span data-ttu-id="d733d-115">垂直翻转。</span><span class="sxs-lookup"><span data-stu-id="d733d-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="d733d-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="d733d-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="d733d-117">4</span><span class="sxs-lookup"><span data-stu-id="d733d-117">4</span></span>  <br/> |<span data-ttu-id="d733d-118">以 90 度为增量在 0 到 270 度之间翻转。</span><span class="sxs-lookup"><span data-stu-id="d733d-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="d733d-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="d733d-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="d733d-120">8</span><span class="sxs-lookup"><span data-stu-id="d733d-120">8</span></span>  <br/> |<span data-ttu-id="d733d-121">不翻转。</span><span class="sxs-lookup"><span data-stu-id="d733d-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="d733d-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="d733d-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d733d-123">注解</span><span class="sxs-lookup"><span data-stu-id="d733d-123">Remarks</span></span>

<span data-ttu-id="d733d-124">ShapePlaceFlip 单元格中的值有助于将可放置形状的方向朝向它连接的下一个可放置形状。</span><span class="sxs-lookup"><span data-stu-id="d733d-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="d733d-125">若要在绘图页上设置此行为*所有*形状，请用页面布局部分中的 PlaceFlip 单元格。</span><span class="sxs-lookup"><span data-stu-id="d733d-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="d733d-126">若要获取对 ShapePlaceFlip 单元格的引用按名称从另一个公式或从程序使用**CellsU**属性，请使用：</span><span class="sxs-lookup"><span data-stu-id="d733d-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d733d-127">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="d733d-127">Cell name:</span></span>  <br/> |<span data-ttu-id="d733d-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="d733d-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="d733d-129">若要从某个程序按索引获取对 ShapePlaceFlip 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="d733d-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d733d-130">内容索引：</span><span class="sxs-lookup"><span data-stu-id="d733d-130">Section index:</span></span>  <br/> |<span data-ttu-id="d733d-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d733d-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d733d-132">行索引：</span><span class="sxs-lookup"><span data-stu-id="d733d-132">Row index:</span></span>  <br/> |<span data-ttu-id="d733d-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="d733d-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="d733d-134">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="d733d-134">Cell index:</span></span>  <br/> |<span data-ttu-id="d733d-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="d733d-135">**visSLOPlaceFlip**</span></span> <br/> |
   
