---
title: HASCATEGORY 函数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: 如果形状的类别列表中包含指定的字符串，则返回 TRUE。
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780388"
---
# <a name="hascategory-function"></a><span data-ttu-id="51db1-103">HASCATEGORY 函数</span><span class="sxs-lookup"><span data-stu-id="51db1-103">HASCATEGORY Function</span></span>

<span data-ttu-id="51db1-104">如果形状的类别列表中包含指定的字符串，则返回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="51db1-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="51db1-105">版本信息</span><span class="sxs-lookup"><span data-stu-id="51db1-105">Version Information</span></span>

<span data-ttu-id="51db1-106">添加的版本： Visio 2010</span><span class="sxs-lookup"><span data-stu-id="51db1-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51db1-107">语法</span><span class="sxs-lookup"><span data-stu-id="51db1-107">Syntax</span></span>

<span data-ttu-id="51db1-108">HASCATEGORY (* **类别** *)</span><span class="sxs-lookup"><span data-stu-id="51db1-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51db1-109">参数</span><span class="sxs-lookup"><span data-stu-id="51db1-109">Parameters</span></span>

|<span data-ttu-id="51db1-110">**名称**</span><span class="sxs-lookup"><span data-stu-id="51db1-110">**Name**</span></span>|<span data-ttu-id="51db1-111">**必需/可选**</span><span class="sxs-lookup"><span data-stu-id="51db1-111">**Required/Optional**</span></span>|<span data-ttu-id="51db1-112">**数据类型**</span><span class="sxs-lookup"><span data-stu-id="51db1-112">**Data Type**</span></span>|<span data-ttu-id="51db1-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="51db1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51db1-114">_category_</span><span class="sxs-lookup"><span data-stu-id="51db1-114">_category_</span></span> <br/> |<span data-ttu-id="51db1-115">必需</span><span class="sxs-lookup"><span data-stu-id="51db1-115">Required</span></span>  <br/> |<span data-ttu-id="51db1-116">**字符串**</span><span class="sxs-lookup"><span data-stu-id="51db1-116">**String**</span></span> <br/> |<span data-ttu-id="51db1-117">要搜索的类别。</span><span class="sxs-lookup"><span data-stu-id="51db1-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51db1-118">返回值</span><span class="sxs-lookup"><span data-stu-id="51db1-118">Return value</span></span>

 <span data-ttu-id="51db1-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="51db1-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51db1-120">备注</span><span class="sxs-lookup"><span data-stu-id="51db1-120">Remarks</span></span>

 <span data-ttu-id="51db1-121">*类别*是可用于对形状进行分类的用户定义的字符串。</span><span class="sxs-lookup"><span data-stu-id="51db1-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="51db1-122">您可以在形状的 ShapeSheet User.msvShapeCategories 单元格中定义类别。</span><span class="sxs-lookup"><span data-stu-id="51db1-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="51db1-123">您可以通过使用分号分隔类别来定义形状的多个类别。</span><span class="sxs-lookup"><span data-stu-id="51db1-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
