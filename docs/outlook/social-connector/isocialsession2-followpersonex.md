---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: 添加为社交网络登录用户的朋友由 emailAddresses 和 displayName 参数标识的人员。
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779251"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

添加为社交网络登录用户的朋友由_emailAddresses_和_displayName_参数标识的人员。 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>参数

_emailAddresses_
  
> [in]社交网络上的人员包含一个或多个有效的 SMTP 地址的数组。
    
_displayName_
  
> [in]一个字符串，包含要添加为朋友的人员的显示名称。
    
## <a name="remarks"></a>说明

如果 Outlook Social Connector (OSC) 提供有关超过**emailAddresses**参数，OSC 提供程序中的数组中的 SMTP 地址可以假定的第一个元素的主 SMTP 地址。 
  
如果提供程序已经**followPerson**元素作为**true**设置中**功能**XML，并且无的元素的_emailAddresses_匹配网络上的用户，提供程序必须返回 OSC_E_NOT_FOUND 错误。 如果提供程序已将**followPerson**设置为**false** ，在**功能**中，提供程序应返回 OSC_E_FAIL 错误。 
  
如果**FollowPersonEx**方法成功，提供程序可以使用字符串_displayName_参数中解决任何后续的好朋友确认电子邮件，而不是解决此人的 SMTP 地址中的人员。 另一方面，提供程序必须能够处理 OSC 传递的_displayName_参数为空字符串。 
  
如果提供程序实现[ISocialSession2](isocialsession2iunknown.md)接口，并且已将**followPerson**设置为**true**的功能 XML 中，OSC 调用**FollowPersonEx**而不是[ISocialSession::FollowPerson](isocialsession-followperson.md)。 如果提供程序已将**followPerson**设置为**true** ，但未实现**ISocialSession2**接口，或**FollowPersonEx**返回 OSC_E_NOTIMPL 错误，OSC 调用**ISocialSession::FollowPerson**。
  
## <a name="see-also"></a>另请参阅

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

