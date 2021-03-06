---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566584"
---
# <a name="updele"></a>UPDELE

**适用于**： Outlook 2013 |Outlook 2016 
  
扩展的本地存储区中已被删除的项目的信息。 [上载删除状态状态](upload-delete-status-state.md)期间使用此信息。
  
## <a name="quick-info"></a>快速信息

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [out] / [输入] 要上载期间确定适当的行为的标志。
    
  - UPD_ASSOC
    
    - [输出]项目相关联。
    
  - UPD_MOV
    
    - [输出]项目被移。
    
  - UPD_OK 
    
    - [in]上载成功。 客户端设置后将上载到服务器的信息。
    
  - UPD_MOVED
    
    - [in]项目已成功移动。
    
  - UPD_UPDATE
    
    - [in]标记源项的修改。
    
  - UPD_COMMIT
    
    - [in]提交现在上载状态 （输入 0）。
    
_skey_
  
> [输出]项目的源键。
    
_dwReserved_
  
> [输出]此成员仅供内部使用的 Outlook，不支持。
    
_binChg_
  
> [输出]如果项目已移动，请更改目标项键。
    
_binPcl_
  
> [输出]如果已移动项目，更改目标项的列表。
    
_skeyDst_
  
> [输出]如果项目的目标项源键已移动。
    
_pupmov_
  
> [输出]目标文件夹信息如果项目已被移动。
    
## <a name="see-also"></a>另请参阅

- [关于复制 API](about-the-replication-api.md) 
- [关于复制状态计算机](about-the-replication-state-machine.md)
- [MAPI 常量](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

