---
title: FIND 函数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: 查找包含在另一个文本字符串中的一个文本字符串，并返回您查找的文本字符串相对于其在所处文本字符串中位置的起始位置。
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780282"
---
# <a name="find-function"></a><span data-ttu-id="b4b7f-103">FIND 函数</span><span class="sxs-lookup"><span data-stu-id="b4b7f-103">FIND Function</span></span>

<span data-ttu-id="b4b7f-104">查找包含在另一个文本字符串中的一个文本字符串，并返回您查找的文本字符串相对于其在所处文本字符串中位置的起始位置。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b4b7f-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4b7f-105">Syntax</span></span>

<span data-ttu-id="b4b7f-106">查找 (* * *find_text* * *，* * *within_text* * *，[* * *start_num* * *]，[* * *ignore_case* * *])</span><span class="sxs-lookup"><span data-stu-id="b4b7f-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4b7f-107">参数</span><span class="sxs-lookup"><span data-stu-id="b4b7f-107">Parameters</span></span>

|<span data-ttu-id="b4b7f-108">**名称**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-108">**Name**</span></span>|<span data-ttu-id="b4b7f-109">**必需/可选**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-109">**Required/Optional**</span></span>|<span data-ttu-id="b4b7f-110">**数据类型**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-110">**Data Type**</span></span>|<span data-ttu-id="b4b7f-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4b7f-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="b4b7f-112">_find_text_</span></span> <br/> |<span data-ttu-id="b4b7f-113">必需</span><span class="sxs-lookup"><span data-stu-id="b4b7f-113">Required</span></span>  <br/> |<span data-ttu-id="b4b7f-114">**字符串**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-114">**String**</span></span> <br/> |<span data-ttu-id="b4b7f-115">要查找的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="b4b7f-116">_format_</span><span class="sxs-lookup"><span data-stu-id="b4b7f-116">_format_</span></span> <br/> |<span data-ttu-id="b4b7f-117">必需</span><span class="sxs-lookup"><span data-stu-id="b4b7f-117">Required</span></span>  <br/> |<span data-ttu-id="b4b7f-118">**字符串**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-118">**String**</span></span> <br/> |<span data-ttu-id="b4b7f-119">包含要查找的文本的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="b4b7f-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="b4b7f-120">_start_num_</span></span> <br/> |<span data-ttu-id="b4b7f-121">可选</span><span class="sxs-lookup"><span data-stu-id="b4b7f-121">Optional</span></span>  <br/> |<span data-ttu-id="b4b7f-122">**编号**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-122">**Number**</span></span> <br/> |<span data-ttu-id="b4b7f-123">开始搜索的字符。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-123">The character at which to start the search.</span></span> <span data-ttu-id="b4b7f-124">在_within_text_中的第一个字符是 1。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="b4b7f-125">如果_start_num_不存在，假定为 1。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="b4b7f-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="b4b7f-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="b4b7f-127">可选</span><span class="sxs-lookup"><span data-stu-id="b4b7f-127">Optional</span></span>  <br/> |<span data-ttu-id="b4b7f-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4b7f-128">**Boolean**</span></span> <br/> |<span data-ttu-id="b4b7f-p102">默认情况下，FIND 函数区分大小写。如果希望 FIND 函数忽略大小写，请将此参数设置为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b4b7f-131">返回值</span><span class="sxs-lookup"><span data-stu-id="b4b7f-131">Return value</span></span>

<span data-ttu-id="b4b7f-132">Number</span><span class="sxs-lookup"><span data-stu-id="b4b7f-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4b7f-133">说明</span><span class="sxs-lookup"><span data-stu-id="b4b7f-133">Remarks</span></span>

<span data-ttu-id="b4b7f-134">如果找到了多个匹配，则 FIND 函数返回字符串中的第一个匹配的起始位置。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="b4b7f-135">_Find_text_参数不考虑为通配符任意字符。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="b4b7f-136">如果_find_text_:</span><span class="sxs-lookup"><span data-stu-id="b4b7f-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="b4b7f-137">为空 ("")，FIND 将匹配搜索字符串中的第一个字符 （即，字符编号_为 start_num_或 1）。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="b4b7f-138">不会显示在_within_text_中，查找返回 #VALUE ！</span><span class="sxs-lookup"><span data-stu-id="b4b7f-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="b4b7f-139">错误值。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-139">error value.</span></span> 
    
<span data-ttu-id="b4b7f-140">如果_start_num_:</span><span class="sxs-lookup"><span data-stu-id="b4b7f-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="b4b7f-p105">不大于零 (0)，FIND 将返回 #VALUE! 错误值。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="b4b7f-143">大于_within_text_，find 将返回 #VALUE 的长度 ！</span><span class="sxs-lookup"><span data-stu-id="b4b7f-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="b4b7f-144">错误值。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="b4b7f-145">示例</span><span class="sxs-lookup"><span data-stu-id="b4b7f-145">Example</span></span>

<span data-ttu-id="b4b7f-146">FIND ("2003","January 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="b4b7f-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="b4b7f-147">返回 12。</span><span class="sxs-lookup"><span data-stu-id="b4b7f-147">Returns 12.</span></span> 
  
