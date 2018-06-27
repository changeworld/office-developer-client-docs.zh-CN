---
title: PidTagReportEntryId 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778207"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="0985e-103">PidTagReportEntryId 规范属性</span><span class="sxs-lookup"><span data-stu-id="0985e-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0985e-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="0985e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0985e-105">包含的项标识符的应接收此消息的报告的收件人。</span><span class="sxs-lookup"><span data-stu-id="0985e-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0985e-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="0985e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0985e-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0985e-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0985e-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="0985e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0985e-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="0985e-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="0985e-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="0985e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0985e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0985e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0985e-112">区域：</span><span class="sxs-lookup"><span data-stu-id="0985e-112">Area:</span></span>  <br/> |<span data-ttu-id="0985e-113">MAPI 信封</span><span class="sxs-lookup"><span data-stu-id="0985e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0985e-114">备注</span><span class="sxs-lookup"><span data-stu-id="0985e-114">Remarks</span></span>

<span data-ttu-id="0985e-115">此属性是一个发件人已委派接收此消息生成任何报告的收件人的地址属性。</span><span class="sxs-lookup"><span data-stu-id="0985e-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="0985e-116">必须将报表路由到另一个用户的客户端应用程序应在消息提交时设置此属性。</span><span class="sxs-lookup"><span data-stu-id="0985e-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="0985e-117">它未设置，如果报告发送到邮件发件人。</span><span class="sxs-lookup"><span data-stu-id="0985e-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0985e-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="0985e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0985e-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="0985e-119">Protocol specifications</span></span>

<span data-ttu-id="0985e-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0985e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0985e-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="0985e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0985e-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0985e-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0985e-123">指定的属性和电子邮件中允许的操作。</span><span class="sxs-lookup"><span data-stu-id="0985e-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0985e-124">头文件</span><span class="sxs-lookup"><span data-stu-id="0985e-124">Header files</span></span>

<span data-ttu-id="0985e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0985e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0985e-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="0985e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0985e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0985e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0985e-128">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="0985e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0985e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0985e-129">See also</span></span>



[<span data-ttu-id="0985e-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="0985e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0985e-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="0985e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0985e-132">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="0985e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0985e-133">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="0985e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
