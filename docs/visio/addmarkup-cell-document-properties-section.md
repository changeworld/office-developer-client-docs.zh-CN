---
title: AddMarkup 单元格（“Document Properties”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: 指示是否正对文档进行审阅以便加标记。
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779645"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="dd73e-103">AddMarkup 单元格（“Document Properties”部分）</span><span class="sxs-lookup"><span data-stu-id="dd73e-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="dd73e-104">指示是否正对文档进行审阅以便加标记。</span><span class="sxs-lookup"><span data-stu-id="dd73e-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="dd73e-105">**值**</span><span class="sxs-lookup"><span data-stu-id="dd73e-105">**Value**</span></span>|<span data-ttu-id="dd73e-106">**说明**</span><span class="sxs-lookup"><span data-stu-id="dd73e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd73e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd73e-107">TRUE</span></span>  <br/> |<span data-ttu-id="dd73e-108">正在对文档进行审阅。</span><span class="sxs-lookup"><span data-stu-id="dd73e-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="dd73e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd73e-109">FALSE</span></span>  <br/> |<span data-ttu-id="dd73e-110">未对文档进行审阅（默认值）。</span><span class="sxs-lookup"><span data-stu-id="dd73e-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd73e-111">注解</span><span class="sxs-lookup"><span data-stu-id="dd73e-111">Remarks</span></span>

<span data-ttu-id="dd73e-112">AddMarkup 单元格设置为 true，则审阅者时添加标记和更改应用于标记贴页面不的原始绘图页。</span><span class="sxs-lookup"><span data-stu-id="dd73e-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="dd73e-113">AddMarkup 单元格时为 FALSE，跟踪标记处于关闭状态，并更改应用于原始绘图页。</span><span class="sxs-lookup"><span data-stu-id="dd73e-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dd73e-114">可以对您的文档使用 GUARD 函数防止标记。</span><span class="sxs-lookup"><span data-stu-id="dd73e-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="dd73e-115">如果 AddMarkup 单元格包含公式 = GUARD(FALSE)，禁用**跟踪标记**命令。</span><span class="sxs-lookup"><span data-stu-id="dd73e-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="dd73e-116">此设置对应于 **“审阅”** 选项卡上的 **“标记”** 组中的 **“跟踪标记”** 命令设置。</span><span class="sxs-lookup"><span data-stu-id="dd73e-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="dd73e-117">若要从另一个公式或使用 **CellsU** 属性从某个程序按名称获取对 AddMarkup 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="dd73e-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd73e-118">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="dd73e-118">Cell name:</span></span>  <br/> |<span data-ttu-id="dd73e-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="dd73e-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="dd73e-120">若要从某个程序按索引获取对 AddMarkup 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="dd73e-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd73e-121">内容索引：</span><span class="sxs-lookup"><span data-stu-id="dd73e-121">Section index:</span></span>  <br/> |<span data-ttu-id="dd73e-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd73e-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd73e-123">行索引：</span><span class="sxs-lookup"><span data-stu-id="dd73e-123">Row index:</span></span>  <br/> |<span data-ttu-id="dd73e-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="dd73e-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="dd73e-125">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="dd73e-125">Cell index:</span></span>  <br/> |<span data-ttu-id="dd73e-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="dd73e-126">**visDocAddMarkup**</span></span> <br/> |
   
