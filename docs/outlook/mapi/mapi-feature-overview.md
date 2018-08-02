---
title: MAPI 功能概述
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 上次修改时间： 2011 年 7 月 23 日
ms.openlocfilehash: 1ff3677a2bbc8ca54e5bc96ae1e873e3efd3c6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776225"
---
# <a name="mapi-feature-overview"></a><span data-ttu-id="b1efa-103">MAPI 功能概述</span><span class="sxs-lookup"><span data-stu-id="b1efa-103">MAPI Feature Overview</span></span>
 
<span data-ttu-id="b1efa-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b1efa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1efa-105">MAPI 有几个重要功能，使其提供的开发人员使用并以无缝方式使用不同邮件系统以一致方式。</span><span class="sxs-lookup"><span data-stu-id="b1efa-105">MAPI has several key features that enable it to provide a consistent way for developers to work with and use different messaging systems in a seamless fashion.</span></span> <span data-ttu-id="b1efa-106">这些功能包括一款全面和打开编程接口，并支持的行业标准。</span><span class="sxs-lookup"><span data-stu-id="b1efa-106">These features include a comprehensive and open programming interface, and support for industry standards.</span></span> 
  
<span data-ttu-id="b1efa-107">由于 MAPI 是开放的编程接口，它使用户能够添加任何必要的自定义现在和未来的泛型方式提供服务。</span><span class="sxs-lookup"><span data-stu-id="b1efa-107">Because MAPI is an open programming interface, it provides services in a generic way, enabling users to add any necessary customization now and in the future.</span></span> <span data-ttu-id="b1efa-108">MAPI 编程接口满足了具有不同的消息需要，如需要只发送文档的能力的字处理应用程序或工作组需要的应用程序共享的能力的客户端应用程序的要求和存储不同类型的数据。</span><span class="sxs-lookup"><span data-stu-id="b1efa-108">The MAPI programming interface fulfills the requirements of client applications with diverse messaging needs, such as a word processing application that requires only the ability to send documents, or a workgroup application that requires the ability to share and store different types of data.</span></span> <span data-ttu-id="b1efa-109">实际上，任何应用程序需要 exchange 或信息存储在特定格式可以受益从 MAPI 编程接口。</span><span class="sxs-lookup"><span data-stu-id="b1efa-109">In fact, any application that needs to either exchange or store information in a particular format can benefit from the MAPI programming interface.</span></span> <span data-ttu-id="b1efa-110">任何服务提供商可以使用接口公开其邮件系统的独特功能选择向应用程序用户提供最大好处这些功能。</span><span class="sxs-lookup"><span data-stu-id="b1efa-110">Any service provider can use the interface to expose the unique features of its messaging system, selecting those features that provide the most benefit to application users.</span></span>
  
<span data-ttu-id="b1efa-111">MAPI 提供了用于前端消息客户端应用程序的编程接口和后端服务提供商使用的编程接口之间分隔。</span><span class="sxs-lookup"><span data-stu-id="b1efa-111">MAPI provides separation between the programming interface used by the front-end messaging client applications and the programming interface used by the back-end service providers.</span></span> <span data-ttu-id="b1efa-112">从服务提供商将客户端界面使单个应用程序以使用多个邮件系统和多个应用程序使用单个服务提供商。</span><span class="sxs-lookup"><span data-stu-id="b1efa-112">Separating the client interface from the service provider enables a single application to use multiple messaging systems and multiple applications to use a single service provider.</span></span> <span data-ttu-id="b1efa-113">常见的 Microsoft 基于 Windows 的用户界面适用于每个组件。</span><span class="sxs-lookup"><span data-stu-id="b1efa-113">Every component works with a common Microsoft Windows-based user interface.</span></span> <span data-ttu-id="b1efa-114">这是用户很有用。</span><span class="sxs-lookup"><span data-stu-id="b1efa-114">This is a great benefit to users.</span></span> <span data-ttu-id="b1efa-115">用户可以从多种系统，具体取决于在任何时候，其需求选择，并可以使用一致每个选定的系统，从而提供从特定的邮件系统，则返回 true 独立性。</span><span class="sxs-lookup"><span data-stu-id="b1efa-115">Users can select from a variety of systems, depending on their needs at any one time, and can work consistently with each selected system, thereby providing true independence from specific messaging systems.</span></span> 
  
