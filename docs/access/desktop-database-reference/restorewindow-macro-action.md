---
title: RestoreWindow 宏操作
TOCTitle: RestoreWindow Macro Action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1dc6776310b0544b8bb807327612637a5fbcff67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468485"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow 宏操作


**适用于**： Access 2013 |Office 2013

可以使用 **RestoreWindow** 操作将已最大化或最小化的窗口还原为其原来的大小。


> [!NOTE]
> <P>[!注释] 此操作不能应用于 Visual Basic 编辑器中的代码窗口。有关如何影响代码窗口的信息，请参阅 <STRONG>WindowState</STRONG> 属性主题。</P>



## <a name="setting"></a>设置

**RestoreWindow** 操作不具有任何参数。

## <a name="remarks"></a>说明

此操作对所选的数据库对象有效。如果对象已经最小化，可以先用 **SelectObject** 操作选定它，然后使用 **RestoreWindow** 操作将它还原为其原来的大小。

可以使用 **MoveAndSizeWindow** 操作移动已经还原的窗口或者调整其大小。

**RestoreWindow** 操作等效于单击窗口右上角的 **"还原"** 按钮或者单击窗口 **"控件"** 菜单上的 **"还原"** 命令。

若要在 Visual Basic for Applications (VBA) 模块中运行 **RestoreWindow** 操作，请使用 **DoCmd** 对象的 **Restore** 方法。
