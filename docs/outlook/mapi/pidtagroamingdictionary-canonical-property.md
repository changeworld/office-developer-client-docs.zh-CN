---
title: PidTagRoamingDictionary 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778249"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="d11ca-103">PidTagRoamingDictionary 规范属性</span><span class="sxs-lookup"><span data-stu-id="d11ca-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="d11ca-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="d11ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d11ca-105">包含描述漫游字典 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="d11ca-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d11ca-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="d11ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d11ca-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="d11ca-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="d11ca-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="d11ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d11ca-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="d11ca-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="d11ca-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="d11ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="d11ca-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d11ca-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d11ca-112">区域：</span><span class="sxs-lookup"><span data-stu-id="d11ca-112">Area:</span></span>  <br/> |<span data-ttu-id="d11ca-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="d11ca-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d11ca-114">备注</span><span class="sxs-lookup"><span data-stu-id="d11ca-114">Remarks</span></span>

<span data-ttu-id="d11ca-115">此属性包含一个使用 UTF8 编码的 UNICODE XML 文档。</span><span class="sxs-lookup"><span data-stu-id="d11ca-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="d11ca-116">具有词典流一条消息必须设置此属性与下面的架构：</span><span class="sxs-lookup"><span data-stu-id="d11ca-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="d11ca-117">以下是存储在配置数据邮件此属性的示例 XML 文档：</span><span class="sxs-lookup"><span data-stu-id="d11ca-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="d11ca-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="d11ca-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d11ca-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="d11ca-119">Protocol specifications</span></span>

<span data-ttu-id="d11ca-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d11ca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d11ca-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="d11ca-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d11ca-122">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d11ca-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d11ca-123">指定的位置和客户端和服务器配置数据，如共享的类别列表和工作时间的属性。</span><span class="sxs-lookup"><span data-stu-id="d11ca-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d11ca-124">头文件</span><span class="sxs-lookup"><span data-stu-id="d11ca-124">Header files</span></span>

<span data-ttu-id="d11ca-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d11ca-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d11ca-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="d11ca-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d11ca-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d11ca-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d11ca-128">包含列为相关属性的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="d11ca-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d11ca-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d11ca-129">See also</span></span>



[<span data-ttu-id="d11ca-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="d11ca-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d11ca-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="d11ca-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d11ca-132">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="d11ca-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d11ca-133">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="d11ca-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
