---
title: 空闲状态
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591798"
---
# <a name="idle-state"></a>空闲状态

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
 本主题介绍复制状态机空闲状态期间出现的情况。 
  
## <a name="quick-info"></a>快速信息

|||
|:-----|:-----|
|状态标识符：  <br/> |**LR_SYNC_IDLE** <br/> |
|相关的数据结构：  <br/> | *None*  <br/> |
|从此状态：  <br/> | *不适用*  <br/> |
|为此状态：  <br/> |[同步状态](synchronize-state.md) <br/> |
   
> [!NOTE]
> 复制状态机是确定性状态机。 从一种状态传出到另一个客户端从后者必须最终返回到前者。 
  
## <a name="description"></a>说明

没有处于此状态反应。 启动复制之前和之后复制已完成的本地存储区处于此状态。
  
## <a name="see-also"></a>另请参阅



[关于复制 API](about-the-replication-api.md)
  
[MAPI 常量](mapi-constants.md)
  
[关于复制状态计算机](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

