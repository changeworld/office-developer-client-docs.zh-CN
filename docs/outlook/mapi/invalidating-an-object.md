---
title: 使对象无效
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566472"
---
# <a name="invalidating-an-object"></a>使对象无效

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
为您提供商的关闭过程的一部分，您可能想要使无效对象。 使无效对象涉及将包含的三种**IUnknown**方法的实现 vtable 替换为其 vtable: **AddRef**和**Release**， **QueryInterface**。 使对象无效通过调用[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)，每个三个公共提供程序类型的支持对象中包含的方法。 提供程序通常在其登录对象**注销**方法的实现中进行此呼叫。 
  
使无效对象提供了 MAPI 最终负责释放与对象关联的内存。 您可以释放所有连接与对象的资源，然后调用**MakeInvalid**使所有其继承接口中的方法无效。 调用下列任一方法将返回 MAPI_E_INVALID_OBJECT。 使用**MakeInvalid**是许多服务提供商忽略选择一个选项。 
  
## <a name="see-also"></a>另请参阅



[关闭服务提供程序](shutting-down-a-service-provider.md)

