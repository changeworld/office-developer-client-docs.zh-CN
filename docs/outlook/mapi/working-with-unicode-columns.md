---
title: 处理 Unicode 列
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: ffeee38920bf1c864b93e6513913c140cb658d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595305"
---
# <a name="working-with-unicode-columns"></a>处理 Unicode 列

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
可以使用标准的 8 位字符，这些属性类型 PT_STRING8 或 16 位 Unicode 字符，它们是属性类型 PT_UNICODE 表示表中的字符串。 表实施可以自由选择其表支持 Unicode 字符串。 因为 Unicode 添加值为客户端和服务提供程序通过扩展的功能集，请尽可能支持 Unicode 建议。 
  
许多表方法接受一个指示应为 Unicode 字符串属性值的标志。 在输入 MAPI_UNICODE 标志指定表示表实施，传入呼叫的所有字符串属性值的 Unicode 字符串并且具有 PT_UNICODE 属性类型。 输出，此标志指示返回的字符串的所有属性值应尽可能都为 Unicode 字符串。 标志是否具有输入或输出的含义取决于的方法。 不支持 Unicode 和传递 MAPI_UNICODE 标志表实施返回 MAPI_E_BAD_CHAR_WIDTH 值。
  
## <a name="see-also"></a>另请参阅



[MAPI 表](mapi-tables.md)

