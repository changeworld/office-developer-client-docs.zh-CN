---
title: Open 方法 (ADO Stream)
TOCTitle: Open Method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 025a1a5141adab07999337f9cc518edd2b669fdf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468377"
---
# <a name="open-method-ado-stream"></a>Open 方法 (ADO Stream)


**适用于**： Access 2013 |Office 2013


用于打开 [Stream](stream-object-ado.md) 对象，以操作二进制数据流或文本数据流。

## <a name="syntax"></a>语法

*流*。 打开*源*、*模式*、 *OpenOptions*、*用户名*、*密码*

## <a name="parameters"></a>参数

  - *Source*

  - 可选。 **变量型** 值，用于指定 **Stream** 的数据源。 *源*可能包含指向已知树结构中，如电子邮件或文件系统中的现有节点的绝对 URL 字符串。 应使用 URL 关键字指定 URL ("URL =*方案*://*服务器*/*文件夹*")。 另外， *Source*可以包含对打开与**记录**相关联的默认流已打开[Record](record-object-ado.md)对象的引用。 如果未指定*源*，**流**实例化和打开，默认情况下与没有基础源关联。 有关 URL 架构及其关联提供程序的详细信息，请参阅 [绝对 URL 和相对 URL](absolute-and-relative-urls.md)。

  - *Mode*

  - 可选。 指定产生的**Stream**的访问模式[ConnectModeEnum](connectmodeenum.md)值 (例如，读/写或只读)。 默认值为**adModeUnknown**。 请参阅有关访问模式的详细信息的[Mode](mode-property-ado.md)属性。 如果未指定*模式*，它被继承的源对象。 例如，如果**记录**的源在只读模式打开，**流**将还打开只读模式中默认情况下。

  - *OpenOptions*

  - 可选。[StreamOpenOptionsEnum](streamopenoptionsenum.md) 值。默认值为 **adOpenStreamUnspecified** 。

  - *UserName*

  - 可选。包含用户标识的 **字符串型** 值，如果需要，将访问 **Stream** 对象。

  - *Password*

  - 可选。包含密码的 **字符串型** 值，如果需要，将访问 **Stream** 对象。

## <a name="remarks"></a>备注

作为源参数，*用户 Id*和*密码*参数中传递**Record**对象时不使用**Record**对象访问是已可用。 同样， **Record**对象[模式](mode-property-ado.md)被转移到**Stream**对象。如果未指定*源*，打开的**流**不包含数据和的[大小](https://msdn.microsoft.com/library/jj250128\(v=office.15\))为零 (0)。 若要避免丢失**流**关闭时，会写入此**流**的任何数据，请使用[CopyTo](copyto-method-ado.md)或[SaveToFile](savetofile-method-ado.md)方法保存**流**或将其保存到另一个内存位置。

**AdOpenStreamFromRecord** *OpenOptions*值标识*源*参数设置为已打开的**Record**对象的内容。 默认行为是*源*视为直接指向树状结构中，例如文件中的节点的 URL。 将打开与该节点关联的默认流。

在 **Stream** 未打开时，可以读取 **Stream** 的所有只读属性。如果 **Stream** 是异步打开的，则所有后续操作（检查 [State 属性 (ADO)](state-property-ado.md) 和其他只读属性的操作除外）将被阻止，直到 **Open** 操作完成。

除了上面讨论的选项外，如果不指定 *Source*，可以在内存中只实例化 **Stream** 对象，而不将其与基础源关联。只需使用 [Write](write-method-ado.md) 或 [WriteText](writetext-method-ado.md) 将二进制数据或文本数据写入 **Stream**，或者使用 [LoadFromFile](loadfromfile-method-ado.md) 从文件中加载数据，便可以动态地向流添加数据。
