---
title: WalkPreference 单元格（“Glue Info”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: 确定一维形状的端点是否移到其所粘附的形状的水平或垂直连接点上（当形状移到不明确的位置上时，使用动态粘附）。默认情况下，一维形状的两个端点都移到水平连接点上。
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781650"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="0d10a-104">WalkPreference 单元格（“Glue Info”内容）</span><span class="sxs-lookup"><span data-stu-id="0d10a-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="0d10a-p102">确定一维形状的端点是否移到其所粘附的形状的水平或垂直连接点上（当形状移到不明确的位置上时，使用动态粘附）。默认情况下，一维形状的两个端点都移到水平连接点上。</span><span class="sxs-lookup"><span data-stu-id="0d10a-p102">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position. By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="0d10a-107">**值**</span><span class="sxs-lookup"><span data-stu-id="0d10a-107">**Value**</span></span>|<span data-ttu-id="0d10a-108">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d10a-108">**Description**</span></span>|<span data-ttu-id="0d10a-109">**自动化常量**</span><span class="sxs-lookup"><span data-stu-id="0d10a-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0d10a-110">1</span><span class="sxs-lookup"><span data-stu-id="0d10a-110">1</span></span>  <br/> | <span data-ttu-id="0d10a-111">一维形状的起点移到垂直连接点，终点移到水平连接点（顶边到侧边连接或底边到侧边连接）。</span><span class="sxs-lookup"><span data-stu-id="0d10a-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="0d10a-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="0d10a-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="0d10a-113">2</span><span class="sxs-lookup"><span data-stu-id="0d10a-113">2</span></span>  <br/> | <span data-ttu-id="0d10a-114">一维形状的起点移到水平连接点，终点移到垂直连接点（侧边到顶边连接或侧边到底边连接）。</span><span class="sxs-lookup"><span data-stu-id="0d10a-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="0d10a-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="0d10a-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d10a-116">注释</span><span class="sxs-lookup"><span data-stu-id="0d10a-116">Remarks</span></span>

<span data-ttu-id="0d10a-p103">该单元格对动态连接线没有影响。动态连接线的行为由其排列样式决定。有关绘图页上动态连接线的默认排列样式的信息，请参见 RouteStyle 单元格；有关特定动态连接线的排列样式的信息，请参见 ShapeRouteStyle 单元格。</span><span class="sxs-lookup"><span data-stu-id="0d10a-p103">This cell has no effect on dynamic connectors. A dynamic connector's behavior is determined by its routing style. See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="0d10a-120">要从另一个公式或使用**CellsU**属性从某个程序按名称获取对 WalkPreference 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="0d10a-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d10a-121">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="0d10a-121">Cell name:</span></span>  <br/> | <span data-ttu-id="0d10a-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="0d10a-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="0d10a-123">若要从某个程序按索引获取对 WalkPreference 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="0d10a-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d10a-124">内容索引：</span><span class="sxs-lookup"><span data-stu-id="0d10a-124">Section index:</span></span>  <br/> |<span data-ttu-id="0d10a-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0d10a-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0d10a-126">行索引：</span><span class="sxs-lookup"><span data-stu-id="0d10a-126">Row index:</span></span>  <br/> |<span data-ttu-id="0d10a-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0d10a-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="0d10a-128">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="0d10a-128">Cell index:</span></span>  <br/> |<span data-ttu-id="0d10a-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="0d10a-129">**visWalkPref**</span></span> <br/> |
   
