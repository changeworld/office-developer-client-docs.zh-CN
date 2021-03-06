---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580682"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
执行显示一个对话框，或在客户端应用程序用户单击按钮控件时启动编程操作等任务。
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>参数

 _ulFlags_
  
> [in]保留;必须为零。
    
 _ulUIParam_
  
> [in]按钮控件将显示的对话框中的父窗口的句柄。
    
## <a name="return-value"></a>返回值

S_OK 
  
> 已成功激活按钮控件。
    
## <a name="remarks"></a>注解

**IMAPIControl::Activate**方法执行关注的用户单击按钮控件的任务。 单击显示表中，处理的一部分发生后 MAPI 调用**激活**后第一个调用[IMAPIControl::GetState](imapicontrol-getstate.md)以确定能否启用按钮。 
  
有关如何实施**激活**和其他详细信息[IMAPIControl: IUnknown](imapicontroliunknown.md)方法，请参阅[控件对象实现](control-object-implementation.md)。
  
## <a name="see-also"></a>另请参阅



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

