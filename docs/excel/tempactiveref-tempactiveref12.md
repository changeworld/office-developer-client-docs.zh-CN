---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref 函数 [excel 2007，] TempActiveRef12 函数 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 适用于： Excel 2013 | Office 2013 | Visual Studio
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773813"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **适用于** Excel 2013 | Office 2013 | Visual Studio 
  
创建临时**XLOPER**的框架库函数/ **XLOPER12**包含对活动工作表上单元格的矩形块的外部引用。 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>参数

 _rwFirst_
  
起始行的引用。
  
 _rwLast_
  
引用的结束行。
  
行参数是从零开始的所以第 1 行传递为 0。 在 Microsoft Office Excel 2003 和早期版本，以及开始在兼容模式下运行的工作簿的 Excel 2007 中的最大值是 65535 = 2 ^16-1，WORD 整数可以采取的最大值。 启动运行工作簿的 Excel 2007 中的最大值是 1048575 = 2 ^20-1。 RW 被定义为 XLCALL 中的 32 位有符号整数。H。
  
 _colFirst_
  
参考的起始列号。
  
 _colLast_
  
参考的结束的列号。
  
列参数是从零开始的所以该列 A 传递为 0。 在 Excel 2003 和早期版本，以及开始在兼容模式下运行的工作簿的 Excel 2007 中的最大值是 255 = 2 ^8-1，字节整数可以采取的最大值。 启动运行工作簿的 Excel 2007 中的最大值是 16,383 = 2 ^14-1。 COL 被定义为 XLCALL 中的 32 位有符号整数。H。
  
## <a name="return-value"></a>返回值

返回对传入的单元格的矩形块**xltypeRef**外部引用。 
  
## <a name="example"></a>示例

本示例使用**TempActiveRef12**函数选择单元格 A105:C110。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>另请参阅



[框架库中的函数](functions-in-the-framework-library.md)

