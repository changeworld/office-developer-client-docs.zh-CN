---
title: PidTagSentRepresentingEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385492"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a>PidTagSentRepresentingEntryId 规范属性

  
  
**适用于**：Outlook 2013 | Outlook 2016 
  
包含表示发件人的邮件用户的项标识符。
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_SENT_REPRESENTING_ENTRYID  <br/> |
|标识符：  <br/> |0x0041  <br/> |
|数据类型：  <br/> |PT_BINARY  <br/> |
|区域：  <br/> |Address  <br/> |
   
## <a name="remarks"></a>说明

此属性是一个正在表示发件人的邮件用户的地址属性。 当客户端应用程序发送消息代表另一个客户端时，它应为该客户端的值设置所有表示发件人属性。 通常在其自己的代表发送消息用户离开表示发件人属性未设置。
  
传出的传输提供程序必须始终保持不变，如果已发送的客户端设置此属性。 如果未设置它，应出站邮件，副本上将其设置为**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) 传输提供程序并将其上的本地副本中保留未设置。
  
## <a name="related-resources"></a>相关资源

### <a name="protocol-specifications"></a>协议规范

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 提供了相关的 Exchange Server 协议规范参考。
    
[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 指定的属性和操作所允许的电子邮件消息对象。
    
[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 处理顺序和客户端和服务器之间的数据传输的流。
    
[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、 RFC2446，和 RFC2447，和约会和会议对象之间进行转换。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 指定的属性和约会、 会议请求和响应消息的操作。
    
[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 指定用于连接到和它们代表另一个用户操作时，作为代理人，以及与邮件和日历的对象交互配置邮箱的方法。
    
[[MS OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> 指定的属性和允许的操作的 post 对象。
    
### <a name="header-files"></a>头文件

Mapidefs.h
  
> 提供数据类型定义。
    
Mapitags.h
  
> 包含列为相关属性的属性的定义。
    
## <a name="see-also"></a>另请参阅



[PidTagEntryId 规范属性](pidtagentryid-canonical-property.md)


[MAPI 属性](mapi-properties.md)
  
[MAPI 规范属性](mapi-canonical-properties.md)
  
[将规范属性名称映射到 MAPI 名称](mapping-canonical-property-names-to-mapi-names.md)
  
[将 MAPI 名称映射到规范属性名称](mapping-mapi-names-to-canonical-property-names.md)

