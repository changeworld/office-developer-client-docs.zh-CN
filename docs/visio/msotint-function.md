---
title: MSOTINT 函数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 通过将颜色的发光度增加指定的百分比来修改颜色。
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780809"
---
# <a name="msotint-function"></a><span data-ttu-id="0c2cb-103">MSOTINT 函数</span><span class="sxs-lookup"><span data-stu-id="0c2cb-103">MSOTINT Function</span></span>

<span data-ttu-id="0c2cb-104">通过将颜色的发光度增加指定的百分比来修改颜色。</span><span class="sxs-lookup"><span data-stu-id="0c2cb-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="0c2cb-105">版本信息</span><span class="sxs-lookup"><span data-stu-id="0c2cb-105">Version Information</span></span>

<span data-ttu-id="0c2cb-106">添加的版本： Visio 2010</span><span class="sxs-lookup"><span data-stu-id="0c2cb-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0c2cb-107">语法</span><span class="sxs-lookup"><span data-stu-id="0c2cb-107">Syntax</span></span>

<span data-ttu-id="0c2cb-108">MSOTINT (* **颜色** *，* * *deltaLum* * *)</span><span class="sxs-lookup"><span data-stu-id="0c2cb-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0c2cb-109">参数</span><span class="sxs-lookup"><span data-stu-id="0c2cb-109">Parameters</span></span>

|<span data-ttu-id="0c2cb-110">**名称**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-110">**Name**</span></span>|<span data-ttu-id="0c2cb-111">**必需/可选**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-111">**Required/Optional**</span></span>|<span data-ttu-id="0c2cb-112">**数据类型**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-112">**Data Type**</span></span>|<span data-ttu-id="0c2cb-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0c2cb-114">_color_</span><span class="sxs-lookup"><span data-stu-id="0c2cb-114">_color_</span></span> <br/> |<span data-ttu-id="0c2cb-115">必需</span><span class="sxs-lookup"><span data-stu-id="0c2cb-115">Required</span></span>  <br/> |<span data-ttu-id="0c2cb-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-116">**RGB**</span></span> <br/> |<span data-ttu-id="0c2cb-117">标准 RGB（红、绿、蓝）颜色值或对颜色的引用。</span><span class="sxs-lookup"><span data-stu-id="0c2cb-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="0c2cb-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="0c2cb-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="0c2cb-119">必需</span><span class="sxs-lookup"><span data-stu-id="0c2cb-119">Required</span></span>  <br/> |<span data-ttu-id="0c2cb-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0c2cb-120">**Integer**</span></span> <br/> |<span data-ttu-id="0c2cb-121">更改百分比白色 (-100%) 或黑色 （100%)_颜色_值。</span><span class="sxs-lookup"><span data-stu-id="0c2cb-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c2cb-122">备注</span><span class="sxs-lookup"><span data-stu-id="0c2cb-122">Remarks</span></span>

<span data-ttu-id="0c2cb-123">越接近_color_值越接近白色或黑色，淡色由特定_deltaLum_值所产生的较小更改。</span><span class="sxs-lookup"><span data-stu-id="0c2cb-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  
