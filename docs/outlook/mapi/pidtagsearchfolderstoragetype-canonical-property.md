---
title: PidTagSearchFolderStorageType 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderStorageType
api_type:
- COM
ms.assetid: 1ec21942-47db-43a5-a6ee-ec6fd2135e8b
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: accea8bdea25ac44e6cc5d8fe88cb32caf1961be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397721"
---
# <a name="pidtagsearchfolderstoragetype-canonical-property"></a>PidTagSearchFolderStorageType 规范属性

  
  
**适用于**：Outlook 2013 | Outlook 2016 
  
包含在**PR_WB_SF_DEFINITION** ([PidTagSearchFolderDefinition](pidtagsearchfolderdefinition-canonical-property.md)) 属性中指定所显示的二进制大型对象 (BLOB) 数据的标志。
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_WB_SF_STORAGE_TYPE  <br/> |
|标识符：  <br/> |0x6846  <br/> |
|数据类型：  <br/> |PT_LONG  <br/> |
|区域：  <br/> |搜索  <br/> |
   
## <a name="remarks"></a>说明

在[[MS OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)中指定的标志的定义。 **PR_WB_SF_STORAGE_TYPE**搜索。
  
## <a name="related-resources"></a>相关资源

### <a name="protocol-specifications"></a>协议规范

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 提供了相关的 Exchange Server 协议规范参考。
    
[[MS OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 指定的属性和操作的搜索文件夹列表配置的操作。
    
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

