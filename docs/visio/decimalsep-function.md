---
title: DECIMALSEP 函数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: 返回当前用户区域设置的小数分隔符字符串。
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780065"
---
# <a name="decimalsep-function"></a>DECIMALSEP 函数

返回当前用户区域设置的小数分隔符字符串。
  
## <a name="syntax"></a>语法

DECIMALSEP( )
  
## <a name="example"></a>示例

SETF(GETREF(user.size)、 user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

