---
title: PidTagReceiveFolderSettings 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571456"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings 规范属性

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
包含表的邮件存储的接收文件夹设置。
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|标识符：  <br/> |0x3415  <br/> |
|数据类型：  <br/> |PT_OBJECT  <br/> |
|区域：  <br/> |MAPI 邮件存储  <br/> |
   
## <a name="remarks"></a>注解

可以在[IMAPIProp::CopyTo](imapiprop-copyto.md)操作中排除或[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作中包括此属性。 作为 PT_OBJECT 类型的属性，它无法成功检索[IMAPIProp::GetProps](imapiprop-getprops.md)方法;应由[IMAPIProp::OpenProperty](imapiprop-openproperty.md)方法，请求具有标识符 IID_IMAPITable 接口访问其内容。 服务提供商必须将其报告[IMAPIProp::GetPropList](imapiprop-getproplist.md)方法或如果其设置，但可以选择将其报告不如果它未设置。 
  
若要检索目录，客户端应用程序应调用[IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)方法。 有关详细信息，请参阅[接收文件夹表](receive-folder-tables.md)。
  
此属性包含的接收文件夹的消息存储库的映射表。 调用**OpenProperty**此属性等效于调用**GetReceiveFolderTable**消息存储库。 
  
## <a name="related-resources"></a>相关资源

### <a name="header-files"></a>头文件

Mapidefs.h
  
> 提供数据类型定义。
    
Mapitags.h
  
> 包含作为替代名称列出的属性的定义。
    
## <a name="see-also"></a>另请参阅



[MAPI 属性](mapi-properties.md)
  
[MAPI 规范属性](mapi-canonical-properties.md)
  
[将规范属性名称映射到 MAPI 名称](mapping-canonical-property-names-to-mapi-names.md)
  
[将 MAPI 名称映射到规范属性名称](mapping-mapi-names-to-canonical-property-names.md)

