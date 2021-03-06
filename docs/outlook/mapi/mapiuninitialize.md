---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567389"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
减少引用计数，清理，并删除每个实例全局数据的 MAPI DLL。 
  
|||
|:-----|:-----|
|头文件：  <br/> |Mapix.h  <br/> |
|通过实现：  <br/> |MAPI  <br/> |
|调用：  <br/> |客户端应用程序  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>参数

无 
  
## <a name="return-value"></a>返回值

无。
  
## <a name="remarks"></a>注解

客户端应用程序调用**MAPIUninitialize**函数结束与 MAPI，与调用[MAPIInitialize](mapiinitialize.md)函数开始与其进行交互。 调用**MAPIUninitialize**后，可以由客户端不进行任何其他 MAPI 呼叫。 
  
 **MAPIUninitialize**减少引用计数，并相应**MAPIInitialize**函数增加引用计数。 因此，一个函数调用次数必须等于到其他呼叫的数目。 
  
> [!NOTE]
> 不能调用**MAPIInitialize**或从**MAPIUninitialize** Win32 **DllMain**函数或创建或终止线程的任何其他函数中。 有关详细信息，请参阅[使用线程安全对象](using-thread-safe-objects.md)。 
  

