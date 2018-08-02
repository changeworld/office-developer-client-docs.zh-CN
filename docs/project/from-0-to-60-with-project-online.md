---
title: Project Online 从入门到精通
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 应用程序开发人员可以自定义 Project Online 承载的网站 （SharePoint） 使用独立应用程序和/或项目外接程序。丰富的应用程序是可能的范围从寻址的那些参与一个项目到 PMO 支持功能，如以下任一需求：
ms.openlocfilehash: c50ed12e9f1127f6313a02db4d84a151778e17b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779417"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="4a744-103">Project Online 从入门到精通</span><span class="sxs-lookup"><span data-stu-id="4a744-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="4a744-104">应用程序开发人员可以自定义 Project Online 承载的网站 （SharePoint） 使用独立应用程序和/或项目外接程序。丰富的应用程序是可能的范围从寻址的那些参与一个项目到 PMO 支持功能，如以下任一需求：</span><span class="sxs-lookup"><span data-stu-id="4a744-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="4a744-105">简化考勤卡工作者的数据输入</span><span class="sxs-lookup"><span data-stu-id="4a744-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="4a744-106">高效考勤卡审批的主管</span><span class="sxs-lookup"><span data-stu-id="4a744-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="4a744-107">允许 （采购和状态） 所需的项目的监督</span><span class="sxs-lookup"><span data-stu-id="4a744-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="4a744-108">活动项目的状态/状况检查</span><span class="sxs-lookup"><span data-stu-id="4a744-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="4a744-109">问题报告</span><span class="sxs-lookup"><span data-stu-id="4a744-109">Issues report</span></span>
- <span data-ttu-id="4a744-110">更改管理状态报告</span><span class="sxs-lookup"><span data-stu-id="4a744-110">Change Management Status report</span></span>
    
<span data-ttu-id="4a744-111">Project Online 包括 API 支持以适应以下方案：</span><span class="sxs-lookup"><span data-stu-id="4a744-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="4a744-112">为项目 (SharePoint) 托管外接程序：</span><span class="sxs-lookup"><span data-stu-id="4a744-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="4a744-113">SharePoint Online 中托管的代码 （JavaScript、 HTML、 CSS）</span><span class="sxs-lookup"><span data-stu-id="4a744-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="4a744-114">下载到浏览器并执行针对 SharePoint Online 的资产。</span><span class="sxs-lookup"><span data-stu-id="4a744-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="4a744-115">JavaScript 中的业务逻辑</span><span class="sxs-lookup"><span data-stu-id="4a744-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="4a744-116">访问数据的是在/存储在 Project Online 或 SharePoint 如 （但不限于）：</span><span class="sxs-lookup"><span data-stu-id="4a744-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="4a744-117">自定义域</span><span class="sxs-lookup"><span data-stu-id="4a744-117">Custom fields</span></span>  
  - <span data-ttu-id="4a744-118">列表</span><span class="sxs-lookup"><span data-stu-id="4a744-118">Lists</span></span>
    
