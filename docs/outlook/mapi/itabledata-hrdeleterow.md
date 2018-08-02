---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776085"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="577e5-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="577e5-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="577e5-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="577e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="577e5-105">删除表格行。</span><span class="sxs-lookup"><span data-stu-id="577e5-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="577e5-106">参数</span><span class="sxs-lookup"><span data-stu-id="577e5-106">Parameters</span></span>

 <span data-ttu-id="577e5-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="577e5-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="577e5-108">[in]指向描述要删除的行的索引列的属性值结构的指针。</span><span class="sxs-lookup"><span data-stu-id="577e5-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="577e5-109">属性值结构的**ulPropTag**成员应包含作为_ulPropTagIndexColumn_参数对[CreateTable](createtable.md)函数的调用中的相同属性标记。</span><span class="sxs-lookup"><span data-stu-id="577e5-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="577e5-110">返回值</span><span class="sxs-lookup"><span data-stu-id="577e5-110">Return value</span></span>

<span data-ttu-id="577e5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="577e5-111">S_OK</span></span> 
  
> <span data-ttu-id="577e5-112">已成功删除行。</span><span class="sxs-lookup"><span data-stu-id="577e5-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="577e5-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="577e5-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="577e5-114">未识别_lpSPropValue_参数指向的属性表中的行。</span><span class="sxs-lookup"><span data-stu-id="577e5-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="577e5-115">说明</span><span class="sxs-lookup"><span data-stu-id="577e5-115">Remarks</span></span>

<span data-ttu-id="577e5-116">**ITableData::HrDeleteRow**方法将删除包含_lpSPropValue_参数指向的属性相匹配的列的表格行。</span><span class="sxs-lookup"><span data-stu-id="577e5-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="577e5-117">删除行的数据，并从所有打开的视图中删除行。</span><span class="sxs-lookup"><span data-stu-id="577e5-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="577e5-118">删除行之后，通知便发送至所有客户端或服务提供商的具有查看表的和已在调用表的[IMAPITable::Advise](imapitable-advise.md)方法注册的通知。</span><span class="sxs-lookup"><span data-stu-id="577e5-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="577e5-119">删除行不会降低列设置可供现有视图或随后打开视图，即使已删除的行具有特定的列的值的最后一行。</span><span class="sxs-lookup"><span data-stu-id="577e5-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="577e5-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="577e5-120">See also</span></span>



[<span data-ttu-id="577e5-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="577e5-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="577e5-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="577e5-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="577e5-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="577e5-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="577e5-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="577e5-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="577e5-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="577e5-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="577e5-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="577e5-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)
