---
title: ConLineJumpStyle 单元格（“Shape Layout”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: 确定动态连接线上的跨线的跨线样式。
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779963"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle 单元格（“Shape Layout”部分）

确定动态连接线上的跨线的跨线样式。
  
|**值**|**跨线样式**|**自动常量**|
|:-----|:-----|:-----|
|0  <br/> |页面默认值  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |弧形  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |间距  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |正方形  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |三角形  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |三个面  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |四个面  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |五个面  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |六个面  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |七个面  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|内容索引：  <br/> |**visSectionObject** <br/> |
|行索引：  <br/> |**visRowShapeLayout** <br/> |
|单元格索引：  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>说明

您还可以设置此单元格的值选择动态连接线，在[开发人员](run-in-developer-mode-display-the-developer-tab.md)选项卡上的**形状设计**组中单击**行为**，然后单击**连接器**选项卡。 
  
若要从另一个公式或使用 **CellsU** 属性从某个程序按名称获取对 ConLineJumpStyle 单元格的引用，请使用： 
  
|||
|:-----|:-----|
|单元格名称：  <br/> |ConLineJumpStyle  <br/> |
   
若要从某个程序按索引获取对 ConLineJumpStyle 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  