<span data-ttu-id="b1efa-116">例如，单个消息客户端应用程序可以接收来自传真、 语音邮件和 RSS 源的邮件。</span><span class="sxs-lookup"><span data-stu-id="b1efa-116">For example, a single messaging client application can receive messages from a fax, voice mail, and an RSS feed.</span></span> <span data-ttu-id="b1efa-117">从所有这些系统的消息可以放在一个位置或通用收件箱，在到达中。</span><span class="sxs-lookup"><span data-stu-id="b1efa-117">Messages from all of these systems can be placed in a single location, or universal Inbox, on arrival.</span></span> <span data-ttu-id="b1efa-118">具有单个应用程序处理所有这些系统可以降低开发、 用户培训和系统管理的成本。</span><span class="sxs-lookup"><span data-stu-id="b1efa-118">Having a single application handle all of these systems lessens the cost of development, user training, and system administration.</span></span> 
  
<span data-ttu-id="b1efa-119">将提供程序接口中的客户端界面中删除任何置于邮件系统，反之亦然的应用程序的编程依赖项。</span><span class="sxs-lookup"><span data-stu-id="b1efa-119">Separating the client interface from the provider interface removes any programming dependencies placed on the application by the messaging system and vice versa.</span></span> <span data-ttu-id="b1efa-120">客户端应用程序和服务提供商的开发人员编写代码以一组标准的 MAPI 功能，而不是多种多样的特定于应用程序或消息系统特定功能。</span><span class="sxs-lookup"><span data-stu-id="b1efa-120">Developers of client applications and service providers write code to a standard set of MAPI features, rather than a diverse set of application-specific or messaging system-specific features.</span></span> <span data-ttu-id="b1efa-121">开发人员关注仅及其组件，它是客户端或服务提供商，是否 MAPI 处理其余，从而减少了开发时间和成本。</span><span class="sxs-lookup"><span data-stu-id="b1efa-121">Developers focus only on their component, whether it is a client or service provider, and MAPI handles the rest, reducing development time and costs.</span></span>
  
<span data-ttu-id="b1efa-122">MAPI 编程接口提供了一组全面的功能。</span><span class="sxs-lookup"><span data-stu-id="b1efa-122">The MAPI programming interface provides a comprehensive set of features.</span></span> <span data-ttu-id="b1efa-123">MAPI 针对在工作组应用程序的强大新市场 — 与传真、 年 12 月一-在-1、 语音邮件和公共 communications 服务，例如在 & T Easylink 服务、 CompuServe 和 MCI 如下不同邮件系统通信的应用程序邮件。</span><span class="sxs-lookup"><span data-stu-id="b1efa-123">MAPI is aimed at the powerful new market of workgroup applications — applications that communicate with such different messaging systems as fax, DEC All-In-1, voice mail, and public communications services such as AT&T Easylink Services, CompuServe, and MCI MAIL.</span></span> <span data-ttu-id="b1efa-124">MAPI 界面使服务提供商可供所有这些系统。</span><span class="sxs-lookup"><span data-stu-id="b1efa-124">The MAPI interface enables service providers to be made available for all of these systems.</span></span> 
  
<span data-ttu-id="b1efa-125">MAPI 兼容的对象是在窗体上类似于组件对象模型 (COM) 对象。</span><span class="sxs-lookup"><span data-stu-id="b1efa-125">MAPI-compliant objects are similar in form to Component Object Model (COM) objects.</span></span> <span data-ttu-id="b1efa-126">COM 对象实现的一组到一个或多个接口所属的方法或相关如何对象的行为和操作 COM 中定义的函数集</span><span class="sxs-lookup"><span data-stu-id="b1efa-126">COM objects implement a set of methods that belong to one or more interfaces, or collections of related functions that define how objects behave and operate in COM.</span></span> <span data-ttu-id="b1efa-127">用户只能通过指向这些接口访问 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="b1efa-127">Users access COM objects only through pointers to these interfaces.</span></span>
  
<span data-ttu-id="b1efa-128">MAPI 提供了通过此类作为 SMTP 和 X.400 的行业标准的跨平台支持。</span><span class="sxs-lookup"><span data-stu-id="b1efa-128">MAPI provides cross-platform support through such industry standards as SMTP and X.400.</span></span> <span data-ttu-id="b1efa-129">您可以运行在 Windows 7、 Windows Vista、 Windows Server 2008、 Windows Server 2003 和 Windows XP 上的 MAPI 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b1efa-129">You can run MAPI applications on Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003, and Windows XP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1efa-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b1efa-130">See also</span></span>

- [<span data-ttu-id="b1efa-131">MAPI 功能和体系结构</span><span class="sxs-lookup"><span data-stu-id="b1efa-131">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)
