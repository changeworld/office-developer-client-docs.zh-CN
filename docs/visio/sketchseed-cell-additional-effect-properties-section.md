---
title: SketchSeed 单元格（“Additional Effect Properties”部分）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: 代表用来确定素描效果，为正整数的几何随机值。 素描效果应用于形状时随机创建 SketchSeed 单元格的值。
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781377"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>SketchSeed 单元格（“Additional Effect Properties”部分）

代表用来确定素描效果，为正整数的几何随机值。 素描效果应用于形状时随机创建**SketchSeed**单元格的值。 
  
## <a name="remarks"></a>说明

要从另一个公式，由**N** **单元格**元素的属性的值或使用**CellsU**属性从某个程序按名称获取对**SketchSeed**单元格的引用，请使用： 
  
|||
|:-----|:-----|
| 单元格名称：  <br/> | SketchSeed  <br/> |
   
若要从某个程序按索引获取对**SketchSeed**单元格的引用，请使用带下列参数的**CellsSRC**属性： 
  
|||
|:-----|:-----|
| 内容索引：  <br/> |**visSectionObject** <br/> |
| 行索引：  <br/> |**visRowOtherEffectProperties** <br/> |
| 单元格索引：  <br/> |**visSketchSeed** <br/> |
   

