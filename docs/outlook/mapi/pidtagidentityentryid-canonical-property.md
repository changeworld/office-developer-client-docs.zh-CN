---
title: PidTagIdentityEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584840"
---
# <a name="pidtagidentityentryid-canonical-property"></a>PidTagIdentityEntryId 规范属性

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
包含服务提供商的标识在邮件系统中定义的项标识符。 
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|标识符：  <br/> |0x3E01  <br/> |
|数据类型：  <br/> |PT_BINARY  <br/> |
|区域：  <br/> |MAPI 状态  <br/> |
   
## <a name="remarks"></a>注解

此属性不显示任何对象的属性但只能作为状态表中的列。 它是标识的公开状态表格行的服务提供程序的一部分。 提供程序的标识通常是指其帐户的服务器上，但可以参考消息系统中定义的提供程序的任何表示。 
  
则此属性通常设置为适当的通讯簿条目标识符。 
  
Furnishing 任一标识属性的服务提供程序应提供所有这些。 属于同一消息服务的提供程序应公开的 identity 属性相同的值。 
  
## <a name="related-resources"></a>相关资源

### <a name="header-files"></a>头文件

Mapidefs.h
  
> 提供数据类型定义。
    
Mapitags.h
  
> 包含作为替代名称列出的属性的定义。
    
## <a name="see-also"></a>另请参阅



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI 属性](mapi-properties.md)
  
[MAPI 规范属性](mapi-canonical-properties.md)
  
[将规范属性名称映射到 MAPI 名称](mapping-canonical-property-names-to-mapi-names.md)
  
[将 MAPI 名称映射到规范属性名称](mapping-mapi-names-to-canonical-property-names.md)

