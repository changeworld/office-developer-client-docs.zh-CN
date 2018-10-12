---
title: 断开和重新连接记录集
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90435606bb0b3059f5769c12fe7cf3cac0c8f9f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468835"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>断开和重新连接记录集


**适用于**： Access 2013 |Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>断开和重新连接记录集

ADO 的一项最强大功能是您能够从数据源打开一个客户端 **Recordset**，然后将该 **Recordset** 与数据源*断开*。一旦 **Recordset** 已断开，即可关闭与数据源的连接，从而释放用来维护该连接的服务器资源。您可以在 **Recordset** 断开的情况下继续查看和编辑其中的数据，随后再重新连接到数据源，并在批模式下发送更新。

若要断开 **Recordset**，请用 **adUseClient** 的游标位置将它打开，然后将 **ActiveConnection** 属性设置为等于 *Nothing*。（C++ 用户应当将 **ActiveConnection** 设置为等于 NULL 才能断开连接。）

在某些情况下，我们需要在客户端计算机不连接网络时让应用程序可以使用 **Recordset** 中的数据，本章随后将针对该情况讨论 **Recordset** 持久化，到时将使用断开的 **Recordset** 。
