---
title: 部署包含代码的 InfoPath 表单模板
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- deploying form templates [infopath 2007],InfoPath 2007, deploying form templates,form templates [InfoPath 2007], deploying,.NET Framework security settings [InfoPath 2007],deployment [InfoPath 2007], form templates
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: InfoPath 托管代码表单模板的表单代码编译为在公共语言运行库 (CLR) 下运行的程序集。这意味着只要您需要对表单代码进行更改，就必须在 Visual Studio 2008 中打开其项目，在代码编辑器中进行更改，重新编译表单模板，然后重新部署该表单模板。此外，由于托管代码表单模板的专用程序集是在托管的 CLR 应用程序域中运行的，因此需要完全信任的表单的安全设置与不需要完全信任的表单模板稍有不同。
ms.openlocfilehash: 56af865a80df75c7e1d973767066a03310cdde1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773981"
---
# <a name="deploy-infopath-form-templates-with-code"></a><span data-ttu-id="c8fff-106">部署包含代码的 InfoPath 表单模板</span><span class="sxs-lookup"><span data-stu-id="c8fff-106">Deploy InfoPath Form Templates with Code</span></span>

<span data-ttu-id="c8fff-p102">InfoPath 托管代码表单模板的表单代码编译为在公共语言运行库 (CLR) 下运行的程序集。这意味着只要您需要对表单代码进行更改，就必须在 Visual Studio 2008 中打开其项目，在代码编辑器中进行更改，重新编译表单模板，然后重新部署该表单模板。此外，由于托管代码表单模板的专用程序集是在托管的 CLR 应用程序域中运行的，因此需要完全信任的表单的安全设置与不需要完全信任的表单模板稍有不同。</span><span class="sxs-lookup"><span data-stu-id="c8fff-p102">The form code for an InfoPath managed code form template is compiled as an assembly that runs under the common language runtime (CLR). This means that whenever you need to make changes to the form code, you must open its project in Visual Studio 2012, make changes in the code editor, recompile your form template, and then re-deploy the form template. Additionally, because the private assembly for a managed code form template is running under a hosted CLR application domain, the security settings for forms that require full trust differ somewhat from form templates that do not require full trust.</span></span>
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a><span data-ttu-id="c8fff-110">部署不需要完全信任的表单模板</span><span class="sxs-lookup"><span data-stu-id="c8fff-110">Deploying Form Templates That Do Not Require Full Trust</span></span>

<span data-ttu-id="c8fff-p103">如果您的表单模板的表单代码不使用需要完全信任的 InfoPath 对象模型成员，并且该表单模板不使用需要完全信任的功能，那么您可以使用以下步骤直接从 InfoPath 发布您的表单模板。有关 InfoPath 安全模型的信息，请参阅[关于具有代码的表单模板的安全模型](about-the-security-model-for-form-templates-with-code.md)。</span><span class="sxs-lookup"><span data-stu-id="c8fff-p103">If the form code for your form template does not use InfoPath object model members that require full trust, and the form template does not use features that require full trust, you can publish your form template directly from InfoPath using the following procedure. For information about the InfoPath security model, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md).</span></span>
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a><span data-ttu-id="c8fff-113">部署不需要完全信任的表单模板</span><span class="sxs-lookup"><span data-stu-id="c8fff-113">Deploy a form template that does not require full trust</span></span>

1. <span data-ttu-id="c8fff-114">在 Visual Studio 2008 中创建和调试表单模板。</span><span class="sxs-lookup"><span data-stu-id="c8fff-114">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="c8fff-115">如果您正在 Visual Studio 2012 代码编辑器中，切换到 InfoPath，再单击**文件**选项卡，，，然后单击在**发布**选项卡上所需发布位置的按钮 (如果您已经以前发布表单模板，则可以单击**文件**选项卡，然后再单击**快速发布**以重新发布到同一位置的表单模板。)</span><span class="sxs-lookup"><span data-stu-id="c8fff-115">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, and then click the button for the desired publishing location on the **Publish** tab. (If you have published the form template previously, you can click the **File** tab, and then click **Quick Publish** to republish the form template to the same location.)</span></span> 
    
    <span data-ttu-id="c8fff-116">编译的表单模板和启动**发布向导**。</span><span class="sxs-lookup"><span data-stu-id="c8fff-116">The form template is compiled and the **Publishing Wizard** is launched.</span></span> <span data-ttu-id="c8fff-117">按照**发布向导**以将表单部署到您选择的位置中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c8fff-117">Follow the steps in the **Publishing Wizard** to deploy your form to the location of your choice.</span></span> <span data-ttu-id="c8fff-118">有关使用**发布向导**的详细信息，"发布表单模板"InfoPath 帮助中搜索。</span><span class="sxs-lookup"><span data-stu-id="c8fff-118">For more information about using the **Publishing Wizard**, search InfoPath Help for "Publish a form template".</span></span>
    
