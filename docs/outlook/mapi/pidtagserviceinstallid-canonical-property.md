---
title: PidTagServiceInstallId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceInstallId
api_type:
- COM
ms.assetid: 1dd14858-2ce6-4629-a2f1-82d23cd6576b
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 273796430cb2ed1badd96ddb9c8fae8b251e5802
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586254"
---
# <a name="pidtagserviceinstallid-canonical-property"></a>PidTagServiceInstallId 规范属性

  
  
**适用于**： Outlook 2013 |Outlook 2016 
  
组件提供程序的 ID。
  
|||
|:-----|:-----|
|相关属性：  <br/> |PR_SERVICE_INSTALL_ID，PR_SERVICE_INSTALL_ID_A，PR_SERVICE_INSTALL_ID_W  <br/> |
|标识符：  <br/> |0x3D13  <br/> |
|数据类型：  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|区域：  <br/> |MAPI 配置文件  <br/> |
   
## <a name="remarks"></a>注解

这些属性可能为 component 参数**MsiProvideQualifiedComponent**调用的用于安装提供程序。 
  
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

