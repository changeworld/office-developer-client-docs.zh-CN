---
title: BeginTransComplete、 CommitTransComplete RollbackTransComplete 事件 (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86bb76b4feacc1b4a06d6cbbb8a436f5f9c55bd5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949487"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete、CommitTransComplete 和 RollbackTransComplete 事件 (ADO)

**适用于**： Access 2013、 Office 2013

这些事件将在对 [Connection](connection-object-ado.md) 对象的关联操作执行完毕之后调用。

- **BeginTransComplete** 在 [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) 操作之后调用。

- **CommitTransComplete** 在 [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) 操作之后调用。

- **RollbackTransComplete** 在 [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) 操作之后调用。

## <a name="syntax"></a>语法

BeginTransComplete*TransactionLevel*， *pError* *adStatus*、 *pConnection*

CommitTransComplete*pError*， *adStatus* *pConnection*

RollbackTransComplete*pError*， *adStatus* *pConnection*

## <a name="parameters"></a>参数

|参数|说明|
|:--------|:----------|
|*TransactionLevel* |**长整型** 值，包含导致该事件的新事务级别的 **BeginTrans** 。|
|*pError* |[Error](error-object-ado.md) 对象。 它介绍**adStatusErrorsOccurred**; EventStatusEnum 的值是否发生的错误否则，它将不设置。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md)。 通过在事件返回之前将该参数设置为 **adStatusUnwantedEvent** ，这些事件可以阻止随后进行通知。|
|*pConnection* |发生此事件的 **Connection** 对象。|

## <a name="remarks"></a>备注

在 Visual C++ 中，多个 **Connection** 可以共享相同的事件处理方法。方法使用返回的 **Connection** 对象来确定导致事件发生的对象。

如果 [Attributes](attributes-property-ado.md) 属性设置为 **adXactCommitRetaining** 或 **adXactAbortRetaining** ，则在提交或回滚事务之后，将开始新的事务。使用 **BeginTransComplete** 事件将忽略除第一个事务开始事件以外的所有事件。

