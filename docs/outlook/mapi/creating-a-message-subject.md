---
title: 创建邮件主题
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395684"
---
# <a name="creating-a-message-subject"></a>创建邮件主题

  
  
**适用于**：Outlook 2013 | Outlook 2016 
  
邮件的主题， **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))，是可选属性，用于汇总用途的一条消息。 如果您选择将其设置，使其包含字符的字符串 128 个字节或更少。 128 字节限制并不是通过 MAPI; 施加限制它是由一些消息存储提供程序的限制。 若要确保与执行实施它的提供程序互操作性，限制为 128 个字节的主题。 
  
请注意，某些消息存储提供程序不允许**PR_SUBJECT**写入到[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)接口的流。 
  
未设置**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md));此属性是设置仅在答复和转发邮件。 
  

