---
title: Requery 方法 (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0105fb67c095355e607c6c73fc73fc4c6b1050ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998184"
---
# <a name="requery-method-ado"></a>Requery 方法 (ADO)

**适用于**： Access 2013、 Office 2013

通过重新执行对象所基于的查询，更新 [Recordset](recordset-object-ado.md) 对象中的数据。

## <a name="syntax"></a>语法

*记录集*。Requery*选项*

## <a name="parameters"></a>参数

|名称 |说明|
|:----|:----------|
|*Options* |可选。包含影响此操作的 [ExecuteOptionEnum](executeoptionenum.md) 和 [CommandTypeEnum](commandtypeenum.md) 值的位掩码。|

> [!NOTE]
> 如果*选项*设置为**adAsyncExecute**，此操作将异步执行，且当它结束时，将发布[RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md)事件。

**adExecuteNoRecords** 或 **adExecuteStream** 的 **ExecuteOpenEnum** 值不应当与 **Requery** 一起使用。

## <a name="remarks"></a>说明

**Requery** 方法用于通过重新发布原始命令和再次检索数据，从数据源刷新 **Recordset** 对象的整个内容。调用此方法的效果相当于依次调用 [Close](close-method-ado.md) 和 [Open](open-method-ado-recordset.md) 方法。如果正在编辑当前记录或添加新记录，那么将发生错误。

当 **Recordset** 对象打开时，用于定义游标特性的属性（[CursorType](cursortype-property-ado.md)、[LockType](locktype-property-ado.md)、[MaxRecords](maxrecords-property-ado.md) 等）为只读状态。因此，**Requery** 方法只能刷新当前游标。若要更改任意游标属性并查看结果，必须使用 [Close](close-method-ado.md) 方法，以使属性再次变为读/写状态。随后，可以更改属性设置并调用 [Open](open-method-ado-recordset.md) 方法重新打开游标。

