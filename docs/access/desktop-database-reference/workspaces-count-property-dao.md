---
title: Workspaces.Count 属性 (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a2e2d048d59add02c020b0c6d3ed5b91918c58e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922921"
---
# <a name="workspacescount-property-dao"></a>Workspaces.Count 属性 (DAO)


**适用于**： Access 2013、 Office 2013

返回指定集合中的对象数。只读。

## <a name="syntax"></a>语法

*表达式*。计数

*表达式*一个代表**Workspaces**对象的变量。

## <a name="remarks"></a>注解

由于集合的成员是从 0 开始编号的，因此应始终将循环编写为从第 0 个成员开始，而在 **Count** 属性的值减 1 处结束。如果想要在不检查 **Count** 属性的情况下遍历集合成员，则可以使用 **For Each...Next** 命令。

**Count** 属性设置从不为 Null。如果其值为 0，则表示集合中没有对象。

