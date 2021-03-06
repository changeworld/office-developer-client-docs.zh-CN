---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582033"
---
# <a name="checkparms"></a>CheckParms

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
调用的内部函数，以验证调试参数调用 MAPI 服务提供程序方法。 
  
|||
|:-----|:-----|
|头文件：  <br/> |Mapival.h  <br/> |
|通过实现：  <br/> |MAPI  <br/> |
|调用：  <br/> |服务提供商  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>参数

 _eMethod_
  
> [in]通过枚举，指定要验证的方法。 
    
 _第一_
  
> [in]堆栈上第一个参数的指针。
    
## <a name="return-value"></a>返回值

S_OK 
  
> 调用成功。
    
## <a name="remarks"></a>注解

与[ValidateParms](validateparms.md)和[UlValidateParms](ulvalidateparms.md)宏**CheckParms**宏不执行完整参数验证。 MAPI 和服务之间传递参数提供程序假定已正确，因此**CheckParms**执行调试验证。 
  

