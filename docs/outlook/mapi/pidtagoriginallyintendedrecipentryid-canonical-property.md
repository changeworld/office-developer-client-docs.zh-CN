---
title: PidTagOriginallyIntendedRecipEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 4e7d97f4b2043c9ca08e487e52d58fb534c7abef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572653"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>PidTagOriginallyIntendedRecipEntryId 规范属性

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
包含自动转发邮件的最初预期接收人的项标识符。
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|标识符：  <br/> |0x1012  <br/> |
|数据类型：  <br/> |PT_BINARY  <br/> |
|区域：  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注解

此属性是在最初预期的邮件收件人的地址属性之一。 它必须已转发邮件的自动代理设置。
  
此属性对应于 X.400 报告每个收件人属性。
  
## <a name="related-resources"></a>相关资源

### <a name="header-files"></a>头文件

Mapidefs.h
  
> 提供数据类型定义。
    
Mapitags.h
  
> 包含列为相关属性的属性的定义。
    
## <a name="see-also"></a>另请参阅



[MAPI 属性](mapi-properties.md)
  
[MAPI 规范属性](mapi-canonical-properties.md)
  
[将规范属性名称映射到 MAPI 名称](mapping-canonical-property-names-to-mapi-names.md)
  
[将 MAPI 名称映射到规范属性名称](mapping-mapi-names-to-canonical-property-names.md)