- <span data-ttu-id="4a744-119">为项目 (SharePoint) 提供商托管外接程序：</span><span class="sxs-lookup"><span data-stu-id="4a744-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="4a744-120">Project Online 站点的外部网站上的代码</span><span class="sxs-lookup"><span data-stu-id="4a744-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="4a744-121">外部网站，它可以是 （但不限于）：</span><span class="sxs-lookup"><span data-stu-id="4a744-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="4a744-122">其他 SharePoint 网站</span><span class="sxs-lookup"><span data-stu-id="4a744-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="4a744-123">在任何平台上构建的 web 应用程序/服务</span><span class="sxs-lookup"><span data-stu-id="4a744-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="4a744-124">外部网站包含业务逻辑</span><span class="sxs-lookup"><span data-stu-id="4a744-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="4a744-125">将浏览器重定向从 Project Online 到具有访问令牌到 Project Online 的外部网站</span><span class="sxs-lookup"><span data-stu-id="4a744-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="4a744-126">对外部网站可以发出呼叫到 SharePoint 和 Project Online</span><span class="sxs-lookup"><span data-stu-id="4a744-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="4a744-127">对于外部/独立外接程序：</span><span class="sxs-lookup"><span data-stu-id="4a744-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="4a744-128">用户在其设备上执行应用程序</span><span class="sxs-lookup"><span data-stu-id="4a744-128">User executes an application on their device</span></span>
  - <span data-ttu-id="4a744-129">应用程序进行身份验证，并直接调用 Project Online Api</span><span class="sxs-lookup"><span data-stu-id="4a744-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="4a744-130">应用程序类型</span><span class="sxs-lookup"><span data-stu-id="4a744-130">Type of application</span></span>|<span data-ttu-id="4a744-131">API 实现</span><span class="sxs-lookup"><span data-stu-id="4a744-131">API implementation</span></span>|<span data-ttu-id="4a744-132">目标环境</span><span class="sxs-lookup"><span data-stu-id="4a744-132">Target environment</span></span>|<span data-ttu-id="4a744-133">应用程序示例</span><span class="sxs-lookup"><span data-stu-id="4a744-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a744-134">托管项目</span><span class="sxs-lookup"><span data-stu-id="4a744-134">Project hosted</span></span>  <br/> |<span data-ttu-id="4a744-135">JSOM （Java Script 对象模型）</span><span class="sxs-lookup"><span data-stu-id="4a744-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="4a744-136">REST</span><span class="sxs-lookup"><span data-stu-id="4a744-136">REST</span></span>  <br/> |<span data-ttu-id="4a744-137">浏览器</span><span class="sxs-lookup"><span data-stu-id="4a744-137">Browser</span></span>  <br/> |<span data-ttu-id="4a744-138">考勤卡条目</span><span class="sxs-lookup"><span data-stu-id="4a744-138">Timecard entry</span></span>  <br/> <span data-ttu-id="4a744-139">考勤卡审批</span><span class="sxs-lookup"><span data-stu-id="4a744-139">Timecard approval</span></span>  <br/> <span data-ttu-id="4a744-140">项目状态</span><span class="sxs-lookup"><span data-stu-id="4a744-140">Project Status</span></span>  <br/> <span data-ttu-id="4a744-141">问题报告</span><span class="sxs-lookup"><span data-stu-id="4a744-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="4a744-142">项目提供程序承载</span><span class="sxs-lookup"><span data-stu-id="4a744-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="4a744-143">CSOM 客户端库</span><span class="sxs-lookup"><span data-stu-id="4a744-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="4a744-144">Azure 网站/应用程序</span><span class="sxs-lookup"><span data-stu-id="4a744-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="4a744-145">非 Windows 环境 （LAMP 等）</span><span class="sxs-lookup"><span data-stu-id="4a744-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="4a744-146">外部时间表验证程序</span><span class="sxs-lookup"><span data-stu-id="4a744-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="4a744-147">项目导入程序</span><span class="sxs-lookup"><span data-stu-id="4a744-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="4a744-148">外部/独立</span><span class="sxs-lookup"><span data-stu-id="4a744-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="4a744-149">REST</span><span class="sxs-lookup"><span data-stu-id="4a744-149">REST</span></span>  <br/> <span data-ttu-id="4a744-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="4a744-150">CSOM</span></span>  <br/> |<span data-ttu-id="4a744-151">REST-任何平台</span><span class="sxs-lookup"><span data-stu-id="4a744-151">REST - any platform</span></span>  <br/> <span data-ttu-id="4a744-152">CSOM 的任何支持的.NET 平台</span><span class="sxs-lookup"><span data-stu-id="4a744-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="4a744-153">考勤卡条目</span><span class="sxs-lookup"><span data-stu-id="4a744-153">Timecard entry</span></span>  <br/> <span data-ttu-id="4a744-154">向新网站的项目的迁移</span><span class="sxs-lookup"><span data-stu-id="4a744-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="4a744-155">管理状态更改。</span><span class="sxs-lookup"><span data-stu-id="4a744-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="4a744-156">开始开发 for Project Online 中的应用程序需要什么？</span><span class="sxs-lookup"><span data-stu-id="4a744-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="4a744-157">所需的开发 Project Online 的应用程序的常见项的 Project Online 的帐户和测试数据-项目和项目相关的信息，包括分配、 任务、 资源和自定义字段。</span><span class="sxs-lookup"><span data-stu-id="4a744-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="4a744-158">开发环境所需以及，但开发环境具体情况取决于应用程序和应用程序所需的 API 接口的类型。</span><span class="sxs-lookup"><span data-stu-id="4a744-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="4a744-159">下面几节介绍的三个 API 接口的开发需求。</span><span class="sxs-lookup"><span data-stu-id="4a744-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="4a744-160">参考文档描述的所有三个接口，以及实体映射显示对象模型组件之间的关系的情况很常见的对象模型。</span><span class="sxs-lookup"><span data-stu-id="4a744-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="4a744-161">Project 托管外接程序开发环境</span><span class="sxs-lookup"><span data-stu-id="4a744-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="4a744-162">托管加载项是外接程序驻留在服务器上，下载到浏览器中的运行时执行。</span><span class="sxs-lookup"><span data-stu-id="4a744-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="4a744-163">托管加载项可以使用 JSOM 或 REST 接口和 JavaScript 中写入。</span><span class="sxs-lookup"><span data-stu-id="4a744-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="4a744-164">Project Online 的运行时执行提供对 JSOM 库的引用。</span><span class="sxs-lookup"><span data-stu-id="4a744-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="4a744-165">假定开发与在 Windows 平台上，按所需的资源：</span><span class="sxs-lookup"><span data-stu-id="4a744-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="4a744-166">Visual Studio 2015 （首选） 或 Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4a744-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="4a744-167">Visual Studio 的 office 开发工具</span><span class="sxs-lookup"><span data-stu-id="4a744-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="4a744-168">JavaScript 语言</span><span class="sxs-lookup"><span data-stu-id="4a744-168">JavaScript language</span></span>
    
