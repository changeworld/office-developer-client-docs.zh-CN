---
title: PidLidSharingLocalType 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: aa1f76a3f410294de9c7ebfb3e64bbb1cd6cc25c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394711"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a>PidLidSharingLocalType 规范属性

  
  
**适用于**：Outlook 2013 | Outlook 2016 
  
指定要共享的文件夹的**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) 属性的值。 这是邮件的共享的属性。
  
|||
|:-----|:-----|
|相关属性：  <br/> |dispidSharingLocalType  <br/> |
|属性进行设置：  <br/> |PSETID_Sharing  <br/> |
|长 ID （盖）：  <br/> |0x00008A14  <br/> |
|数据类型：  <br/> |PT_UNICODE  <br/> |
|区域：  <br/> |共享  <br/> |
   
## <a name="remarks"></a>说明

此属性的值必须是下列选项之一：
  
- "IPF。约会"
    
- "IPF。联系人"
    
- "IPF。任务"
    
- "IPF。便笺"
    
- "IPF。日记"
    
## <a name="related-resources"></a>相关资源

### <a name="protocol-specifications"></a>协议规范

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 提供属性集定义和相关的 Exchange Server 协议规范的引用。
    
[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> 共享客户端之间的邮箱文件夹。
    
### <a name="header-files"></a>头文件

Mapidefs.h
  
> 提供数据类型定义。
    
## <a name="see-also"></a>另请参阅



[MAPI 属性](mapi-properties.md)
  
[MAPI 规范属性](mapi-canonical-properties.md)
  
[将规范属性名称映射到 MAPI 名称](mapping-canonical-property-names-to-mapi-names.md)
  
[将 MAPI 名称映射到规范属性名称](mapping-mapi-names-to-canonical-property-names.md)

