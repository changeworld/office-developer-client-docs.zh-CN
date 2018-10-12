---
title: EditMode 属性 (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466232"
---
# <a name="editmode-property-ado"></a>EditMode 属性 (ADO)


**适用于**： Access 2013 |Office 2013

指示当前记录的编辑状态。

## <a name="return-value"></a>返回值

返回 [EditModeEnum](editmodeenum.md) 值。

## <a name="remarks"></a>备注

ADO 维护着一个与当前记录关联的编辑缓冲区。此属性指示是否对此缓冲区进行了更改，或是否创建了新记录。通过使用 **EditMode** 属性，可以确定当前记录的编辑状态。如果编辑进程已中断，可以检测是否存在待定更改，并确定是否需要使用 [Update](update-method-ado.md) 或 [CancelUpdate](cancelupdate-method-ado.md) 方法。

有关 [EditMode](addnew-method-ado.md) 属性在各种不同编辑情况下的更为详细的说明，请参阅 **AddNew** 方法。

[删除](delete-method-ado-recordset.md)呼叫不会成功删除记录或[Recordset](recordset-object-ado.md) （由于参照完整性冲突，例如），源中数据的记录时仍处于编辑模式 (**EditMode** = **adEditInProgress**). 这意味着在从当前记录移动到别的位置（例如，使用 **Move**、[NextRecordset](move-method-ado.md) 或 [Close](nextrecordset-method-ado.md)）前，必须调用 [CancelUpdate](close-method-ado.md) 。


> [!NOTE]
> <P>[!注释] <STRONG>EditMode</STRONG> 仅在存在当前记录时才能返回有效值。如果 <STRONG>BOF 或 EOF</STRONG> 为 True 或当前记录已删除， <A href="bof-eof-properties-ado.md">EditMode</A> 将返回错误。</P>

