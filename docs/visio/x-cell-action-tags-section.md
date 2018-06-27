---
title: X 单元格（“Action Tags”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: X-周围放置动作标记按钮的形状的本地坐标中某一点的坐标位置。
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781670"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="6f27d-103">X 单元格（“Action Tags”内容）</span><span class="sxs-lookup"><span data-stu-id="6f27d-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="6f27d-104">*X* -坐标周围放置动作标记按钮的形状的本地坐标系中的位置。</span><span class="sxs-lookup"><span data-stu-id="6f27d-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6f27d-105">在以前版本的 Microsoft Visio 中，动作标记称为“智能标记”。</span><span class="sxs-lookup"><span data-stu-id="6f27d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f27d-106">注释</span><span class="sxs-lookup"><span data-stu-id="6f27d-106">Remarks</span></span>

<span data-ttu-id="6f27d-107">X 单元格和 Y 单元格定义形状的本地坐标系中的某一点，X Justify 单元格和 Y Justify 单元格定义动作标记按钮相对于该点的放置位置。</span><span class="sxs-lookup"><span data-stu-id="6f27d-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="6f27d-108">要从另一个公式或使用**CellsU**属性从某个程序按名称获取对 X 单元格的引用，请使用：</span><span class="sxs-lookup"><span data-stu-id="6f27d-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f27d-109">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="6f27d-109">Cell name:</span></span>  <br/> |<span data-ttu-id="6f27d-110">智能标记。</span><span class="sxs-lookup"><span data-stu-id="6f27d-110">SmartTags.</span></span> <span data-ttu-id="6f27d-111">*名称*。其中 x 智能标记。</span><span class="sxs-lookup"><span data-stu-id="6f27d-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="6f27d-112">*name*是动作标记行的名称</span><span class="sxs-lookup"><span data-stu-id="6f27d-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="6f27d-113">若要从某个程序按索引获取对 X 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="6f27d-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f27d-114">内容索引：</span><span class="sxs-lookup"><span data-stu-id="6f27d-114">Section index:</span></span>  <br/> |<span data-ttu-id="6f27d-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="6f27d-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="6f27d-116">行索引：</span><span class="sxs-lookup"><span data-stu-id="6f27d-116">Row index:</span></span>  <br/> |<span data-ttu-id="6f27d-117">**visRowSmartTag** +  *i*其中*i* = 0、 1、 2...</span><span class="sxs-lookup"><span data-stu-id="6f27d-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6f27d-118">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="6f27d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6f27d-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="6f27d-119">**visSmartTagX**</span></span> <br/> |
   
