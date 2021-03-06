---
title: Recordset、SourceRecordset 属性 (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21176e050c77b0f14fcb03b054e8a1ab692df7d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949255"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset、SourceRecordset 属性 (RDS)

**适用于**： Access 2013、 Office 2013

指示从自定义业务对象返回的 **Recordset** 对象。

## <a name="syntax"></a>语法

*DataControl*。SourceRecordset = *Recordset*

*Recordset* = *DataControl*。记录集

## <a name="parameters"></a>参数

|参数|说明|
|:--------|:----------|
|*DataControl* |一个代表 [RDS.DataControl](datacontrol-object-rds.md) 对象的对象变量。|
|*Recordset* |一个代表 **Recordset** 对象的对象变量。|

## <a name="remarks"></a>备注

可以将 **SourceRecordset** 属性设置为从自定义业务对象返回的 [Recordset](recordset-object-ado.md)。

这些属性允许应用程序通过自定义进程处理绑定进程。这些属性接收的行集包装在 **Recordset** 中，因此可以直接与 **Recordset** 进行交互，同时可执行设置属性或遍历 **Recordset** 等操作。

可以设置 **SourceRecordset** 属性，也可以在运行时在脚本代码中读取 **Recordset** 属性。

**SourceRecordset** 为只写属性，与 **Recordset** 属性恰恰相反，后者为只读属性。

