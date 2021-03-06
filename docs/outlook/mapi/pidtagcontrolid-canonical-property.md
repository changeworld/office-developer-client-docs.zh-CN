---
title: PidTagControlId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577511"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId 规范属性

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
包含在对话框中使用的控件的唯一标识符。 
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_CONTROL_ID  <br/> |
|标识符：  <br/> |0x3F07  <br/> |
|数据类型：  <br/> |PT_BINARY  <br/> |
|区域：  <br/> |MAPI 显示表  <br/> |
   
## <a name="remarks"></a>注解

此属性包含控件的唯一标识符。 此标识符应包含一个[GUID](guid.md)结构和**LONG**类型的二进制值。 在对话框中的所有控件应都使用相同的**GUID**标识服务提供商，并每个控件应都使用唯一**LONG**值，以确保控件不互相冲突。 
  
在通知中使用此属性。 例如，显示表上发送的通知必须设置此属性来唯一地标识要更新的控件。 
  
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

