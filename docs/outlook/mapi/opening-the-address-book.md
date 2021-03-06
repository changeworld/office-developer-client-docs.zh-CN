---
title: 打开在通讯簿
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 62a4e6a09570cc3d71b0797ed7fff162d05ee416
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583685"
---
# <a name="opening-the-address-book"></a>打开在通讯簿

**适用于**： Outlook 2013 |Outlook 2016 
  
调用[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)打开集成的通讯簿和检索指向 MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)接口。 **IAddrBook**接口的方法可用于访问所有的配置文件中的地址簿提供程序的每个容器中的条目。 
  
**OpenAddressBook**可能返回警告，MAPI_W_ERRORS_RETURNED，以指示时出现问题与一个或多个地址簿提供程序。 交互式客户端应调用[IMAPISession::GetLastError](imapisession-getlasterror.md)检索其他错误信息并显示呼叫**OpenAddressBook**返回的信息第一个时间，并返回一条警告。 
  
非交互式客户端应忽略的警告，并继续如同方法成功。 返回的**IAddrBook**接口是有效无论是否所有，一些，或无配置文件中的地址簿提供程序正在运行。 因此，交互式和非交互式客户端必须始终记住要在会话结束时释放**IAddrBook**指针。 
  

