---
title: 具有可重复读取的隔离级别死锁
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742a9157c3f2f26d70351fc05afa35472654af9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944324"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>具有可重复读取的隔离级别死锁


**适用于**： Access 2013、 Office 2013

如果自定义业务对象使用可重复读取隔离级别访问 SQL Server，且该业务对象同时被两个在相同事务中发送查询并进行更新的客户端调用，那么有可能发生死锁。远程数据服务专门设计为允许其中一个进程超时以释放死锁，但该客户端的更新将失败。

使用[游标服务](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out**动态属性来修改超时的长度。

