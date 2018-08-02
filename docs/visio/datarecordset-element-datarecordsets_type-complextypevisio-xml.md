---
title: DataRecordSet 元素 （DataRecordSets_Type 复杂类型） (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: 在 Microsoft Visio 中对从数据库中查询的数据进行存储、格式设置、刷新和公开操作。
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780039"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="f847b-103">DataRecordSet 元素 （DataRecordSets_Type 复杂类型） (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f847b-103">DataRecordSet element (DataRecordSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f847b-104">在 Microsoft Visio 中对从数据库中查询的数据进行存储、格式设置、刷新和公开操作。</span><span class="sxs-lookup"><span data-stu-id="f847b-104">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f847b-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="f847b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f847b-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="f847b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f847b-107">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-107">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f847b-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="f847b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f847b-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="f847b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f847b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f847b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f847b-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="f847b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f847b-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="f847b-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f847b-113">定义</span><span class="sxs-lookup"><span data-stu-id="f847b-113">Definition</span></span>

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f847b-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="f847b-114">Elements and attributes</span></span>

<span data-ttu-id="f847b-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="f847b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f847b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="f847b-116">Parent elements</span></span>

|<span data-ttu-id="f847b-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="f847b-117">**Element**</span></span>|<span data-ttu-id="f847b-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="f847b-118">**Type**</span></span>|<span data-ttu-id="f847b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f847b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f847b-120">DataRecordSets</span><span class="sxs-lookup"><span data-stu-id="f847b-120">DataRecordSets</span></span>](datarecordsets-elementvisio-xml.md) <br/> |[<span data-ttu-id="f847b-121">DataRecordSets_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-121">DataRecordSets_Type</span></span>](datarecordsets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-122">包含文档中的所有**数据记录集**元素。</span><span class="sxs-lookup"><span data-stu-id="f847b-122">Contains all the **DataRecordset** elements in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f847b-123">子元素</span><span class="sxs-lookup"><span data-stu-id="f847b-123">Child elements</span></span>

|<span data-ttu-id="f847b-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="f847b-124">**Element**</span></span>|<span data-ttu-id="f847b-125">**类型**</span><span class="sxs-lookup"><span data-stu-id="f847b-125">**Type**</span></span>|<span data-ttu-id="f847b-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="f847b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f847b-127">ADOData</span><span class="sxs-lookup"><span data-stu-id="f847b-127">ADOData</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-128">ADOData_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-128">ADOData_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-129">包含符合 ADO 记录集的 ADO 经典 XML 架构，并且描述的数据记录集中的数据的 XML。</span><span class="sxs-lookup"><span data-stu-id="f847b-129">Contains XML that conforms to the ADO classic XML schema for an ADO recordset and that describes the data in the data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f847b-130">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="f847b-130">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-131">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-131">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-132">定义一个将形状数据项目从上次成功自动链接执行的操作在用户界面中将父**DataRecordset**元素中的列进行比较的规则。</span><span class="sxs-lookup"><span data-stu-id="f847b-132">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span>  <br/> |
|[<span data-ttu-id="f847b-133">DataColumn</span><span class="sxs-lookup"><span data-stu-id="f847b-133">DataColumn</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-134">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-134">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-135">定义在 Visio 用户界面中的**外部数据**窗口中的数据列的显示方式，并通过定义其数据类型和格式限定列中的数据。</span><span class="sxs-lookup"><span data-stu-id="f847b-135">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
|[<span data-ttu-id="f847b-136">DataColumns</span><span class="sxs-lookup"><span data-stu-id="f847b-136">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-137">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-137">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-138">包含数据记录集中的所有**DataColumn**元素。</span><span class="sxs-lookup"><span data-stu-id="f847b-138">Contains all the **DataColumn** elements in a data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f847b-139">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f847b-139">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-140">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-140">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-141">标识数据记录集中的一个或多个主键列。</span><span class="sxs-lookup"><span data-stu-id="f847b-141">Identifies one or more primary-key columns in the data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f847b-142">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="f847b-142">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-143">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-143">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-144">指示链接到形状的数据记录集刷新后存在冲突的数据记录集中的行。</span><span class="sxs-lookup"><span data-stu-id="f847b-144">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>  <br/> |
|[<span data-ttu-id="f847b-145">RowMap</span><span class="sxs-lookup"><span data-stu-id="f847b-145">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f847b-146">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="f847b-146">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f847b-147">映射到形状的数据记录集行。</span><span class="sxs-lookup"><span data-stu-id="f847b-147">Maps a data-recordset row to a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f847b-148">Attributes</span><span class="sxs-lookup"><span data-stu-id="f847b-148">Attributes</span></span>

|<span data-ttu-id="f847b-149">**属性**</span><span class="sxs-lookup"><span data-stu-id="f847b-149">**Attribute**</span></span>|<span data-ttu-id="f847b-150">**类型**</span><span class="sxs-lookup"><span data-stu-id="f847b-150">**Type**</span></span>|<span data-ttu-id="f847b-151">**必需**</span><span class="sxs-lookup"><span data-stu-id="f847b-151">**Required**</span></span>|<span data-ttu-id="f847b-152">**说明**</span><span class="sxs-lookup"><span data-stu-id="f847b-152">**Description**</span></span>|<span data-ttu-id="f847b-153">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="f847b-153">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f847b-154">校验和</span><span class="sxs-lookup"><span data-stu-id="f847b-154">Checksum</span></span>  <br/> |<span data-ttu-id="f847b-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-156">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-156">optional</span></span>  <br/> |<span data-ttu-id="f847b-157">一个校验和值由 Visio，生成和基于数据记录集属性。</span><span class="sxs-lookup"><span data-stu-id="f847b-157">A checksum value, generated by Visio, and based on data-recordset properties.</span></span> <span data-ttu-id="f847b-158">将此 attirbute 设置为 0;Visio 将此值在运行时进行重新计算。</span><span class="sxs-lookup"><span data-stu-id="f847b-158">Set this attirbute to 0; Visio recalculates this value at runtime.</span></span>  <br/> |<span data-ttu-id="f847b-159">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-160">命令</span><span class="sxs-lookup"><span data-stu-id="f847b-160">Command</span></span>  <br/> |<span data-ttu-id="f847b-161">xsd: string</span><span class="sxs-lookup"><span data-stu-id="f847b-161">xsd:string</span></span>  <br/> |<span data-ttu-id="f847b-162">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-162">optional</span></span>  <br/> |<span data-ttu-id="f847b-163">从数据源查询数据使用的命令字符串。</span><span class="sxs-lookup"><span data-stu-id="f847b-163">The command string used to query data from the data source.</span></span>  <br/> |<span data-ttu-id="f847b-164">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-164">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f847b-165">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="f847b-165">ConnectionID</span></span>  <br/> |<span data-ttu-id="f847b-166">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-166">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-167">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-167">optional</span></span>  <br/> |<span data-ttu-id="f847b-168">关联的**DataConnection**对象的连接 ID。</span><span class="sxs-lookup"><span data-stu-id="f847b-168">The connection ID for the associated **DataConnection** object.</span></span> <span data-ttu-id="f847b-169">不存在的 XML 数据源。</span><span class="sxs-lookup"><span data-stu-id="f847b-169">Does not exist for XML data sources.</span></span>  <br/> |<span data-ttu-id="f847b-170">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-170">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-171">ID</span><span class="sxs-lookup"><span data-stu-id="f847b-171">ID</span></span>  <br/> |<span data-ttu-id="f847b-172">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-172">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-173">必需</span><span class="sxs-lookup"><span data-stu-id="f847b-173">required</span></span>  <br/> |<span data-ttu-id="f847b-174">数据记录集 ID，唯一的文档中。</span><span class="sxs-lookup"><span data-stu-id="f847b-174">The data recordset ID, unique within the document.</span></span>  <br/> |<span data-ttu-id="f847b-175">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-176">名称</span><span class="sxs-lookup"><span data-stu-id="f847b-176">Name</span></span>  <br/> |<span data-ttu-id="f847b-177">xsd: string</span><span class="sxs-lookup"><span data-stu-id="f847b-177">xsd:string</span></span>  <br/> |<span data-ttu-id="f847b-178">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-178">optional</span></span>  <br/> |<span data-ttu-id="f847b-179">显示 （或"友好"） 的数据记录集的名称。</span><span class="sxs-lookup"><span data-stu-id="f847b-179">The display (or "friendly") name of the data recordset.</span></span>  <br/> |<span data-ttu-id="f847b-180">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-180">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f847b-181">NextRowID</span><span class="sxs-lookup"><span data-stu-id="f847b-181">NextRowID</span></span>  <br/> |<span data-ttu-id="f847b-182">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-182">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-183">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-183">optional</span></span>  <br/> |<span data-ttu-id="f847b-184">下一个可用 Visio 行 id。</span><span class="sxs-lookup"><span data-stu-id="f847b-184">The next available Visio row ID.</span></span>  <br/> |<span data-ttu-id="f847b-185">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-185">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-186">选项</span><span class="sxs-lookup"><span data-stu-id="f847b-186">Options</span></span>  <br/> |<span data-ttu-id="f847b-187">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-187">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-188">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-188">optional</span></span>  <br/> |<span data-ttu-id="f847b-189">要应用于的数据记录集的选项。</span><span class="sxs-lookup"><span data-stu-id="f847b-189">Options to apply to the data recordset.</span></span> <span data-ttu-id="f847b-190">可能的值可以是任意组合的一个或多个下表中所示。</span><span class="sxs-lookup"><span data-stu-id="f847b-190">Possible values can be any combination of one or more of those shown in the following table.</span></span>  <br/> |<span data-ttu-id="f847b-191">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-191">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-192">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="f847b-192">RefreshInterval</span></span>  <br/> |<span data-ttu-id="f847b-193">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-193">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-194">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-194">optional</span></span>  <br/> |<span data-ttu-id="f847b-195">频率 （以分钟为单位） Visio 自动刷新数据记录集。</span><span class="sxs-lookup"><span data-stu-id="f847b-195">How often (in minutes) Visio refreshes the data recordset automatically.</span></span> <span data-ttu-id="f847b-196">该值必须是 1 或更大。</span><span class="sxs-lookup"><span data-stu-id="f847b-196">This value must be 1 or larger.</span></span>  <br/> |<span data-ttu-id="f847b-197">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-197">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-198">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="f847b-198">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="f847b-199">化</span><span class="sxs-lookup"><span data-stu-id="f847b-199">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f847b-200">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-200">optional</span></span>  <br/> |<span data-ttu-id="f847b-201">是否应禁用数据调节用户界面。</span><span class="sxs-lookup"><span data-stu-id="f847b-201">Whether the data-reconciliation user interface should be disabled.</span></span> <span data-ttu-id="f847b-202">True (1) 若要禁用的用户界面 (UI)。</span><span class="sxs-lookup"><span data-stu-id="f847b-202">True (1) to disable the user interface (UI).</span></span> <span data-ttu-id="f847b-203">False (0)，以启用 UI。</span><span class="sxs-lookup"><span data-stu-id="f847b-203">False (0) to enable the UI.</span></span>  <br/> |<span data-ttu-id="f847b-204">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-204">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f847b-205">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="f847b-205">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="f847b-206">化</span><span class="sxs-lookup"><span data-stu-id="f847b-206">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f847b-207">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-207">optional</span></span>  <br/> |<span data-ttu-id="f847b-208">刷新数据记录集时是否覆盖用户更改形状中的形状数据项目链接到数据。</span><span class="sxs-lookup"><span data-stu-id="f847b-208">Whether to overwrite user changes to shape data items in shapes linked to data when the data recordset is refreshed.</span></span>  <br/> |<span data-ttu-id="f847b-209">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-209">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f847b-210">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="f847b-210">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="f847b-211">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f847b-211">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f847b-212">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-212">optional</span></span>  <br/> |<span data-ttu-id="f847b-213">定义形状数据链接复制或剪切形状时的处理方式。</span><span class="sxs-lookup"><span data-stu-id="f847b-213">Defines how shape-data links are treated when shapes are copied or cut.</span></span> <span data-ttu-id="f847b-214">若要替换现有的链接的目标形状中的 1。</span><span class="sxs-lookup"><span data-stu-id="f847b-214">1 to replace existing links in the target shape.</span></span> <span data-ttu-id="f847b-215">维护现有的链接的目标形状中的 0。</span><span class="sxs-lookup"><span data-stu-id="f847b-215">0 to maintain existing links in the target shape.</span></span>  <br/> |<span data-ttu-id="f847b-216">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-216">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f847b-217">RowOrder</span><span class="sxs-lookup"><span data-stu-id="f847b-217">RowOrder</span></span>  <br/> |<span data-ttu-id="f847b-218">化</span><span class="sxs-lookup"><span data-stu-id="f847b-218">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f847b-219">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-219">optional</span></span>  <br/> |<span data-ttu-id="f847b-220">是否为主键使用中的数据记录集的行的顺序。</span><span class="sxs-lookup"><span data-stu-id="f847b-220">Whether to use the order of the rows in the data recordset as the primary key.</span></span> <span data-ttu-id="f847b-221">如果行 Id 由行顺序，则 true (1)。</span><span class="sxs-lookup"><span data-stu-id="f847b-221">True (1) if row IDs are determined by row order.</span></span> <span data-ttu-id="f847b-222">False (0)，如果行 Id 由中的数据记录集主键列的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-222">False (0) if row IDs are determined by values in the primary key column(s) of the data recordset.</span></span>  <br/> |<span data-ttu-id="f847b-223">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-223">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f847b-224">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="f847b-224">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="f847b-225">化</span><span class="sxs-lookup"><span data-stu-id="f847b-225">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="f847b-226">可选</span><span class="sxs-lookup"><span data-stu-id="f847b-226">optional</span></span>  <br/> |<span data-ttu-id="f847b-227">日期和时间上次刷新数据记录集。</span><span class="sxs-lookup"><span data-stu-id="f847b-227">The date and time the data recordset was last refreshed.</span></span>  <br/> |<span data-ttu-id="f847b-228">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="f847b-228">Values of the xsd:dateTime type.</span></span>  <br/> |
   
