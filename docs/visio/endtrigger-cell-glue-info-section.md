---
title: EndTrigger 单元格（“Glue Info”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: 包含由应用程序生成的触发器公式，该公式确定是否移动一维形状的终点以便保持其与另一个形状的连接。
ms.openlocfilehash: 3a2fadd3d00bc23e689bbf22bb3b5db3efcd71f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780187"
---
# <a name="endtrigger-cell-glue-info-section"></a>EndTrigger 单元格（“Glue Info”部分）

包含由应用程序生成的触发器公式，该公式确定是否移动一维形状的终点以便保持其与另一个形状的连接。
  
## <a name="remarks"></a>注释

当使用动态粘附将一维形状粘附到另一个形状时，Visio 会生成一个公式，公式中引用其他形状的 EventXFMod 单元格。当更改该形状时，Visio 会重新计算引用其 EventXFMod 单元格的任何公式，包括 EndTrigger 单元格中的公式。该一维形状的其他公式引用 EndTrigger 单元格并根据需要移动一维形状的端点或变更形状。
  
要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 EndTrigger 单元格的引用，请使用： 
  
|||
|:-----|:-----|
| 单元格名称：  <br/> | EndTrigger  <br/> |
   
要从某个程序按索引获取对 EndTrigger 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  
|||
|:-----|:-----|
| 内容索引：  <br/> |**visSectionObject** <br/> |
| 行索引：  <br/> |**visRowMisc** <br/> |
| 单元格索引：  <br/> |**visEndTrigger** <br/> |
   

