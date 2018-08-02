---
title: NoLiveDynamics 单元格（“Miscellaneous”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: 确定在您操纵一个形状时，该形状是否动态改变大小或旋转。
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780789"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="23621-103">NoLiveDynamics 单元格（“Miscellaneous”部分）</span><span class="sxs-lookup"><span data-stu-id="23621-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="23621-104">确定在您操纵一个形状时，该形状是否动态改变大小或旋转。</span><span class="sxs-lookup"><span data-stu-id="23621-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="23621-105">**值**</span><span class="sxs-lookup"><span data-stu-id="23621-105">**Value**</span></span>|<span data-ttu-id="23621-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="23621-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="23621-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="23621-107">TRUE</span></span>  <br/> | <span data-ttu-id="23621-108">操纵形状时不动态更新它。</span><span class="sxs-lookup"><span data-stu-id="23621-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="23621-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="23621-109">FALSE</span></span>  <br/> | <span data-ttu-id="23621-110">操纵形状时动态更新它。</span><span class="sxs-lookup"><span data-stu-id="23621-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23621-111">注释</span><span class="sxs-lookup"><span data-stu-id="23621-111">Remarks</span></span>

<span data-ttu-id="23621-p101">当您调整不具备实时动态的二维 (2-D) 形状的大小或旋转该形状时，您将看到一个选择框。如果是一维 (1-D) 形状，您看到的是基于 DynFeedback 单元格的值的反馈。</span><span class="sxs-lookup"><span data-stu-id="23621-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="23621-114">要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 NoLiveDynamics 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="23621-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23621-115">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="23621-115">Cell name:</span></span>  <br/> | <span data-ttu-id="23621-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="23621-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="23621-117">要从某个程序按索引获取对 NoLiveDynamics 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="23621-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23621-118">内容索引：</span><span class="sxs-lookup"><span data-stu-id="23621-118">Section index:</span></span>  <br/> |<span data-ttu-id="23621-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23621-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23621-120">行索引：</span><span class="sxs-lookup"><span data-stu-id="23621-120">Row index:</span></span>  <br/> |<span data-ttu-id="23621-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="23621-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="23621-122">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="23621-122">Cell index:</span></span>  <br/> |<span data-ttu-id="23621-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="23621-123">**visNoLiveDynamics**</span></span> <br/> |
   
