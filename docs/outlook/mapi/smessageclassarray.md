---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: b2caa70600bd32234e38420f274bcd5c46ffb070
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578155"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
包含指向邮件类字符串的数组。
  
|||
|:-----|:-----|
|头文件：  <br/> |Mapiform.h  <br/> |
|相关的宏：  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Members

 **cValues**
  
> 该数组中的邮件类字符串指针的计数。
    
 **aMessageClass**
  
> 指向邮件类字符串的数组。
    
## <a name="remarks"></a>注解

**SMessageClassArray**结构作为中的以下方法的参数传递： 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>另请参阅



[MAPI 结构](mapi-structures.md)

