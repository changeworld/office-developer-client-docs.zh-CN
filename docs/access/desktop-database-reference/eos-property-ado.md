---
title: EOS 属性 (ADO-访问桌面数据库参考 （英文）)）
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25467138"
---
# <a name="eos-property-ado"></a>EOS 属性 (ADO)


**适用于**： Access 2013 |Office 2013

指示当前位置是否位于流的末尾。

## <a name="return-values"></a>返回值

返回一个 **Boolean** 值，以指示当前位置是否位于流的末尾。如果流中没有更多的字节， **EOS** 将返回 **True** ；如果当前位置后还有字节，它将返回 **False** 。

若要设置流位置的末尾位置，请使用 [SetEOS](seteos-method-ado.md) 方法。若要确定当前位置，请使用 [Position](position-property-ado.md) 属性。
