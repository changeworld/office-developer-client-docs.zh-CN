---
title: 强制执行通知
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578771"
---
# <a name="forcing-a-notification"></a>强制执行通知

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
当服务提供商使用[IMAPISupport: IUnknown](imapisupportiunknown.md)的通知，MAPI 方法提供了使用隐藏的窗口和其对应的窗口过程的通知。 为每个过程以接收通知，MAPI 发送给隐藏窗口的特殊的消息。 使用常量**szMAPINotificationMsg**中 MAPIDEFS 定义命名此消息。H。 
  
当隐藏的窗口的窗口过程处理**szMAPINotificationMsg**邮件，您会收到这些通知。 若要确保将发送通知，它和所需等待调度此**szMAPINotificationMsg**消息。 可以相当简单，完成实现逻辑以完成此任务，但 MAPI 提供了 MAPI DLL 入口点调用[HrDispatchNotifications](hrdispatchnotifications.md)进行处理甚至更简单。 呼叫**HrDispatchNotifications** ，如下所示，以在您的客户端接收通知： 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


