---
title: State 属性 (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33933fb71ee3d7541640469eebc650c0f52a9784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922011"
---
# <a name="state-property-ado-md"></a>State 属性 (ADO MD)


**适用于**： Access 2013、 Office 2013

指示单元格集的当前状态。

## <a name="return-values"></a>返回值

返回一个 **Long** 整数值，该值指示 [Cellset](cellset-object-ado-md.md) 对象的当前状况，并且为只读。以下属性值有效： **adStateClosed** (0) 和 **adStateOpen** (1)。

## <a name="remarks"></a>备注

若要使用 [ObjectStateEnum](objectstateenum.md) 常量名称，必须在项目中引用 ADO 类型库。有关更多信息，请参阅 [将 ADO 与 ADO MD 结合使用](using-ado-with-ado-md.md)。

