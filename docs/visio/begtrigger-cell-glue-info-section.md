---
title: BegTrigger 单元格（“Glue Info”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: 包含由应用程序生成的触发器公式，该公式确定是否移动一维形状的起点以便保持其与另一个形状的连接。
ms.openlocfilehash: 5dec179f1847c30c6ef563d866360b6dd31a1d88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779663"
---
# <a name="begtrigger-cell-glue-info-section"></a>BegTrigger 单元格（“Glue Info”部分）

包含由应用程序生成的触发器公式，该公式确定是否移动一维形状的起点以便保持其与另一个形状的连接。
  
## <a name="remarks"></a>注释

当使用动态粘附将一维形状粘附到另一个形状时，应用程序会生成一个公式，公式中引用其他形状的 EventXFMod 单元格。当更改该形状时，Visio 会重新计算引用其 EventXFMod 单元格的任何公式，包括 BegTrigger 单元格中的公式。该一维形状的其他公式引用 BegTrigger 单元格并根据需要移动一维形状的起点或变更形状。
  
要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 BegTrigger 单元格的引用，请使用： 
  
|||
|:-----|:-----|
| 单元格名称：  <br/> | BegTrigger  <br/> |
   
要从某个程序按索引获取对 BegTrigger 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  
|||
|:-----|:-----|
| 内容索引：  <br/> |**visSectionObject** <br/> |
| 行索引：  <br/> |**visRowGroup** <br/> |
| 单元格索引：  <br/> |**visBegTrigger** <br/> |
   

