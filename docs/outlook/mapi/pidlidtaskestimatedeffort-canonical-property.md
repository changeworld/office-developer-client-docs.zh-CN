---
title: PidLidTaskEstimatedEffort 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: ceb055f6269e7abc8270c7d16da79c041d7f4ed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777063"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="4205e-103">PidLidTaskEstimatedEffort 规范属性</span><span class="sxs-lookup"><span data-stu-id="4205e-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="4205e-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="4205e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4205e-105">指示的时间，以分钟为单位，用户需要执行的任务。</span><span class="sxs-lookup"><span data-stu-id="4205e-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4205e-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="4205e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4205e-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="4205e-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="4205e-108">属性进行设置：</span><span class="sxs-lookup"><span data-stu-id="4205e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4205e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4205e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4205e-110">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="4205e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4205e-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="4205e-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="4205e-112">数据类型：</span><span class="sxs-lookup"><span data-stu-id="4205e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4205e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4205e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4205e-114">区域：</span><span class="sxs-lookup"><span data-stu-id="4205e-114">Area:</span></span>  <br/> |<span data-ttu-id="4205e-115">Task</span><span class="sxs-lookup"><span data-stu-id="4205e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4205e-116">说明</span><span class="sxs-lookup"><span data-stu-id="4205e-116">Remarks</span></span>

<span data-ttu-id="4205e-117">值必须是大于或等于 0 和小于 0x5AE980DF (1,525,252,319)，其中 480 分钟等于一个天和 2400 分钟等于一周 （在工作日和工作周中的五天 8 小时）。</span><span class="sxs-lookup"><span data-stu-id="4205e-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4205e-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="4205e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4205e-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="4205e-119">Protocol specifications</span></span>

<span data-ttu-id="4205e-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4205e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4205e-121">提供属性集定义和相关的 Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="4205e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4205e-122">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4205e-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4205e-123">定义模型的任务、 任务分配和任务更新电子等效项的多个对象。</span><span class="sxs-lookup"><span data-stu-id="4205e-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4205e-124">头文件</span><span class="sxs-lookup"><span data-stu-id="4205e-124">Header files</span></span>

<span data-ttu-id="4205e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4205e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4205e-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="4205e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4205e-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4205e-127">See also</span></span>



[<span data-ttu-id="4205e-128">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="4205e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4205e-129">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="4205e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4205e-130">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="4205e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4205e-131">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="4205e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
