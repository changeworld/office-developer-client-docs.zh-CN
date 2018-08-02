---
title: POINTALONGPATH 函数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: 返回路径上某一点的坐标或在路径中的偏离量。
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780890"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="62624-103">POINTALONGPATH 函数</span><span class="sxs-lookup"><span data-stu-id="62624-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="62624-104">返回路径上某一点的坐标或在路径中的偏离量。</span><span class="sxs-lookup"><span data-stu-id="62624-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="62624-105">版本信息</span><span class="sxs-lookup"><span data-stu-id="62624-105">Version Information</span></span>

<span data-ttu-id="62624-106">添加的版本： Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="62624-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62624-107">语法</span><span class="sxs-lookup"><span data-stu-id="62624-107">Syntax</span></span>

<span data-ttu-id="62624-108">POINTALONGPATH (* **部分** *，* **差旅** * * * *[，偏移量]* * * * * *[、 段]* * *)</span><span class="sxs-lookup"><span data-stu-id="62624-108">POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="62624-109">参数</span><span class="sxs-lookup"><span data-stu-id="62624-109">Parameters</span></span>

|<span data-ttu-id="62624-110">**名称**</span><span class="sxs-lookup"><span data-stu-id="62624-110">**Name**</span></span>|<span data-ttu-id="62624-111">**必需/可选**</span><span class="sxs-lookup"><span data-stu-id="62624-111">**Required/Optional**</span></span>|<span data-ttu-id="62624-112">**数据类型**</span><span class="sxs-lookup"><span data-stu-id="62624-112">**Data Type**</span></span>|<span data-ttu-id="62624-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="62624-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="62624-114">_section_</span><span class="sxs-lookup"><span data-stu-id="62624-114">_section_</span></span> <br/> |<span data-ttu-id="62624-115">必需</span><span class="sxs-lookup"><span data-stu-id="62624-115">Required</span></span>  <br/> |<span data-ttu-id="62624-116">**字符串**</span><span class="sxs-lookup"><span data-stu-id="62624-116">**String**</span></span> <br/> |<span data-ttu-id="62624-117">Geometry 节代表路径，通过对其 Path 单元格的引用指定（例如 Geometry1.Path）。</span><span class="sxs-lookup"><span data-stu-id="62624-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="62624-118">_出差_</span><span class="sxs-lookup"><span data-stu-id="62624-118">_travel_</span></span> <br/> |<span data-ttu-id="62624-119">必需</span><span class="sxs-lookup"><span data-stu-id="62624-119">Required</span></span>  <br/> |<span data-ttu-id="62624-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="62624-120">**Double**</span></span> <br/> |<span data-ttu-id="62624-p101">从起点到终点经过的路径的百分比，用于标识点。必须为介于 0 和 1 之间的值。</span><span class="sxs-lookup"><span data-stu-id="62624-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="62624-123">_偏移量_</span><span class="sxs-lookup"><span data-stu-id="62624-123">_offset_</span></span> <br/> |<span data-ttu-id="62624-124">可选</span><span class="sxs-lookup"><span data-stu-id="62624-124">Optional</span></span>  <br/> |<span data-ttu-id="62624-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="62624-125">**Double**</span></span> <br/> |<span data-ttu-id="62624-p102">点在路径中的偏移量。有关详细信息，请参阅“注解”。</span><span class="sxs-lookup"><span data-stu-id="62624-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="62624-128">_段_</span><span class="sxs-lookup"><span data-stu-id="62624-128">_segment_</span></span> <br/> |<span data-ttu-id="62624-129">可选</span><span class="sxs-lookup"><span data-stu-id="62624-129">Optional</span></span>  <br/> |<span data-ttu-id="62624-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="62624-130">**Integer**</span></span> <br/> |<span data-ttu-id="62624-131">用于计算坐标的路径段（从 1 开始）。</span><span class="sxs-lookup"><span data-stu-id="62624-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="62624-132">返回值</span><span class="sxs-lookup"><span data-stu-id="62624-132">Return value</span></span>

 <span data-ttu-id="62624-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="62624-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62624-134">说明</span><span class="sxs-lookup"><span data-stu-id="62624-134">Remarks</span></span>

<span data-ttu-id="62624-135">如果_section_或_segment_不存在，Microsoft Visio 将返回 #REF ！。</span><span class="sxs-lookup"><span data-stu-id="62624-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="62624-136">正*偏移*值指定点位于路径延伸方向的左侧。</span><span class="sxs-lookup"><span data-stu-id="62624-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="62624-137">负*偏移*值指定点位于路径延伸方向的右侧。</span><span class="sxs-lookup"><span data-stu-id="62624-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="62624-138">**点**是指以单个值表示的几何坐标有序对 (*x,y*)。</span><span class="sxs-lookup"><span data-stu-id="62624-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  
