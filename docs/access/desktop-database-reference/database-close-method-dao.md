---
title: Database.Close 方法 (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920681"
---
# <a name="databaseclose-method-dao"></a>Database.Close 方法 (DAO)


**适用于**： Access 2013、 Office 2013

关闭已打开的 **Database**。

## <a name="syntax"></a>语法

*表达式*。关闭

*表达式*一个代表**Database**对象的变量。

## <a name="remarks"></a>注解

如果使用 **Close** 时 **Database** 对象已被关闭，将发生运行时错误。

**Close**方法的替代方法是将对象变量的值设置为**Nothing** (Set dbsTemp = Nothing)。

