---
title: RunMenuCommand 宏操作
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25467421"
---
# <a name="runmenucommand-macro-action"></a>RunMenuCommand 宏操作


**适用于**： Access 2013 |Office 2013

可以使用 **RunMenuCommand** 操作运行内置的 Microsoft Access 命令。

## <a name="setting"></a>设置

**RunMenuCommand** 操作具有以下操作参数。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>操作参数</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Command</strong></p></td>
<td><p>要运行的命令的名称。<strong>“命令”</strong>框按照字母顺序显示 Access 中可用的内置命令。这是一个必选参数。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>说明

可以使用 **RunMenuCommand** 操作运行自定义菜单栏、全局菜单栏、自定义快捷菜单或全局快捷菜单中的 Access 命令。

可以在具有条件表达式的宏内使用 **RunMenuCommand** 操作，以便根据某些条件运行命令。


> [!NOTE]
> <P>单击<STRONG>文件</STRONG>选项卡，然后单击<STRONG>最近</STRONG>显示最近使用过的数据库。 您可以单击其中一个数据库，而不是单击<STRONG>打开</STRONG>。 这些数据库项不显示在下拉列表框中的<STRONG>命令</STRONG>参数，并且在宏中使用<STRONG>RunMenuCommand</STRONG>操作不可用。</P>



从以前版本的 Access 转换 Access 数据库时，某些命令可能不再可用。 命令可能已重命名，移动到不同的菜单上，或可能不再在 Access 中可用。 此类命令的**DoMenuItem**操作无法转换为**RunMenuCommand**操作。 当打开该宏时，Access 将显示空白**命令**参数此类命令的**RunMenuCommand**操作。 您必须编辑该宏，并输入有效的命令的参数，或删除**RunMenuCommand**操作。

若要在 Visual Basic for Applications (VBA) 模块中运行 **RunMenuCommand** 操作，请使用 **Application** 对象的 **RunCommand** 方法。（此方法等效于 **DoCmd** 对象的 **RunCommand** 方法。）
