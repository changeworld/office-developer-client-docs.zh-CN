---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19775718"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="0a3ea-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0a3ea-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="0a3ea-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="0a3ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a3ea-105">返回表的状态和类型。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="0a3ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="0a3ea-106">Parameters</span></span>

 <span data-ttu-id="0a3ea-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="0a3ea-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="0a3ea-108">[输出]指向一个值，该值表的状态。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="0a3ea-109">可以返回下列值之一：</span><span class="sxs-lookup"><span data-stu-id="0a3ea-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="0a3ea-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="0a3ea-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="0a3ea-111">不正在执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-111">No operations are in progress.</span></span>
    
<span data-ttu-id="0a3ea-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="0a3ea-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="0a3ea-113">Expectantly 已更改的表的内容。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="0a3ea-114">此状态值不会返回的结果排序或限制的操作的更改。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="0a3ea-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="0a3ea-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="0a3ea-116">[IMAPITable::Restrict](imapitable-restrict.md)操作过程中出错。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="0a3ea-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="0a3ea-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="0a3ea-118">正在**IMAPITable::Restrict**操作。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="0a3ea-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="0a3ea-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="0a3ea-120">[IMAPITable::SetColumns](imapitable-setcolumns.md)操作过程中出错。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="0a3ea-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="0a3ea-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="0a3ea-122">正在**IMAPITable::SetColumns**操作。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="0a3ea-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="0a3ea-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="0a3ea-124">[IMAPITable::SortTable](imapitable-sorttable.md)操作过程中出错。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="0a3ea-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="0a3ea-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="0a3ea-126">正在**IMAPITable::SortTable**操作。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="0a3ea-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="0a3ea-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="0a3ea-128">[输出]指向一个值，指示表的类型。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="0a3ea-129">可以返回以下三个表类型之一：</span><span class="sxs-lookup"><span data-stu-id="0a3ea-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="0a3ea-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="0a3ea-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="0a3ea-131">表的内容是动态;行和列的值可以更改基础数据集更改。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="0a3ea-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="0a3ea-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="0a3ea-133">表中的行固定的但这些行中的列的值动态，并可以更改基础数据集更改。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="0a3ea-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="0a3ea-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="0a3ea-135">表是静态的而在基础数据更改时不更改其内容。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a3ea-136">返回值</span><span class="sxs-lookup"><span data-stu-id="0a3ea-136">Return value</span></span>

<span data-ttu-id="0a3ea-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a3ea-137">S_OK</span></span> 
  
> <span data-ttu-id="0a3ea-138">成功返回表的状态。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a3ea-139">说明</span><span class="sxs-lookup"><span data-stu-id="0a3ea-139">Remarks</span></span>

<span data-ttu-id="0a3ea-140">**IMAPTable::GetStatus**方法检索有关表的类型和当前状态信息。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0a3ea-141">给调用方的说明</span><span class="sxs-lookup"><span data-stu-id="0a3ea-141">Notes to callers</span></span>

<span data-ttu-id="0a3ea-142">您可用于**GetStatus**结合使用三种其他**IMAPITable**方法以监视这些操作的状态，并确定表的效果。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="0a3ea-143">呼叫**GetStatus**后使下面的**IMAPITable**调用之一：</span><span class="sxs-lookup"><span data-stu-id="0a3ea-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="0a3ea-144">[IMAPITable::Restrict](imapitable-restrict.md)设置限制。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="0a3ea-145">[IMAPITable::SortTable](imapitable-sorttable.md)建立排序顺序。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="0a3ea-146">[IMAPITable::SetColumns](imapitable-setcolumns.md)定义一列。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0a3ea-147">MFCMAPI 参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="0a3ea-147">MFCMAPI reference</span></span>

<span data-ttu-id="0a3ea-148">MFCMAPI 示例代码，请参阅下表。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0a3ea-149">**文件**</span><span class="sxs-lookup"><span data-stu-id="0a3ea-149">**File**</span></span>|<span data-ttu-id="0a3ea-150">**函数**</span><span class="sxs-lookup"><span data-stu-id="0a3ea-150">**Function**</span></span>|<span data-ttu-id="0a3ea-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0a3ea-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0a3ea-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="0a3ea-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="0a3ea-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0a3ea-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="0a3ea-154">MFCMAPI 使用**IMAPITable::GetStatus**方法报告表的状态。</span><span class="sxs-lookup"><span data-stu-id="0a3ea-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a3ea-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a3ea-155">See also</span></span>



[<span data-ttu-id="0a3ea-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="0a3ea-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="0a3ea-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0a3ea-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="0a3ea-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0a3ea-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0a3ea-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a3ea-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="0a3ea-160">MFCMAPI 代码示例</span><span class="sxs-lookup"><span data-stu-id="0a3ea-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