## <a name="deploying-form-templates-that-require-full-trust"></a><span data-ttu-id="c8fff-119">部署需要完全信任的表单模板</span><span class="sxs-lookup"><span data-stu-id="c8fff-119">Deploying Form Templates That Require Full Trust</span></span>

<span data-ttu-id="c8fff-p105">如果您的表单模板的表单代码使用需要完全信任的 InfoPath 对象模型成员，或者该表单模板使用需要完全信任的功能，则您必须使用来自受信任发布者的代码签名证书对您的表单模板 (.xsn) 文件进行数字签名，当您的用户打开表单时，系统将提示他们信任该证书。这将使您的表单完全受信任，反过来也对您的表单代码授予 FullTrust 权限集。</span><span class="sxs-lookup"><span data-stu-id="c8fff-p105">If the form code for your form template does use InfoPath object model members that require full trust, or the form template uses features that require full trust, you must digitally sign your form template (.xsn) file with a code signing certificate from a trusted publisher, which your users will be prompted to trust when they open the form. This will also make your form fully-trusted, and in turn grant the FullTrust permission set to your form code.</span></span>
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a><span data-ttu-id="c8fff-122">编译、发布表单模板并对其进行数字签名</span><span class="sxs-lookup"><span data-stu-id="c8fff-122">Compile, publish, and digitally sign a form template</span></span>

1. <span data-ttu-id="c8fff-123">在 Visual Studio 2008 中创建和调试表单模板。</span><span class="sxs-lookup"><span data-stu-id="c8fff-123">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="c8fff-124">如果您正在 Visual Studio 2012 代码编辑器中，切换到 InfoPath，单击**文件**选项卡，然后单击**表单选项**。</span><span class="sxs-lookup"><span data-stu-id="c8fff-124">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="c8fff-125">单击**安全和信任**类别。</span><span class="sxs-lookup"><span data-stu-id="c8fff-125">Click the **Security and Trust** category.</span></span> 
    
4. <span data-ttu-id="c8fff-126">在下，**安全级别**，清除**自动确定安全级别**复选框，然后选择**完全信任**。</span><span class="sxs-lookup"><span data-stu-id="c8fff-126">Under **Security Level**, clear the **Automatically determine security level** check box, and then select **Full Trust**.</span></span>
    
5. <span data-ttu-id="c8fff-127">在**表单模板签名**选择**此表单模板签名**，单击**选择证书**，然后指定的代码签名证书用于对表单模板签名。</span><span class="sxs-lookup"><span data-stu-id="c8fff-127">Under **Form Template Signature**, select **Sign this form template**, click **Select Certificate**, and then specify the code signing certificate with which to sign the form template.</span></span>
    
6. <span data-ttu-id="c8fff-128">单击**确定**两次以关闭**表单选项**对话框，然后保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="c8fff-128">Click **OK** twice to close the **Form Options** dialog box, and then save your changes.</span></span> 
    
7. <span data-ttu-id="c8fff-129">单击**发布**选项卡，然后单击所需发布位置的按钮。</span><span class="sxs-lookup"><span data-stu-id="c8fff-129">Click the **Publish** tab, and then click the button for the desired publishing location.</span></span> 
    
8. <span data-ttu-id="c8fff-130">编译的表单模板和启动**发布向导**。</span><span class="sxs-lookup"><span data-stu-id="c8fff-130">The form template is compiled and the **Publishing Wizard** is launched.</span></span> <span data-ttu-id="c8fff-131">按照**发布向导**以部署表单模板中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c8fff-131">Follow the steps in the **Publishing Wizard** to deploy your form template.</span></span> <span data-ttu-id="c8fff-132">有关使用**发布向导**将部署需要完全信任的表单模板的详细信息，"发布具有完全信任的表单模板"InfoPath 帮助中搜索。</span><span class="sxs-lookup"><span data-stu-id="c8fff-132">For more information about using the **Publishing Wizard** to deploy a form template that requires full trust, search InfoPath Help for "Publish a form template with full trust".</span></span> 
    
 <span data-ttu-id="c8fff-133">**备注**</span><span class="sxs-lookup"><span data-stu-id="c8fff-133">**Notes**</span></span>
- <span data-ttu-id="c8fff-p107">要对表单进行数字签名，计算机上必须安装了经过验证的代码签名证书。要获取这样的证书，必须与证书颁发机构或网络管理员联系。</span><span class="sxs-lookup"><span data-stu-id="c8fff-p107">To digitally sign a form, you must have an authenticated code signing certificate installed on your computer. To acquire such a certificate, you must contact a certification authority or your network administrator.</span></span>
    
