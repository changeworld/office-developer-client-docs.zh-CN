---
title: SelectMode 单元格（“Group Properties”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: 确定如何选择组合形状及其组成部分。
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781232"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="2f2ca-103">SelectMode 单元格（“Group Properties”内容）</span><span class="sxs-lookup"><span data-stu-id="2f2ca-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="2f2ca-104">确定如何选择组合形状及其组成部分。</span><span class="sxs-lookup"><span data-stu-id="2f2ca-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="2f2ca-105">**值**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-105">**Value**</span></span>|<span data-ttu-id="2f2ca-106">**选择模式**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-106">**Selection mode**</span></span>|<span data-ttu-id="2f2ca-107">**自动化常量**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f2ca-108">0</span><span class="sxs-lookup"><span data-stu-id="2f2ca-108">0</span></span>  <br/> |<span data-ttu-id="2f2ca-109">仅选择组合形状。</span><span class="sxs-lookup"><span data-stu-id="2f2ca-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="2f2ca-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="2f2ca-111">1</span><span class="sxs-lookup"><span data-stu-id="2f2ca-111">1</span></span>  <br/> |<span data-ttu-id="2f2ca-112">首先选择组合形状。</span><span class="sxs-lookup"><span data-stu-id="2f2ca-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="2f2ca-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="2f2ca-114">2</span><span class="sxs-lookup"><span data-stu-id="2f2ca-114">2</span></span>  <br/> |<span data-ttu-id="2f2ca-115">首先选择组合的组成部分。</span><span class="sxs-lookup"><span data-stu-id="2f2ca-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="2f2ca-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f2ca-117">备注</span><span class="sxs-lookup"><span data-stu-id="2f2ca-117">Remarks</span></span>

<span data-ttu-id="2f2ca-118">您还可以在**行为**对话框来设置此值 （组选定形状，在[开发人员](run-in-developer-mode-display-the-developer-tab.md)选项卡的**形状设计**组中，单击**行为**，，然后单击**组下的**选择**列表中的模式行为**)。</span><span class="sxs-lookup"><span data-stu-id="2f2ca-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="2f2ca-119">要从另一个公式或使用**CellsU**属性从某个程序按名称获取对 SelectMode 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f2ca-120">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-120">Cell name:</span></span>  <br/> |<span data-ttu-id="2f2ca-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="2f2ca-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="2f2ca-122">若要从某个程序按索引获取对 SelectMode 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f2ca-123">内容索引：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-123">Section index:</span></span>  <br/> |<span data-ttu-id="2f2ca-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2f2ca-125">行索引：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-125">Row index:</span></span>  <br/> |<span data-ttu-id="2f2ca-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="2f2ca-127">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="2f2ca-127">Cell index:</span></span>  <br/> |<span data-ttu-id="2f2ca-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-128">**visGroupSelectMode**</span></span> <br/> |
   
