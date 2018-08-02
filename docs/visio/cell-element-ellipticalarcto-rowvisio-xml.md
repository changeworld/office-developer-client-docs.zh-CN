---
title: 单元格元素 （EllipticalArcTo 行） (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: 包含 x 坐标或 y 坐标的椭圆弧终结点的 x 坐标或 y 坐标控件的 points 弧形，夹角从 x 轴到椭圆的长轴或比椭圆的主要和次要刻度轴上。
ms.openlocfilehash: 01d28fae5943251b61d0d26211ee91f09f25b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779835"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a><span data-ttu-id="e24cc-103">单元格元素 （EllipticalArcTo 行） (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e24cc-103">Cell element (EllipticalArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="e24cc-104">包含 x 坐标或 y 坐标的椭圆弧终结点的 x 坐标或 y 坐标控件的 points 弧形，夹角从 x 轴到椭圆的长轴或比椭圆的主要和次要刻度轴上。</span><span class="sxs-lookup"><span data-stu-id="e24cc-104">Contains x- or y-coordinates of an elliptical arc's endpoint, x- or y-coordinates of the control points on the arc, angle from the x-axis to the ellipse's major axis, or ratio between the ellipse's major and minor axes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e24cc-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="e24cc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e24cc-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="e24cc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e24cc-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e24cc-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e24cc-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="e24cc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e24cc-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="e24cc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e24cc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e24cc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e24cc-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="e24cc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e24cc-112">母版页 #.xml、 页面 #.xml</span><span class="sxs-lookup"><span data-stu-id="e24cc-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e24cc-113">定义</span><span class="sxs-lookup"><span data-stu-id="e24cc-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e24cc-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="e24cc-114">Elements and attributes</span></span>

<span data-ttu-id="e24cc-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="e24cc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e24cc-116">父元素</span><span class="sxs-lookup"><span data-stu-id="e24cc-116">Parent elements</span></span>

|<span data-ttu-id="e24cc-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="e24cc-117">**Element**</span></span>|<span data-ttu-id="e24cc-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="e24cc-118">**Type**</span></span>|<span data-ttu-id="e24cc-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e24cc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e24cc-120">Row 元素 （geometry)</span><span class="sxs-lookup"><span data-stu-id="e24cc-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e24cc-121">EllipticalArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="e24cc-121">EllipticalArcTo_Type</span></span>](ellipticalarcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e24cc-122">包含 x 坐标或 y 坐标的椭圆弧终结点的 x 坐标或 y 坐标控件的 points 弧形，夹角从 x 轴到椭圆的长轴或比椭圆的主要和次要刻度轴上。</span><span class="sxs-lookup"><span data-stu-id="e24cc-122">Contains x- or y-coordinates of an elliptical arc's endpoint, x- or y-coordinates of the control points on the arc, angle from the x-axis to the ellipse's major axis, or ratio between the ellipse's major and minor axes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e24cc-123">子元素</span><span class="sxs-lookup"><span data-stu-id="e24cc-123">Child elements</span></span>

|<span data-ttu-id="e24cc-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="e24cc-124">**Element**</span></span>|<span data-ttu-id="e24cc-125">**类型**</span><span class="sxs-lookup"><span data-stu-id="e24cc-125">**Type**</span></span>|<span data-ttu-id="e24cc-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="e24cc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e24cc-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e24cc-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e24cc-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e24cc-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e24cc-129">指定在绘图页上的引用。</span><span class="sxs-lookup"><span data-stu-id="e24cc-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e24cc-130">Attributes</span><span class="sxs-lookup"><span data-stu-id="e24cc-130">Attributes</span></span>

|<span data-ttu-id="e24cc-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="e24cc-131">**Attribute**</span></span>|<span data-ttu-id="e24cc-132">**类型**</span><span class="sxs-lookup"><span data-stu-id="e24cc-132">**Type**</span></span>|<span data-ttu-id="e24cc-133">**必需**</span><span class="sxs-lookup"><span data-stu-id="e24cc-133">**Required**</span></span>|<span data-ttu-id="e24cc-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="e24cc-134">**Description**</span></span>|<span data-ttu-id="e24cc-135">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="e24cc-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e24cc-136">E</span><span class="sxs-lookup"><span data-stu-id="e24cc-136">E</span></span>  <br/> |<span data-ttu-id="e24cc-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e24cc-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e24cc-138">可选</span><span class="sxs-lookup"><span data-stu-id="e24cc-138">optional</span></span>  <br/> |<span data-ttu-id="e24cc-139">指示该公式计算为错误。</span><span class="sxs-lookup"><span data-stu-id="e24cc-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e24cc-140">**E**的值是当前值 （错误消息字符串）;**V**属性的值是最后一个有效的值。</span><span class="sxs-lookup"><span data-stu-id="e24cc-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e24cc-141">错误消息字符串。</span><span class="sxs-lookup"><span data-stu-id="e24cc-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e24cc-142">F</span><span class="sxs-lookup"><span data-stu-id="e24cc-142">F</span></span>  <br/> |<span data-ttu-id="e24cc-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e24cc-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e24cc-144">可选</span><span class="sxs-lookup"><span data-stu-id="e24cc-144">optional</span></span>  <br/> | <span data-ttu-id="e24cc-145">代表元素的公式。</span><span class="sxs-lookup"><span data-stu-id="e24cc-145">Represents the element's formula.</span></span> <span data-ttu-id="e24cc-146">此属性可以包含以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="e24cc-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e24cc-147">（某些公式） 如果公式本地存在</span><span class="sxs-lookup"><span data-stu-id="e24cc-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e24cc-148">`No Formula`如果本地删除或阻止公式</span><span class="sxs-lookup"><span data-stu-id="e24cc-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e24cc-149">`Inh`如果继承的公式。</span><span class="sxs-lookup"><span data-stu-id="e24cc-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e24cc-150">公式。</span><span class="sxs-lookup"><span data-stu-id="e24cc-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e24cc-151">N</span><span class="sxs-lookup"><span data-stu-id="e24cc-151">N</span></span>  <br/> |<span data-ttu-id="e24cc-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e24cc-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e24cc-153">必需</span><span class="sxs-lookup"><span data-stu-id="e24cc-153">required</span></span>  <br/> |<span data-ttu-id="e24cc-154">表示的 ShapeSheet 单元格的名称。</span><span class="sxs-lookup"><span data-stu-id="e24cc-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e24cc-155">ShapeSheet 单元格的名称。</span><span class="sxs-lookup"><span data-stu-id="e24cc-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e24cc-156">请参阅下面的备注部分。</span><span class="sxs-lookup"><span data-stu-id="e24cc-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e24cc-157">U</span><span class="sxs-lookup"><span data-stu-id="e24cc-157">U</span></span>  <br/> |<span data-ttu-id="e24cc-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e24cc-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e24cc-159">可选</span><span class="sxs-lookup"><span data-stu-id="e24cc-159">optional</span></span>  <br/> |<span data-ttu-id="e24cc-160">代表单位默认值是度量的 DL。</span><span class="sxs-lookup"><span data-stu-id="e24cc-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e24cc-161">单元格的单位。</span><span class="sxs-lookup"><span data-stu-id="e24cc-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e24cc-162">V</span><span class="sxs-lookup"><span data-stu-id="e24cc-162">V</span></span>  <br/> |<span data-ttu-id="e24cc-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e24cc-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e24cc-164">可选</span><span class="sxs-lookup"><span data-stu-id="e24cc-164">optional</span></span>  <br/> |<span data-ttu-id="e24cc-165">代表单元格的值。</span><span class="sxs-lookup"><span data-stu-id="e24cc-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e24cc-166">ShapeSheet 单元格的值。</span><span class="sxs-lookup"><span data-stu-id="e24cc-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e24cc-167">说明</span><span class="sxs-lookup"><span data-stu-id="e24cc-167">Remarks</span></span>

<span data-ttu-id="e24cc-168">此**单元格**元素的**N**属性必须为一组有限的对应于 ShapeSheet 单元格的值之一。</span><span class="sxs-lookup"><span data-stu-id="e24cc-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e24cc-169">请参阅下表为确定允许此**单元格**元素的**N**属性的值。</span><span class="sxs-lookup"><span data-stu-id="e24cc-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e24cc-170">**值**</span><span class="sxs-lookup"><span data-stu-id="e24cc-170">**Value**</span></span>|<span data-ttu-id="e24cc-171">**说明**</span><span class="sxs-lookup"><span data-stu-id="e24cc-171">**Description**</span></span>|<span data-ttu-id="e24cc-172">**更多信息**</span><span class="sxs-lookup"><span data-stu-id="e24cc-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e24cc-173">X</span><span class="sxs-lookup"><span data-stu-id="e24cc-173">X</span></span>  <br/> |<span data-ttu-id="e24cc-174">弧形上的终顶点的 x 坐标。</span><span class="sxs-lookup"><span data-stu-id="e24cc-174">The x-coordinate of the ending vertex on an arc.</span></span>  <br/> |[<span data-ttu-id="e24cc-175">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-175">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e24cc-176">Y</span><span class="sxs-lookup"><span data-stu-id="e24cc-176">Y</span></span>  <br/> |<span data-ttu-id="e24cc-177">弧形上的终顶点的 y 坐标。</span><span class="sxs-lookup"><span data-stu-id="e24cc-177">The y-coordinate of the ending vertex on an arc.</span></span>  <br/> |[<span data-ttu-id="e24cc-178">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-178">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e24cc-179">A</span><span class="sxs-lookup"><span data-stu-id="e24cc-179">A</span></span>  <br/> |<span data-ttu-id="e24cc-180">弧形的控制点（弧形上的一个点）的 x 坐标。控制点最好位于弧形的始顶点和终顶点的中间附近。否则，弧形可能要变得极大才能穿过该控制点，因而结果将难以预料。</span><span class="sxs-lookup"><span data-stu-id="e24cc-180">The x-coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |[<span data-ttu-id="e24cc-181">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-181">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e24cc-182">B</span><span class="sxs-lookup"><span data-stu-id="e24cc-182">B</span></span>  <br/> |<span data-ttu-id="e24cc-183">弧形的控制点的 y 坐标。</span><span class="sxs-lookup"><span data-stu-id="e24cc-183">The y-coordinate of an arc's control point.</span></span>  <br/> |[<span data-ttu-id="e24cc-184">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-184">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e24cc-185">C</span><span class="sxs-lookup"><span data-stu-id="e24cc-185">C</span></span>  <br/> |<span data-ttu-id="e24cc-186">弧形的长轴相对于其父形状的 x 轴的角度。</span><span class="sxs-lookup"><span data-stu-id="e24cc-186">The angle of an arc's major axis relative to the x-axis of its parent shape.</span></span>  <br/> |[<span data-ttu-id="e24cc-187">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-187">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e24cc-188">D</span><span class="sxs-lookup"><span data-stu-id="e24cc-188">D</span></span>  <br/> |<span data-ttu-id="e24cc-p104">弧形的长短轴之比。尽管每一词都有其本义，但在此处“长”轴却并不一定大于“短”轴，所以此比值也就不一定大于 1。如果将此单元格设置为小于等于 0 或大于 1000 的值，可能导致无法预料的结果。</span><span class="sxs-lookup"><span data-stu-id="e24cc-p104">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |[<span data-ttu-id="e24cc-192">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e24cc-192">EllipticalArcTo Row (Geometry Section)</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |
   
