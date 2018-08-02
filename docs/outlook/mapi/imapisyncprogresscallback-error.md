---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775672"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="6414a-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="6414a-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="6414a-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="6414a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6414a-105">提供发送/接收对话框中显示的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6414a-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="6414a-106">如果同步过程中遇到错误，存储提供程序调用此函数。</span><span class="sxs-lookup"><span data-stu-id="6414a-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="6414a-107">参数</span><span class="sxs-lookup"><span data-stu-id="6414a-107">Parameters</span></span>

 <span data-ttu-id="6414a-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="6414a-108">**hResult**</span></span>
  
> <span data-ttu-id="6414a-109">相应的 HRESULT 错误或警告。</span><span class="sxs-lookup"><span data-stu-id="6414a-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="6414a-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="6414a-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="6414a-111">指向与该错误以显示关联的字符串的指针。</span><span class="sxs-lookup"><span data-stu-id="6414a-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6414a-112">返回值</span><span class="sxs-lookup"><span data-stu-id="6414a-112">Return value</span></span>

<span data-ttu-id="6414a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6414a-113">S_OK</span></span> 
  
> <span data-ttu-id="6414a-114">呼叫成功或多个预期值返回。</span><span class="sxs-lookup"><span data-stu-id="6414a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6414a-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6414a-115">See also</span></span>



[<span data-ttu-id="6414a-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6414a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