<span data-ttu-id="4a744-169">请访问https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages示例应用程序。</span><span class="sxs-lookup"><span data-stu-id="4a744-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="4a744-170">您可以下载并运行该示例中一些简单的步骤：</span><span class="sxs-lookup"><span data-stu-id="4a744-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="4a744-171">下载并打开示例应用程序</span><span class="sxs-lookup"><span data-stu-id="4a744-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4a744-172">更新属性窗口中的 siteurl 属性</span><span class="sxs-lookup"><span data-stu-id="4a744-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4a744-173">Project Online 检查外接程序和管理访问的 Project Online 主机上的信息的用户权限的应用程序范围。</span><span class="sxs-lookup"><span data-stu-id="4a744-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4a744-174">如果访问明确拒绝中任意一种或两个设置，Project Online 拒绝访问的信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4a744-175">否则，授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="4a744-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4a744-176">启用 sideloading 网站上。</span><span class="sxs-lookup"><span data-stu-id="4a744-176">Enable sideloading on your site.</span></span> <span data-ttu-id="4a744-177">请参阅[配置 Project Online 应用程序开发的](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)文章的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-177">See the [Configuring Project Online for App Development ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)article for more information.</span></span> 
    
4. <span data-ttu-id="4a744-178">生成项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-178">Build the project.</span></span>
    
5. <span data-ttu-id="4a744-179">运行项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-179">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="4a744-180">项目提供托管外接程序开发环境</span><span class="sxs-lookup"><span data-stu-id="4a744-180">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="4a744-181">提供程序承载的加载项是编写的应用程序和驻留在任何 web 平台上。</span><span class="sxs-lookup"><span data-stu-id="4a744-181">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="4a744-182">他们可以连接并执行数据操作使用 REST （或 Microsoft 平台的 CSOM） API。</span><span class="sxs-lookup"><span data-stu-id="4a744-182">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="4a744-183">任何语言和环境支持 REST 接口的可用于开发。</span><span class="sxs-lookup"><span data-stu-id="4a744-183">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="4a744-184">这种应用程序的 Windows 开发环境的示例包括以下各项：</span><span class="sxs-lookup"><span data-stu-id="4a744-184">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="4a744-185">Visual Studio 2015 （首选） 或 Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4a744-185">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4a744-186">Visual Studio （提供与 Visual Studio 2015 专业版和企业版） 的 Microsoft Office 开发工具</span><span class="sxs-lookup"><span data-stu-id="4a744-186">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4a744-187">.NET framework 4.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="4a744-187">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4a744-188">[SharePointOnline CSOM 包](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx)（对于 CSOM 调用）</span><span class="sxs-lookup"><span data-stu-id="4a744-188">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4a744-189">编程语言，例如，C#</span><span class="sxs-lookup"><span data-stu-id="4a744-189">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4a744-190">请访问https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations的示例脚本。</span><span class="sxs-lookup"><span data-stu-id="4a744-190">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="4a744-191">您可以运行该示例在几个步骤：</span><span class="sxs-lookup"><span data-stu-id="4a744-191">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4a744-192">下载并打开示例应用程序</span><span class="sxs-lookup"><span data-stu-id="4a744-192">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4a744-193">更新属性窗口中的 siteurl 属性</span><span class="sxs-lookup"><span data-stu-id="4a744-193">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4a744-194">Project Online 检查外接程序和管理访问的 Project Online 主机上的信息的用户权限的应用程序范围。</span><span class="sxs-lookup"><span data-stu-id="4a744-194">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4a744-195">如果访问明确拒绝中任意一种或两个设置，Project Online 拒绝访问的信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-195">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4a744-196">否则，授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="4a744-196">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4a744-197">启用 sideloading 网站上。</span><span class="sxs-lookup"><span data-stu-id="4a744-197">Enable sideloading on your site.</span></span> <span data-ttu-id="4a744-198">请参阅[配置 Project Online 应用程序开发的](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)文章的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-198">See the [Configuring Project Online for App Development ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)article for more information.</span></span> 
    
