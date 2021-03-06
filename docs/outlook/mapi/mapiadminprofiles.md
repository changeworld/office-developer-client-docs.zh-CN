---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581284"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
创建一个配置文件管理对象。 
  
|||
|:-----|:-----|
|头文件：  <br/> |Mapix.h  <br/> |
|通过实现：  <br/> |MAPI  <br/> |
|调用：  <br/> |客户端应用程序  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>参数

 _ulFlags_
  
> [in]标志指示的服务项功能的选项的位掩码。 
    
 _lppProfAdmin_
  
> [输出]为指向新的配置文件管理对象的指针。
    
## <a name="return-value"></a>返回值

S_OK 
  
> 呼叫成功或多个预期值返回。
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参考 （英文）

MFCMAPI 示例代码，请参阅下表。
  
|**文件**|**函数**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI 使用**MAPIAdminProfiles**方法来获取配置文件管理对象。  <br/> |
   
## <a name="see-also"></a>另请参阅



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI 代码示例](mfcmapi-as-a-code-sample.md)

