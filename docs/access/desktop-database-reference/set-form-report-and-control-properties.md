---
title: 设置窗体、 报表和控件属性
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466703"
---
# <a name="set-form-report-and-control-properties"></a>设置窗体、 报表和控件属性

**适用于**： Access 2013 |Office 2013

每个窗体、报表、节和控件都有各自的属性设置，可以利用这些属性来更改特定项的外观和行为。使用属性表、宏或 Visual Basic 可以查看并更改属性。

## <a name="set-properties"></a>设置属性

1. 在窗体设计视图或报表设计视图中，选择要设置其属性的控件、节、窗体或报表。可以选择：
    
   - 一个或多个控件。要选择多个控件，请按住 Shift 键并单击相应控件，或者将鼠标指针在要选择的控件上拖动。如果选择多个控件，属性表将仅显示选中的控件所共有的属性。
    
   - 一个节。单击要选择的节的节选择器。
    
   - 整个窗体或报表。单击窗体或报表左上角的窗体选择器或报表选择器。

2. 通过右键单击对象或节，然后在快捷菜单上，单击**属性**或通过单击**属性**工具栏上显示的属性表。

3. 单击要为其设置值的属性，然后执行下列操作之一：
    
   - 在属性框中键入适当的设置或表达式。
    
   - 如果属性框包含箭头，单击该箭头，然后单击列表中的值。
    
   - 如果**生成**按钮显示在右侧的属性框中，单击该按钮以显示生成器或显示一个对话框，使您可以选择生成器。 例如，您可以使用代码生成器、 宏生成器或查询生成器设置某些属性。

## <a name="tips"></a>提示

- Microsoft Access 提供了键入和查看表达式或其他长属性设置的**缩放**框。 若要显示**缩放**框中，单击属性表中的属性框。 然后按 SHIFT + F2 或右键单击，然后单击快捷菜单上的**缩放 （英文）** 。

- 对于某些控件，可以通过在控件本身中键入属性设置来设置 **ControlSource** 属性。

- 可以为一类控件更改默认属性设置，以便使未来创建的该类控件具有新的默认设置。

- 绑定控件的属性设置可能与控件所绑定到的基础表或基础查询中字段的相应设置不匹配。如果设置不同，窗体或报表设置通常会覆盖表或查询中的相应设置。有关如何继承属性的详细信息，请参阅"控件属性与其基础字段的属性的关联方式"。
