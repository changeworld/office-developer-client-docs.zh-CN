---
title: BulletString 单元格（“Paragraph”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: 允许您创建自定义的项目符号样式。
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779817"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="cf8cc-103">BulletString 单元格（“Paragraph”内容）</span><span class="sxs-lookup"><span data-stu-id="cf8cc-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="cf8cc-104">允许您创建自定义的项目符号样式。</span><span class="sxs-lookup"><span data-stu-id="cf8cc-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf8cc-105">注解</span><span class="sxs-lookup"><span data-stu-id="cf8cc-105">Remarks</span></span>

<span data-ttu-id="cf8cc-p101">将样式作为字符串输入（加上引号）。例如，可输入下面的字符串：“ooo”。</span><span class="sxs-lookup"><span data-stu-id="cf8cc-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="cf8cc-108">您还可以设置此单元格的值右键单击形状，指向**格式**，单击**文本**，然后单击**项目符号**选项卡。</span><span class="sxs-lookup"><span data-stu-id="cf8cc-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="cf8cc-109">若要获取对 BulletString 单元格的引用按名称从另一个公式或从程序使用**CellsU**属性，请使用：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf8cc-110">单元格名称：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-110">Cell name:</span></span>  <br/> |<span data-ttu-id="cf8cc-111">Para.BulletStr [ *i* ] 其中*i* = < 1 >，2，3，...</span><span class="sxs-lookup"><span data-stu-id="cf8cc-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="cf8cc-112">若要从某个程序按索引获取对 BulletString 单元格的引用，请使用带下列参数的**CellsSRC**属性：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf8cc-113">内容索引：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-113">Section index:</span></span>  <br/> |<span data-ttu-id="cf8cc-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="cf8cc-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="cf8cc-115">行索引：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-115">Row index:</span></span>  <br/> |<span data-ttu-id="cf8cc-116">**visRowParagraph** +  *i*其中*i* = 0、 1、 2...</span><span class="sxs-lookup"><span data-stu-id="cf8cc-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="cf8cc-117">单元格索引：</span><span class="sxs-lookup"><span data-stu-id="cf8cc-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cf8cc-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="cf8cc-118">**visBulletString**</span></span> <br/> |
   
