---
title: PageRightMargin 单元格（“Print Properties”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: 指定打印页右侧的边距。
ms.openlocfilehash: 951a16ff20e294b68ed5447d330f4e7cbc100c82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780832"
---
# <a name="pagerightmargin-cell-print-properties-section"></a>PageRightMargin 单元格（“Print Properties”部分）

指定打印页右侧的边距。
  
## <a name="remarks"></a>注释

此值表示物理单位并且不受缩放单位或绘图单位的影响。例如，如果此单元格的值为 0.25 in.，那么，即使页面单位是英尺，此边距仍为 0.25 英寸。如果没有明确规定单位，则此值默认为页面单位。 
  
要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 PageRightMargin 单元格的引用，请使用： 
  
|||
|:-----|:-----|
| 单元格名称：  <br/> | PageRightMargin  <br/> |
   
要从某个程序按索引获取对 PageRightMargin 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  
|||
|:-----|:-----|
| 内容索引：  <br/> |**visSectionObject** <br/> |
| 行索引：  <br/> |**visRowPrintProperties** <br/> |
| 单元格索引：  <br/> |**visPrintPropertiesRightMargin** <br/> |
   

