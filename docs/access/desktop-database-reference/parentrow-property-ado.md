---
title: ParentRow 属性 (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950145"
---
# <a name="parentrow-property-ado"></a>ParentRow 属性 (ADO)

**适用于**： Access 2013、 Office 2013

在 **ADORecordConstruction** 对象上设置 OLE DB **Row** 对象的容器，以便将行的父项转换为 ADO **Record** 对象。

为只写属性。

## <a name="syntax"></a>语法

HRESULT 放置\_ParentRow (\[的\]IUnknown\* pParent);

## <a name="parameters"></a>参数

|参数|说明|
|:--------|:----------|
|*pParent* |行的容器。|

## <a name="return-values"></a>返回值

此属性方法返回标准 HRESULT 值，包括 S\_确定和 E\_失败。

## <a name="applies-to"></a>适用于

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

