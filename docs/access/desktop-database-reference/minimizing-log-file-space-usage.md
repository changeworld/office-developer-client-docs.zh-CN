---
title: 尽量减少日志文件空间使用率
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c462641616c126c7732433fc8b7d23bb137b06a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944765"
---
# <a name="minimizing-log-file-space-usage"></a>尽量减少日志文件空间使用率

**适用于**： Access 2013、 Office 2013

如果 SQL Server 数据库上存在大量的活动，那么日志文件可能很快就会写满（从而阻碍服务器的运行）。您可以将日志文件设置为 **在检查点截断日志** ，以显著延长数据库日志文件的使用时间。

**在 Microsoft SQL Server 6.5 中启用"在检查点截断日志"功能的方法**

1.  启动 Microsoft SQL Server 企业管理器，打开"服务器"树，然后打开"数据库设备"树。

2.  双击要启用此功能的服务器的名称。

3.  从**数据库**选项卡中，选择**截断**。

4.  从**选项**选项卡中，选择**在检查点截断日志**，然后单击**确定**。

**在 Microsoft SQL Server 7.0 中启用"在检查点截断日志"功能的方法**

1.  启动 Microsoft SQL Server 企业管理器，打开"服务器"树，然后打开"数据库"树。

2.  右键单击此功能将启用在其，选择**属性**的数据库的名称。

3.  从**选项**选项卡中，选择**在检查点截断日志**，然后单击**确定**。

有关 **在检查点截断日志** 功能的详细信息，请参阅 Microsoft SQL Server 文档。

