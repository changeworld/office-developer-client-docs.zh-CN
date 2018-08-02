---
title: FillPattern 单元格（“Fill Format”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: 确定形状的填充图案。要指定自定义的填充图案，请使用本单元格中的 USE 函数。
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780257"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="61d1b-104">FillPattern 单元格（“Fill Format”部分）</span><span class="sxs-lookup"><span data-stu-id="61d1b-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="61d1b-p102">确定形状的填充图案。要指定自定义的填充图案，请使用本单元格中的 USE 函数。</span><span class="sxs-lookup"><span data-stu-id="61d1b-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="61d1b-107">**值**</span><span class="sxs-lookup"><span data-stu-id="61d1b-107">**Value**</span></span>|<span data-ttu-id="61d1b-108">**说明**</span><span class="sxs-lookup"><span data-stu-id="61d1b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61d1b-109">0</span><span class="sxs-lookup"><span data-stu-id="61d1b-109">0</span></span>  <br/> |<span data-ttu-id="61d1b-110">无（透明填充）。</span><span class="sxs-lookup"><span data-stu-id="61d1b-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="61d1b-111">1</span><span class="sxs-lookup"><span data-stu-id="61d1b-111">1</span></span>  <br/> |<span data-ttu-id="61d1b-112">前景纯色。</span><span class="sxs-lookup"><span data-stu-id="61d1b-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="61d1b-113">2-40</span><span class="sxs-lookup"><span data-stu-id="61d1b-113">2 - 40</span></span>  <br/> |<span data-ttu-id="61d1b-114">各种类型的填充图案，与 **“填充”** 对话框中的索引项相对应。</span><span class="sxs-lookup"><span data-stu-id="61d1b-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61d1b-115">说明</span><span class="sxs-lookup"><span data-stu-id="61d1b-115">Remarks</span></span>

<span data-ttu-id="61d1b-116">您还可以使用 **“填充”** 对话框设置此值（在 **“开始”** 选项卡上的 **“形状”** 组中，单击 **“填充”**，然后单击 **“填充选项”**）。</span><span class="sxs-lookup"><span data-stu-id="61d1b-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="61d1b-117">若要从另一个公式或使用 **CellsU** 属性从某个程序按名称获取对 FillPattern 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="61d1b-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61d1b-118">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="61d1b-118">Cell name:</span></span>  <br/> |<span data-ttu-id="61d1b-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="61d1b-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="61d1b-120">若要从某个程序按索引获取对 FillPattern 单元格的引用，请使用带下列参数的 **CellsSRC** 属性：</span><span class="sxs-lookup"><span data-stu-id="61d1b-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61d1b-121">内容索引：</span><span class="sxs-lookup"><span data-stu-id="61d1b-121">Section index:</span></span>  <br/> |<span data-ttu-id="61d1b-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61d1b-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="61d1b-123">行索引：</span><span class="sxs-lookup"><span data-stu-id="61d1b-123">Row index:</span></span>  <br/> |<span data-ttu-id="61d1b-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="61d1b-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="61d1b-125">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="61d1b-125">Cell index:</span></span>  <br/> |<span data-ttu-id="61d1b-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="61d1b-126">**visFillPattern**</span></span> <br/> |
   
