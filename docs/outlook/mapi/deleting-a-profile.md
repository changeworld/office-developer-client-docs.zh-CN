---
title: 删除配置文件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573241"
---
# <a name="deleting-a-profile"></a>删除配置文件

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
 **删除配置文件**
  
- 调用[IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)。
    
 **DeleteProfile**标记为删除的配置文件，如果当前正在使用它，等待它不再处于活动状态，以将其删除。 配置文件没有实际消失之前每个客户端与活动会话已断开。 
  
 **DeleteProfile** _ulContext_参数设置为 MSG_SERVICE_DELETE 配置文件中调用每种消息服务的入口点函数。 对入口点函数的调用发生之前从配置文件已从物理上隔离到服务。 
  

