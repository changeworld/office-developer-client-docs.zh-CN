---
title: 获取和设置与 GetProps SetProps 属性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395005"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>获取和设置与 GetProps SetProps 属性
 
**适用于**：Outlook 2013 | Outlook 2016 
  
只要有可能，尝试检索或使用[IMAPIProp::GetProps](imapiprop-getprops.md)和[IMAPIProp::SetProps](imapiprop-setprops.md)方法修改的属性。 除非您正在使用该属性是非常大，这些方法应已足够。 其他替代方法是从读取或写入到[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)接口的流。 流可以成功处理非常大的属性，但它们是更高版本耗尽资源，因为它们需要的 COM 库。 仅在您调用**IMAPIProp::GetProps**或**IMAPIProp::SetProps**失败后，请使用**IStream**接口。 
  

