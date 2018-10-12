---
title: RowPosition 属性 (ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466404"
---
# <a name="rowposition-property-ado"></a>RowPosition 属性 (ADO)


**适用于**： Access 2013 |Office 2013



通过 **ADORecordsetConstruction** 对象获取或设置一个 OLE DB **RowPosition** 对象。 当您使用**放置\_RowPosition**设置**RowPosition**对象，生成的**Recordset**对象使用**RowPosition**对象来确定当前行。

为可读/写属性。

## <a name="syntax"></a>语法

HRESULT get\_RowPosition (\[out，retval\] IUnknown\* \* ppRowPos);

HRESULT 放置\_RowPosition (\[的\]IUnknown\* pRowPos);

## <a name="parameters"></a>参数

  - *ppRowPos*

  - 指向 OLE DB **RowPosition** 对象的指针。

  - *PRowPos*

  - 一个 OLE DB **RowPosition** 对象。

## <a name="return-values"></a>返回值

此属性方法返回标准 HRESULT 值，包括 S\_确定和 E\_失败。

## <a name="remarks"></a>备注

设置此属性时，如果 **RowPosition** 对象上的 **Rowset** 对象与 **Recordset** 对象上的 **Rowset** 对象不同，则前者将覆盖后者。 **RowPosition** 的当前 **Chapter** 也是如此。

## <a name="applies-to"></a>应用于

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)
