---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776081"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="e7b6d-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="e7b6d-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="e7b6d-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7b6d-105">删除多个表行。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="e7b6d-106">参数</span><span class="sxs-lookup"><span data-stu-id="e7b6d-106">Parameters</span></span>

 <span data-ttu-id="e7b6d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7b6d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e7b6d-108">[in]位掩码的标志控制删除的。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="e7b6d-109">可以设置以下标记：</span><span class="sxs-lookup"><span data-stu-id="e7b6d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e7b6d-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="e7b6d-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="e7b6d-111">从表和发送单个 TABLE_RELOAD 通知的所有相应的视图中删除所有行。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="e7b6d-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="e7b6d-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="e7b6d-113">[in]一个指向介绍要删除的行的行集。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="e7b6d-114">_LprowsetToDelete_参数可以是 NULL，如果_ulFlags_参数中设置 TAD_ALL_ROWS 标志。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e7b6d-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="e7b6d-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="e7b6d-116">[输出]已删除的行数。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7b6d-117">返回值</span><span class="sxs-lookup"><span data-stu-id="e7b6d-117">Return value</span></span>

<span data-ttu-id="e7b6d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7b6d-118">S_OK</span></span> 
  
> <span data-ttu-id="e7b6d-119">已成功删除的表格行。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7b6d-120">说明</span><span class="sxs-lookup"><span data-stu-id="e7b6d-120">Remarks</span></span>

<span data-ttu-id="e7b6d-121">**ITableData::HrDeleteRows**方法查找并删除包含匹配指向按行中每个**aRow**条目的**lpProps**成员设置的属性的列的表格行。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="e7b6d-122">索引列用于标识每一行;此列必须具有相同的属性标记为对[CreateTable](createtable.md)函数的调用中_ulPropTagIndexColumn_参数中传递的属性标记。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="e7b6d-123">_CRowsDeleted_返回的实际已删除的行数。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="e7b6d-124">如果找不到一个或多个行，则不返回任何错误。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="e7b6d-125">删除行之后，通知便发送至所有客户端或服务提供商的具有查看表的和已在调用表的[IMAPITable::Advise](imapitable-advise.md)方法注册的通知。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="e7b6d-126">删除行不会降低到现有表视图中可用的列或随后打开表视图，即使已删除的行的最后一个具有特定的列的值。</span><span class="sxs-lookup"><span data-stu-id="e7b6d-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7b6d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7b6d-127">See also</span></span>



[<span data-ttu-id="e7b6d-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="e7b6d-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="e7b6d-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="e7b6d-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="e7b6d-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="e7b6d-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="e7b6d-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e7b6d-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e7b6d-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e7b6d-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e7b6d-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7b6d-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)
