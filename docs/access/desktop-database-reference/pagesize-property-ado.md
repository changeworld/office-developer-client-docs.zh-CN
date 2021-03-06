---
title: PageSize 属性 (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883272"
---
# <a name="pagesize-property-ado"></a>PageSize 属性 (ADO)


**适用于**： Access 2013、 Office 2013

指示由多少记录构成 [Recordset](recordset-object-ado.md) 中的一页。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个 **Long** 值，指示页上的记录数。默认值为 10。

## <a name="remarks"></a>备注

使用 **PageSize** 属性可确定组成数据逻辑页的记录数。 建立页大小允许您使用 [AbsolutePage](absolutepage-property-ado.md) 属性来移到特定页的第一个记录。 当您希望允许逐页浏览数据，用户一次查看一定数量的记录时，这很有用在 web 服务器方案。

可随时设置此属性，并将其值用于计算特定页的首条记录的位置。

