---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589845"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
返回的收件人的传输提供程序处理的类型。
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>参数

 _lpulFlags_
  
> [输出]返回控制的字符串类型的标志位掩码。 可以设置以下标记：
    
MAPI_UNICODE 
  
> 返回的字符串采用 Unicode 格式。 如果未设置 MAPI_UNICODE 标志的字符串是以 ANSI 格式。
    
 _lpcAdrType_
  
> [输出]一个指向_lpppszAdrTypeArray_参数指向该数组中的条目数。 
    
 _lpppszAdrTypeArray_
  
> [输出]指向为标识的收件人类型的字符串数组的指针的指针。
    
 _lpcMAPIUID_
  
> [输出]一个指向_lpppUIDArray_参数指向该数组中的条目数。 
    
 _lpppUIDArray_
  
> [输出]指向为数组指向[MAPIUID](mapiuid.md)结构标识的收件人类型的指针的指针的指针。 
    
## <a name="return-value"></a>返回值

S_OK 
  
> 传输提供程序成功指明它可以处理的收件人的类型。
    
## <a name="notes-to-implementers"></a>针对实施者的注释

MAPI 后台处理程序调用**IXPLogon::AddressTypes**方法，以便传输提供程序可以指示处理哪些类型的收件人的传输提供程序返回从调用[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)方法后立即。 指示此，传输提供程序应_lpppszAdrTypeArray_参数中后将指针传递给数组指针为字符串，或_lpppUIDArray_参数中后将指针传递给数组指向**MAPIUID**结构或在这两个参数传递值。 
  
以下两个数组用于不同标识过程。 MAPI 和 MAPI 后台处理程序用于[MAPIUID](mapiuid.md)结构_lpppUIDArray_数组中标识的直接处理通过传输提供程序或消息系统传输提供程序连接到这些收件人的项标识符. MAPI 和 MAPI 后台处理程序都不使用任何这些**MAPIUID**结构; 中包含的项标识符展开地址这些结构仅用于收件人类型标识。 
  
MAPI 后台处理程序使用每个字符串_lpppszAdrTypeArray_参数中的比较测试在决定哪些传输提供程序应处理出站邮件的收件人。 如果邮件收件人的**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 属性与标识消息传输提供程序提供的地址类型之一的字符串完全匹配，提供程序可以将邮件传递给该收件人。
  
如果多个传输提供程序可以处理相同类型的收件人，MAPI 选择基于客户端应用程序的配置文件中所指示的传输优先级顺序传输提供程序。 若要确定要使用的传输提供程序，MAPI 后台处理程序扫描优先级顺序中的所有提供程序指定**MAPIUID**结构，然后所有提供程序指定的地址类型值的优先级顺序。 要匹配此扫描中的特定收件人的第一个传输提供程序获取处理此收件人的第一个机会。 如果该提供商并不处理收件人，MAPI 后台处理程序将继续扫描尚未处理任何收件人查找传输提供程序。 直到找到没有进一步的匹配项，此时原件报告生成的未处理任何收件人，将继续扫描。 
  
如果提供程序始终支持一组特定的收件人类型，可以是静态的地址类型和**MAPIUID**数组传递传输提供程序。 如果传输提供程序动态构造这些数组，它可以使用以前对**TransportLogon**的调用中传递的支持对象，尽管这是不必要分配内存。
  
直到最后一个呼叫到[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)方法中，在这段时间传输提供程序可以释放内存，如有必要，用于地址类型和**MAPIUID**数组的内存应保持分配。 返回从**TransportLogoff**呼叫之后，传输提供程序不应改变这些阵列的内容。 
  
传输提供程序可以处理任何类型的收件人可以在_lpppszAdrTypeArray_参数中返回 NULL。 对于基于 LAN 的消息系统使用中央服务器通常将传出邮件传递到各种外部消息系统传输提供程序执行此操作。 此类型的传输提供程序应在 MAPI 和 MAPI 上次安装后台处理程序的配置文件中的传输提供程序的优先级顺序。 
  
不支持与其根据地址类型调度的出站消息的传输提供程序应在_lpppszAdrTypeArray_中返回一个零长度字符串。 如果传输提供程序支持无收件人类型，它应**MAPIUID**结构和地址类型为空字符串传递 NULL。 此类型的传输提供程序通常用于安装消息预处理器。 
  
## <a name="see-also"></a>另请参阅



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

