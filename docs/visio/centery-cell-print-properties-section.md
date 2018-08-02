---
title: CenterY 单元格（“Print Properties”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: 确定绘图页是否在打印纸上垂直居中。
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779889"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="3a62f-103">CenterY 单元格（“Print Properties”部分）</span><span class="sxs-lookup"><span data-stu-id="3a62f-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="3a62f-104">确定绘图页是否在打印纸上垂直居中。</span><span class="sxs-lookup"><span data-stu-id="3a62f-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="3a62f-105">**值**</span><span class="sxs-lookup"><span data-stu-id="3a62f-105">**Value**</span></span>|<span data-ttu-id="3a62f-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a62f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3a62f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a62f-107">TRUE</span></span>  <br/> | <span data-ttu-id="3a62f-108">使绘图页在打印纸上垂直居中。</span><span class="sxs-lookup"><span data-stu-id="3a62f-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="3a62f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a62f-109">FALSE</span></span>  <br/> | <span data-ttu-id="3a62f-110">使绘图页在打印纸上不垂直居中（默认值）。</span><span class="sxs-lookup"><span data-stu-id="3a62f-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a62f-111">注释</span><span class="sxs-lookup"><span data-stu-id="3a62f-111">Remarks</span></span>

<span data-ttu-id="3a62f-p101">默认情况下，绘图页与打印纸的左上角对齐。将 CenterX 单元格和 CenterY 单元格设置为 TRUE，可以将绘图页放置在打印纸的中心（如果需要平铺，则放置在多张打印纸的中心）。</span><span class="sxs-lookup"><span data-stu-id="3a62f-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="3a62f-114">要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 CenterY 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="3a62f-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a62f-115">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="3a62f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3a62f-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="3a62f-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="3a62f-117">要从某个程序按索引获取对 CenterY 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="3a62f-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a62f-118">内容索引：</span><span class="sxs-lookup"><span data-stu-id="3a62f-118">Section index:</span></span>  <br/> |<span data-ttu-id="3a62f-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a62f-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3a62f-120">行索引：</span><span class="sxs-lookup"><span data-stu-id="3a62f-120">Row index:</span></span>  <br/> |<span data-ttu-id="3a62f-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="3a62f-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="3a62f-122">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="3a62f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3a62f-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="3a62f-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   
