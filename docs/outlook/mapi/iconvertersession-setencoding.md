---
title: IConverterSessionSetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382419"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**适用于**：Outlook 2013 | Outlook 2016 
  
初始化转换期间使用的编码。
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>参数

_et_
  
> 一个[ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx)值。 支持仅以下值： 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>返回值

E_INVALIDARG
  
> 传递的编码类型无效。
    
## <a name="remarks"></a>说明

使用[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)执行转换之前调用**SetEncoding** 。 
  
使用**SetEncoding**设置的最外面的消息正文将的邮件项目的编码。 Microsoft Outlook 2010 和 Microsoft Outlook 2013 中选择的任何单个附件的编码。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 引用

有关 MFCMAPI 示例代码，请参阅下表。
  
|**文件**|**函数**|**备注**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI 使用 MimeToMAPI 将 EML 文件转换为 MAPI 邮件。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI 使用 MAPIToMIMEStm 将转换为 EML 文件的 MAPI 邮件。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI 常量](mapi-constants.md)

