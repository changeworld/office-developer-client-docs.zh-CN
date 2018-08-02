---
title: NoFill 单元格（“Geometry”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: 指示是否可以填充路径。
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780792"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="b7266-103">NoFill 单元格（“Geometry”部分）</span><span class="sxs-lookup"><span data-stu-id="b7266-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="b7266-104">指示是否可以填充路径。</span><span class="sxs-lookup"><span data-stu-id="b7266-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="b7266-105">**值**</span><span class="sxs-lookup"><span data-stu-id="b7266-105">**Value**</span></span>|<span data-ttu-id="b7266-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7266-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b7266-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b7266-107">TRUE</span></span>  <br/> | <span data-ttu-id="b7266-108">不填充该路径，即使可填充形状中的其他路径。</span><span class="sxs-lookup"><span data-stu-id="b7266-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="b7266-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7266-109">FALSE</span></span>  <br/> | <span data-ttu-id="b7266-110">形状的填充适用于该路径，即使它不是封闭的路径。</span><span class="sxs-lookup"><span data-stu-id="b7266-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7266-111">注释</span><span class="sxs-lookup"><span data-stu-id="b7266-111">Remarks</span></span>

<span data-ttu-id="b7266-p101">如果将形状的填充图案设置为非 (0)，则不填充该形状的任何路径。此单元格用于选择性地禁用形状中路径的填充方式。</span><span class="sxs-lookup"><span data-stu-id="b7266-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="b7266-114">要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 NoFill 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="b7266-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7266-115">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="b7266-115">Cell name:</span></span>  <br/> | <span data-ttu-id="b7266-116">Geometry *i* 。NoFill 其中*i* = < 1 >，2，3...</span><span class="sxs-lookup"><span data-stu-id="b7266-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b7266-117">要从某个程序按索引获取对 NoFill 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="b7266-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7266-118">内容索引：</span><span class="sxs-lookup"><span data-stu-id="b7266-118">Section index:</span></span>  <br/> |<span data-ttu-id="b7266-119">**visSectionFirstComponent** +  *i*其中*i* = 0、 1、 2...</span><span class="sxs-lookup"><span data-stu-id="b7266-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b7266-120">行索引：</span><span class="sxs-lookup"><span data-stu-id="b7266-120">Row index:</span></span>  <br/> |<span data-ttu-id="b7266-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="b7266-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="b7266-122">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="b7266-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b7266-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="b7266-123">**visCompNoFill**</span></span> <br/> |
   
