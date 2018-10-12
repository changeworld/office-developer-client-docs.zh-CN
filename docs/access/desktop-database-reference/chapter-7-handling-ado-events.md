---
title: 第 7 章：处理 ADO 事件
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468190"
---
# <a name="chapter-7-handling-ado-events"></a>第 7 章：处理 ADO 事件


**适用于**： Access 2013 |Office 2013

ADO 事件模型支持某些可在操作开始之前或在完成之后发出*事件*（即通知）的同步和异步 ADO 操作。事件实际上是对应用程序中所定义的事件处理程序例程的调用。

如果为在操作开始之前发生的一组事件提供处理程序函数或过程，则可以检查或修改传递给操作的参数。由于操作尚未执行，因此可以取消该操作或允许它完成。

如果异步使用 ADO，则在操作完成之后所发生的这组事件尤其重要。例如，操作结束时，执行完成事件将通知启动异步 [Recordset.Open](open-method-ado-recordset.md) 操作的应用程序。

使用 ADO 事件模型会使应用程序增加一些开销，但与其他处理异步操作的方法相比，它会提供更大的灵活性，例如，通过循环来监视对象的 [State](state-property-ado.md) 属性。
