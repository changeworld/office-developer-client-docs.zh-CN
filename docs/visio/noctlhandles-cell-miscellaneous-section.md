---
title: NoCtlHandles 单元格（“Miscellaneous”内容）
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: 切换选中形状的控制手柄的显示状态 - 显示或不显示。
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780784"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>NoCtlHandles 单元格（“Miscellaneous”部分）

切换选中形状的控制手柄的显示状态 - 显示或不显示。
  
|**值**|**说明**|
|:-----|:-----|
| TRUE  <br/> | 选中形状后不显示控制手柄。  <br/> |
| FALSE  <br/> | 选中形状后显示控制手柄。  <br/> |
   
## <a name="remarks"></a>注解

要从另一个公式或从使用 **CellsU** 属性的某个程序按名称获取对 NoCtlHandles 单元格的引用，请使用： 
  
|||
|:-----|:-----|
| 单元格名称：  <br/> | NoCtlHandles  <br/> |
   
要从某个程序按索引获取对 NoCtlHandles 单元格的引用，请使用带下列参数的 **CellsSRC** 属性： 
  
|||
|:-----|:-----|
| 内容索引：  <br/> |**visSectionObject** <br/> |
| 行索引：  <br/> |**visRowMisc** <br/> |
| 单元格索引：  <br/> |**visNoCtlHandles** <br/> |
   

