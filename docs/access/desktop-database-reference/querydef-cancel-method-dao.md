---
title: QueryDef.Cancel 方法 (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab28f1b976144c40eb8be639bb7c7a1adc3e4450
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920226"
---
# <a name="querydefcancel-method-dao"></a>QueryDef.Cancel 方法 (DAO)


**适用于**： Access 2013、 Office 2013

## <a name="syntax"></a>语法

*表达式*。取消

*表达式*一个代表**QueryDef**对象的变量。

## <a name="remarks"></a>说明

使用**Cancel**方法可以终止执行异步**Execute**或**OpenConnection**方法调用 （即，该方法使用 dbRunAsync 选项调用）。 如果您正在尝试进行终止的方法中未使用 dbRunAsync，则**取消**将返回一个运行时错误。