4. <span data-ttu-id="4a744-199">生成项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-199">Build the project.</span></span>
    
5. <span data-ttu-id="4a744-200">运行项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-200">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="4a744-201">外部/独立应用程序开发环境</span><span class="sxs-lookup"><span data-stu-id="4a744-201">External/standalone application development environment</span></span>

<span data-ttu-id="4a744-202">独立的应用程序可以呼叫 Project Online 中使用的客户端对象模型 (CSOM) 或 REST 进行通信与 Project Online 中创建、 检索、 更新和删除驻留在服务器上的信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-202">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="4a744-203">这是取决于用户的访问级别，以运行独立客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="4a744-203">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="4a744-204">这种应用程序的 Windows 开发环境的示例包括以下各项：</span><span class="sxs-lookup"><span data-stu-id="4a744-204">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="4a744-205">Visual Studio 2015 （首选） 或 Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4a744-205">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4a744-206">Visual Studio （提供与 Visual Studio 2015 专业版和企业版） 的 Microsoft Office 开发工具</span><span class="sxs-lookup"><span data-stu-id="4a744-206">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4a744-207">.NET framework 4.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="4a744-207">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4a744-208">[SharePointOnline CSOM 包](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx)（对于 CSOM 调用）</span><span class="sxs-lookup"><span data-stu-id="4a744-208">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4a744-209">编程语言，例如，C#</span><span class="sxs-lookup"><span data-stu-id="4a744-209">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4a744-210">请访问https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields示例应用程序。</span><span class="sxs-lookup"><span data-stu-id="4a744-210">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="4a744-211">您可以运行该示例在几个步骤：</span><span class="sxs-lookup"><span data-stu-id="4a744-211">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4a744-212">下载示例应用程序</span><span class="sxs-lookup"><span data-stu-id="4a744-212">Download the sample application</span></span>
    
2. <span data-ttu-id="4a744-213">进行几个更改以访问 Project Online 网站 — 站点名称、 用户帐户和密码。</span><span class="sxs-lookup"><span data-stu-id="4a744-213">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="4a744-214">确保用户有权访问所有项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-214">Ensure the user has access to all projects.</span></span> <span data-ttu-id="4a744-215">Project Online 使用用户权限来控制对数据存储中的信息的访问。</span><span class="sxs-lookup"><span data-stu-id="4a744-215">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="4a744-216">将 SharePoint 程序集添加到使用 Nuget 程序包管理器控制台，可从工具菜单下 Nuget 控制台中键入以下内容的引用：</span><span class="sxs-lookup"><span data-stu-id="4a744-216">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="4a744-217">生成项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-217">Build the project.</span></span>
    
5. <span data-ttu-id="4a744-218">运行项目。</span><span class="sxs-lookup"><span data-stu-id="4a744-218">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="4a744-219">后续步骤</span><span class="sxs-lookup"><span data-stu-id="4a744-219">Next steps</span></span>

<span data-ttu-id="4a744-220">每个示例应用程序具有文章介绍使用单个项目 API 的要点。</span><span class="sxs-lookup"><span data-stu-id="4a744-220">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="4a744-221">文章将显示以下列表中，一些文章的描述的实体关系，以及查询系统，并在访问自定义字段的信息。</span><span class="sxs-lookup"><span data-stu-id="4a744-221">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="4a744-222">开发 Project Online 应用程序使用的客户端对象模型</span><span class="sxs-lookup"><span data-stu-id="4a744-222">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="4a744-223">开发的 Project Online 外接程序使用 JavaScript 对象模型 (JSOM)</span><span class="sxs-lookup"><span data-stu-id="4a744-223">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="4a744-224">访问 Project Online 企业自定义字段</span><span class="sxs-lookup"><span data-stu-id="4a744-224">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="4a744-225">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a744-225">See also</span></span>

<span data-ttu-id="4a744-226">有关文档和与 Project Online 和使用 CSOM 的应用程序开发相关的示例，请参阅[Project 开发门户](http://dev.office.com/project.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a744-226">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    
