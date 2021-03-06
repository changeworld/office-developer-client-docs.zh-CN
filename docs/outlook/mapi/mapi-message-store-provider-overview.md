---
title: MAPI 消息存储提供程序概述
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 614d9ab1037f0fc2735112801e30e530bfafe4db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569069"
---
# <a name="mapi-message-store-provider-overview"></a>MAPI 消息存储提供程序概述
  
**适用于**： Outlook 2013 |Outlook 2016 
  
消息存储提供程序处理对存储和检索的邮件和其他用户的客户端应用程序的信息。 使用称为的消息存储的分层系统，邮件信息的排列方式。 消息存储在多个级别实现与名为按住不同类型的邮件的文件夹的容器。 没有为邮件存储区; 中的级别数限制文件夹可以包含很多子文件夹。 
  
下图显示分层消息存储体系结构。
  
**消息存储体系结构**
  
![消息存储体系结构](media/amapi_03.gif "消息存储体系结构")
  
下图显示了两个文件夹，其中用子文件夹。 客户端应用程序用户可以访问的每个文件夹中包含的邮件的摘要视图或单独查看与表单。 客户端显示 MAPI 提供对标准窗体或自定义窗体的窗体开发人员提供取决于类型或类的邮件。 第一个文件夹包含说明消息，并使用 MAPI 标准注意窗体。 第二个文件夹包含库存请求消息，并使用自定义清单窗体。 两个窗体上的信息代表消息的属性。
  
您可以使用多种方式中的消息存储数据。 除了使用传统的电子邮件数据，可用于文件夹作为的论坛公共讨论，作为参考文档的库或容器的语音邮件、 日历、 联系人或任务，例如。 单个消息存储可以保留许多类型的信息。 多个客户端可以安装相同的消息存储。 这样共享数据，轻松和快速。 
  
消息存储文件夹使您能够进行排序和筛选消息和自定义用户界面中的消息显示。 指向筛选的邮件保存在名为搜索结果文件夹的特殊文件夹中。 客户端应用程序的用户输入筛选条件，其中 MAPI 指限制和条件应用于一个或多个文件夹中存储的消息。 例如，用户可能想要查看的处理特定主题和已到达日期晚于上一周的邮件。 在搜索文件夹中，列出引用符合条件的邮件和实际的邮件保留在其正则文件夹。
  
邮件是从一个用户或另一个用户或应用程序的应用程序传输的数据的单位。 每个邮件包含一些消息文本，与简单或复杂格式和用于传输邮件信封信息。 某些消息包括一个或多个附件或其他数据与传输的文件，另一条消息或 OLE 对象形式一条消息。 
  
根据邮件存储提供程序，用户可以保存当前的已发送或接收邮件此外编写的新消息。 消息可以复制或从一个文件夹移动到另一个用成为可复制、 删除或修改单独的单独消息每个副本。 某些消息存储提供程序启用另一个功能是已收到后更改一条消息，并将其存储在其文件夹返回的功能。 用户可能需要使用此功能的旋转，颠倒传入传真邮件。 用户可供以后查看的文件夹中存储的正确的视图。 
  
## <a name="see-also"></a>另请参阅

- [MAPI 功能和体系结构](mapi-features-and-architecture.md)

