---
title: 控制事务
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4acd03e387f50d9035c73dd2fef934f6fd6985a5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889642"
---
# <a name="controlling-transactions"></a>控制事务


**适用于**： Access 2013、 Office 2013

*事务*确定的开头和结尾的一系列连接上发生的数据访问操作。 根据数据源的事务处理功能，利用 **Connection** 对象还可以创建和管理事务。 例如，使用 Microsoft OLE DB Provider for SQL Server 访问 Microsoft SQL Server 2000 上的数据库，您可以为所执行的命令创建多个嵌套事务。

ADO 确保由于事务中的操作而引起的数据源更改一起成功发生或者根本不发生。

如果取消该事务，或其中一个操作失败，最终结果就像事务中没有发生任何操作一样。数据源将仍然保持事务开始前的状态。

ADO 对象模型不显式包括事务，但会用一组 **Connection** 对象方法（**BeginTrans**、**CommitTrans** 和 **RollbackTrans**）来代表它们。

有关事务的详细信息，请参阅[第 5 章：更新和持久化数据](chapter-5-updating-and-persisting-data.md)。

