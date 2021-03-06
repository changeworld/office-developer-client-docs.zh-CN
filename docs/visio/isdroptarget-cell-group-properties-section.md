---
title: IsDropTarget 单元格（“Group Properties”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: 确定组合是否允许您通过将形状放在该组合上来添加形状。
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780480"
---
# <a name="isdroptarget-cell-group-properties-section"></a>IsDropTarget 单元格（“Group Properties”部分）

确定组合是否允许您通过将形状放在该组合上来添加形状。
  
|**值**|**说明**|
|:-----|:-----|
|TRUE  <br/> |可以通过将形状放在组合上来将形状添加到其中。  <br/> |
|FALSE  <br/> |不能将形状拖放在组合上。  <br/> |
   
## <a name="remarks"></a>注解

您还可以采用以下方法设置此值：选择该组合，在[“开发工具”](run-in-developer-mode-display-the-developer-tab.md)选项卡上单击 **“行为”**，然后选中 **“接受放下的形状”** 复选框。 
  
若要通过将形状拖放到组合中的方法将形状添加到组合中，您还必须启用类似的形状行为。您必须选择该形状，在[“开发工具”](run-in-developer-mode-display-the-developer-tab.md)选项卡上单击 **“行为”**，然后选中 **“放下时将形状添加到组合”** 复选框。此值将存储在“Miscellaneous”内容中的 IsDropSource 单元格中。 
  
若要从另一个公式或使用 **CellsU** 属性从某个程序按名称获取对 IsDropTarget 单元格的引用，请使用： 
  
|||
|:-----|:-----|
|单元格名称：  <br/> |IsDropTarget  <br/> |
   
若要从某个程序按索引获取对 IsDropTarget 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  
|||
|:-----|:-----|
|内容索引：  <br/> |**visSectionObject** <br/> |
|行索引：  <br/> |**visRowGroup** <br/> |
|单元格索引：  <br/> |**visGroupIsDropTarget** <br/> |
   