- <span data-ttu-id="c8fff-136">如果您需要在发布表单之后对表单进行更改，必须重复上述过程并重新对表单模板进行签名。</span><span class="sxs-lookup"><span data-stu-id="c8fff-136">If you need to make changes to the form after publishing, you must repeat the procedure and re-sign the form template.</span></span> <span data-ttu-id="c8fff-137">这是因为更改表单会使数字签名失效。</span><span class="sxs-lookup"><span data-stu-id="c8fff-137">This is because altering the form invalidates the digital signature.</span></span> <span data-ttu-id="c8fff-138">需要完全信任权限的窗体的开发过程中可以使用[预览和调试需要完全信任的表单模板](how-to-preview-and-debug-form-templates-that-require-full-trust.md)中介绍的过程在本地计算机上注册的表单模板。</span><span class="sxs-lookup"><span data-stu-id="c8fff-138">During the development of a form that requires full trust permissions you can use the procedure described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md) to register the form template on your local computer.</span></span> 
    
## <a name="configuring-net-framework-security-settings"></a><span data-ttu-id="c8fff-139">配置 .NET Framework 安全设置</span><span class="sxs-lookup"><span data-stu-id="c8fff-139">Configuring .NET Framework Security Settings</span></span>

<span data-ttu-id="c8fff-140">要对授予在 InfoPath 托管代码表单模板中运行的托管代码的权限进行更多控制，可以使用 .NET Framework 2.0 配置实用程序对您的表单代码授予特定权限集。</span><span class="sxs-lookup"><span data-stu-id="c8fff-140">For additional control over the permissions granted to managed code running in an InfoPath managed code form template, you can use the .NET Framework 2.0 Configuration utility to grant a particular permission set to your form code.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c8fff-p109">[!重要信息] 为 InfoPath 托管代码表单模板配置 .NET Framework 安全设置时，不会影响是否允许运行需要完全信任的 InfoPath 对象模型成员。您必须按照本主题前面所述的过程对表单模板进行数字签名或注册，以允许调用需要完全信任的 InfoPath 对象模型成员。配置 .NET Framework 安全设置仅适用于对 .NET Framework 类的成员和托管组件的调用，而不适用于 InfoPath 对象模型。</span><span class="sxs-lookup"><span data-stu-id="c8fff-p109">Configuring .NET Framework security settings for an InfoPath managed code form template does not affect whether InfoPath object model members that require full trust are allowed to run. You must either digitally sign or register a form template as described earlier in this topic to enable calls to InfoPath object model members that require full trust. Configuring .NET Framework security settings apply only to calls to members of .NET Framework classes and managed components other than the InfoPath object model.</span></span> 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a><span data-ttu-id="c8fff-144">编译、发布和配置表单模板的 .NET 安全设置</span><span class="sxs-lookup"><span data-stu-id="c8fff-144">Compile, publish, and configure .NET security settings for a form template</span></span>

1. <span data-ttu-id="c8fff-145">在 Visual Studio 2008 中创建和调试表单模板。</span><span class="sxs-lookup"><span data-stu-id="c8fff-145">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="c8fff-146">如果您正在 Visual Studio 2012 代码编辑器中，切换到 InfoPath、**文件**选项卡，单击**发布**，然后单击所需发布位置的按钮。</span><span class="sxs-lookup"><span data-stu-id="c8fff-146">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, click **Publish**, and then click the button for the desired publishing location.</span></span>
    
    <span data-ttu-id="c8fff-147">编译的表单模板和启动**发布向导**。</span><span class="sxs-lookup"><span data-stu-id="c8fff-147">The form template is compiled and the **Publishing Wizard** is launched.</span></span> <span data-ttu-id="c8fff-148">按照**发布向导**以部署表单模板中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c8fff-148">Follow the steps in the **Publishing Wizard** to deploy your form template.</span></span> <span data-ttu-id="c8fff-149">有关使用**发布向导**的详细信息，"发布表单模板"InfoPath 帮助中搜索。</span><span class="sxs-lookup"><span data-stu-id="c8fff-149">For more information about using the **Publishing Wizard**, search InfoPath Help for "Publish a form template".</span></span>
    
3. <span data-ttu-id="c8fff-150">执行[与代码的表单模板配置安全设置](how-to-configure-security-settings-for-form-templates-with-code.md)"分配 FullTrust 到窗体位于特定 URL 或 UNC"部分中所述的步骤</span><span class="sxs-lookup"><span data-stu-id="c8fff-150">Perform the procedure described in the "Assigning FullTrust to Forms at a Specific URL or UNC" section of the [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8fff-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8fff-151">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="c8fff-152">任务</span><span class="sxs-lookup"><span data-stu-id="c8fff-152">Tasks</span></span>

[<span data-ttu-id="c8fff-153">配置与代码的表单模板的安全设置</span><span class="sxs-lookup"><span data-stu-id="c8fff-153">Configure Security Settings for Form Templates with Code</span></span>](how-to-configure-security-settings-for-form-templates-with-code.md)


[<span data-ttu-id="c8fff-154">关于具有代码的表单模板的安全模型</span><span class="sxs-lookup"><span data-stu-id="c8fff-154">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)
  
[<span data-ttu-id="c8fff-155">预览和调试需要完全信任的表单模板</span><span class="sxs-lookup"><span data-stu-id="c8fff-155">Preview and Debug Form Templates that Require Full Trust</span></span>](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
