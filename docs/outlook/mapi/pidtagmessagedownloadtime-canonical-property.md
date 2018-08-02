---
title: PidTagMessageDownloadTime 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777849"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="15239-103">PidTagMessageDownloadTime 规范属性</span><span class="sxs-lookup"><span data-stu-id="15239-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="15239-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="15239-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15239-105">包含要从远程服务器的邮件下载到本地邮件存储的估计的时间。</span><span class="sxs-lookup"><span data-stu-id="15239-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15239-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="15239-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15239-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="15239-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="15239-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="15239-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15239-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="15239-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="15239-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="15239-110">Data type:</span></span>  <br/> |<span data-ttu-id="15239-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15239-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15239-112">区域：</span><span class="sxs-lookup"><span data-stu-id="15239-112">Area:</span></span>  <br/> |<span data-ttu-id="15239-113">常规消息</span><span class="sxs-lookup"><span data-stu-id="15239-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15239-114">说明</span><span class="sxs-lookup"><span data-stu-id="15239-114">Remarks</span></span>

<span data-ttu-id="15239-115">此属性以秒为单位表示并代表时间也很远程传输提供程序从其当前位置的给定的邮件下载到的消息存储本地到客户端查看标头文件夹的最佳估计值。</span><span class="sxs-lookup"><span data-stu-id="15239-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="15239-116">远程传输提供程序通常由**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) 属性的值除以中每秒字节数的 communications 链接的速度计算此属性的值。</span><span class="sxs-lookup"><span data-stu-id="15239-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="15239-117">如果提供程序无法计算下载时间，例如，如果不知道的链接速度，它应提供此列标题文件夹内容表中如**MAPI_E_NO_SUPPORT** **PT_ERROR**值。</span><span class="sxs-lookup"><span data-stu-id="15239-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="15239-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="15239-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="15239-119">头文件</span><span class="sxs-lookup"><span data-stu-id="15239-119">Header files</span></span>

<span data-ttu-id="15239-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15239-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="15239-121">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="15239-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="15239-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15239-122">Mapitags.h</span></span>
  
> <span data-ttu-id="15239-123">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="15239-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15239-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15239-124">See also</span></span>



[<span data-ttu-id="15239-125">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="15239-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15239-126">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="15239-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15239-127">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="15239-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15239-128">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="15239-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
