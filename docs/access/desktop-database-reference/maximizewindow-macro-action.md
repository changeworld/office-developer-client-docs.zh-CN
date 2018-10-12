---
title: MaximizeWindow 宏操作
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b612d050d6c523ae836b21aa27826ff180e8f977
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25467005"
---
# <a name="maximizewindow-macro-action"></a>MaximizeWindow 宏操作


**适用于**： Access 2013 |Office 2013

如果访问配置为使用重叠窗口而不是选项卡式文档，您可以使用**MaximizeWindow**操作放大活动窗口，使其填充 Access 窗口。 此操作可使您看到活动窗口中尽可能多的数据库对象。


> [!NOTE]
> <P>[!注释] 此操作不能应用于 Visual Basic 编辑器中的代码窗口。有关如何影响代码窗口的信息，请参阅 <STRONG>WindowState</STRONG> 属性主题。</P>



## <a name="setting"></a>设置

**MaximizeWindow** 操作不具有任何参数。

## <a name="remarks"></a>说明

此操作等效于单击窗口右上角中的 **"最大化"** 按钮或单击窗口 **"控件"** 菜单上的 **"最大化"**。

可以使用 **RestoreWindow** 操作使最大化窗口还原为其原来的大小。

**提示**

  - 如果要最大化的窗口不是活动窗口，可能需要使用 **SelectObject** 操作。

  - 当在 Access 窗口最大化时，所有其他窗口不会最大化时所打开或切换到它们。 不过，弹出式窗体不会最大化。 如果您希望在其他窗口最大化时保持其大小的窗体，，设置其**PopUp**属性为**是**。

若要在 Visual Basic for Applications 模块中运行 **MaximizeWindow** 操作，请使用 **DoCmd** 对象的 **Maximize** 方法。
