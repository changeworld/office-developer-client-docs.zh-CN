---
title: Type 属性 (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1a5c9c69b5de6fbdf57efedf9724ae71ac151b7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945528"
---
# <a name="type-property-ado-stream"></a>Type 属性（ADO 流）


**适用于**： Access 2013、 Office 2013

指示 [Stream](stream-object-ado.md) 中包含的数据类型（二进制或文本）。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个 [StreamTypeEnum](streamtypeenum.md) 值，该值指定 **Stream** 对象中包含的数据类型。默认值是 **adTypeText** 。但是，如果最初将二进制数据写入新的空 **Stream** 中，则 **Type** 将更改为 **adTypeBinary** 。

## <a name="remarks"></a>备注

仅在当前位置在 **Stream** 的开始处（[Position](position-property-ado.md) 为 0）时，**Type** 属性才为可读/写属性，在任何其他位置时都为只读属性。

**Type** 属性确定对 **Stream** 执行读写操作时应使用的方法。对于文本 **Streams** ，应使用 [ReadText](readtext-method-ado.md) 和 [WriteText](writetext-method-ado.md)。对于二进制 **Streams** ，应使用 [Read](read-method-ado.md) 和 [Write](write-method-ado.md)。

