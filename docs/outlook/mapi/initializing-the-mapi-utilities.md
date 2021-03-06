---
title: 初始化 MAPI 实用工具
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567669"
---
# <a name="initializing-the-mapi-utilities"></a>初始化 MAPI 实用工具

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
如果您需要使用 MAPI 的唯一部分都实用程序 — 接口和函数在 MAPI 的 MAPIUTIL 中声明。如**IPropData**和**ITableData** H 头文件 — 您不需要进行初始化调用**MAPIInitialize** 。 有关详细信息，请参阅[IPropData: IMAPIProp](ipropdataimapiprop.md)， [ITableData: IUnknown](itabledataiunknown.md)，和[MAPIInitialize](mapiinitialize.md)。 相反，调用**ScInitMapiUtil**函数。 有关详细信息，请参阅[ScInitMapiUtil](scinitmapiutil.md)。 **ScInitMapiUtil**允许客户端应用程序使用实用工具函数和需要 MAPI 分配器，但的不要求其明确的方法。 
  
在关闭时，请调用**DeinitMapiUtil**以释放资源连接到实用程序。 不要调用**MAPIUninitialize**。 有关详细信息，请参阅[DeinitMapiUtil](deinitmapiutil.md)和[MAPIUninitialize](mapiuninitialize.md)。
  
注意**ITableData**接口不支持的客户端的以前呼叫过**ScInitMapiUtil** ，而不是**MAPIInitialize**表通知。 
  

