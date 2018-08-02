---
title: 一次性表
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 上次修改时间： 2011 年 11 月 8 日
ms.openlocfilehash: 3ad9141f2530e64664a2d0c75ece2b834cc6ad78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19776536"
---
# <a name="one-off-tables"></a><span data-ttu-id="606db-103">一次性表</span><span class="sxs-lookup"><span data-stu-id="606db-103">One-Off Tables</span></span>

<span data-ttu-id="606db-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="606db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="606db-105">一次性表包含有关用于创建新的收件人的地址簿提供程序支持的模板的信息。</span><span class="sxs-lookup"><span data-stu-id="606db-105">A one-off table contains information about the templates that an address book provider supports for creating new recipients.</span></span> <span data-ttu-id="606db-106">一次性表按通讯簿提供程序，单个地址簿容器和 MAPI，实现，并且可以是永久或临时。</span><span class="sxs-lookup"><span data-stu-id="606db-106">One-off tables are implemented by address book providers, individual address book containers, and by MAPI, and can be persistent or temporary.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="606db-107">请勿将混淆一次性模板标识符; 表中的模板其目的相似时，其代码构造是之类 nothing。</span><span class="sxs-lookup"><span data-stu-id="606db-107">Do not confuse the templates in one-off tables with template identifiers; while their purposes are similar, their code constructs are nothing alike.</span></span> <span data-ttu-id="606db-108">模板用于创建特定类型的收件人，而模板标识符用于将数据绑定的一个收件人属于代码的宿主提供程序以支持另一个收件人属于外的提供程序。</span><span class="sxs-lookup"><span data-stu-id="606db-108">Templates are used to create recipients of a particular type while template identifiers are used to bind the data of one recipient that belong to a host provider with code to support another recipient that belong to a foreign provider.</span></span> 
  
<span data-ttu-id="606db-109">客户端创建新的收件人：</span><span class="sxs-lookup"><span data-stu-id="606db-109">Clients create new recipients:</span></span>
  
- <span data-ttu-id="606db-110">若要添加到的传出邮件的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="606db-110">To add to the recipient list of an outgoing message.</span></span>
    
- <span data-ttu-id="606db-111">若要添加到某个通讯簿中的容器。</span><span class="sxs-lookup"><span data-stu-id="606db-111">To add to one of the containers in the address book.</span></span>
    
<span data-ttu-id="606db-112">在这两种方案中，通讯簿提供程序被请求返回一次性表。</span><span class="sxs-lookup"><span data-stu-id="606db-112">In both scenarios, an address book provider is asked to return a one-off table.</span></span> <span data-ttu-id="606db-113">一个一次性表用于同时的情况下或唯一一次性表对于每种情况，可以实现通讯簿提供程序。</span><span class="sxs-lookup"><span data-stu-id="606db-113">Address book providers can implement either a single one-off table to be used in both situations or a unique one-off table for each situation.</span></span> 
  
<span data-ttu-id="606db-114">当收件人将包含在传出 message 时，MAPI 调用通讯簿提供程序的[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)方法来检索其一次性表。</span><span class="sxs-lookup"><span data-stu-id="606db-114">When the recipient will be included with an outgoing message, MAPI calls the address book provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method to retrieve its one-off table.</span></span> <span data-ttu-id="606db-115">一次性表包含模板，它使用户能够输入有效的地址与收件人的创建过程中生成的信息。</span><span class="sxs-lookup"><span data-stu-id="606db-115">The one-off table includes templates which enable a user to enter information resulting in the creation of a recipient with a valid address.</span></span> <span data-ttu-id="606db-116">此表中，使其保持上的通知的 MAPI register 打开，以便更改可以反映到用户。</span><span class="sxs-lookup"><span data-stu-id="606db-116">MAPI registers for notifications on this table, keeping it open so that changes can be reflected to the user.</span></span> <span data-ttu-id="606db-117">仅当调用其子系统或地址簿状态对象的[IMAPIStatus::ValidateState](imapistatus-validatestate.md)方法时，MAPI 释放表。</span><span class="sxs-lookup"><span data-stu-id="606db-117">MAPI releases the table only when its subsystem or address book status object's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> 
  
<span data-ttu-id="606db-118">当收件人将添加到容器时，MAPI 调用不同，调用容器的[IMAPIProp::OpenProperty](imapiprop-openproperty.md)方法来检索其**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) 属性。</span><span class="sxs-lookup"><span data-stu-id="606db-118">When the recipient will be added to a container, MAPI makes a different call, invoking the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve its **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="606db-119">模板包括在此一次性表组表示可以添加到容器的收件人的类型。</span><span class="sxs-lookup"><span data-stu-id="606db-119">The set of templates included in this one-off table represents the types of recipients that can be added to the container.</span></span> <span data-ttu-id="606db-120">例如，邮件服务器通常公开一个容器以便每个容器仅包含地址特定于相应的网关安装每个网关。</span><span class="sxs-lookup"><span data-stu-id="606db-120">For example, mail servers often expose one container for every gateway that is installed so that each container only holds addresses specific to the corresponding gateway.</span></span>
  
<span data-ttu-id="606db-121">MAPI 提供了一次性的会话中包括自己模板以及从通讯簿提供程序的每个模板表。</span><span class="sxs-lookup"><span data-stu-id="606db-121">MAPI provides a one-off table that includes its own templates as well as templates from each of the address book providers in the session.</span></span> <span data-ttu-id="606db-122">MAPI 提供了可用于创建一个新收件人的任何地址类型，假定用户知道其格式的泛型模板。</span><span class="sxs-lookup"><span data-stu-id="606db-122">MAPI provides a generic template that can be used to create a new recipient for any address type, assuming that the user knows its format.</span></span> <span data-ttu-id="606db-123">通讯簿提供程序通过调用[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)使用此一次性表。</span><span class="sxs-lookup"><span data-stu-id="606db-123">Address book providers use this one-off table by calling [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span></span> <span data-ttu-id="606db-124">每个中创建具有有效的收件人地址的收件人的 MAPI 一次性表结果中包含的模板。</span><span class="sxs-lookup"><span data-stu-id="606db-124">Each of the templates included in the MAPI one-off table results in the creation of recipients with valid recipient addresses.</span></span>
  
<span data-ttu-id="606db-125">通讯簿提供程序通常提供一个模板的它们支持每个地址类型。</span><span class="sxs-lookup"><span data-stu-id="606db-125">Address book providers typically supply one template for every address type they support.</span></span> <span data-ttu-id="606db-126">但是，支持的模板，则不需要。</span><span class="sxs-lookup"><span data-stu-id="606db-126">However, support for templates is not required.</span></span> <span data-ttu-id="606db-127">MAPI 呼叫请求一次性表时，不允许创建的新地址的地址簿提供程序可以返回 MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="606db-127">Address book providers that do not allow the creation of new addresses can return MAPI_E_NO_SUPPORT when MAPI calls to request a one-off table.</span></span> <span data-ttu-id="606db-128">通讯簿提供程序的执行允许创建新的地址，但不是提供任何模板可以调用**IMAPISupport::GetOneOffTable**使用 MAPI 一次性表中列出的模板。</span><span class="sxs-lookup"><span data-stu-id="606db-128">Address book providers that do allow new address creation but do not supply any templates can call **IMAPISupport::GetOneOffTable** to use the templates listed in the MAPI one-off table.</span></span> 
  
<span data-ttu-id="606db-129">以下属性构成一次性表中所需的列：</span><span class="sxs-lookup"><span data-stu-id="606db-129">The following properties make up the required column set in one-off tables:</span></span>
  
- <span data-ttu-id="606db-130">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-131">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-131">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-132">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-133">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-134">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-135">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-135">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="606db-136">**PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="606db-136">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))</span></span>
    
 <span data-ttu-id="606db-137">**PR_ADDRTYPE**指示可以使用模板创建新收件人与相关联的地址的类型。</span><span class="sxs-lookup"><span data-stu-id="606db-137">**PR_ADDRTYPE** indicates the type of address that can be associated with the new recipient created with the template.</span></span> 
  
 <span data-ttu-id="606db-138">**PR_DISPLAY_NAME**和**PR_DISPLAY_TYPE**将数据与新收件人关联。</span><span class="sxs-lookup"><span data-stu-id="606db-138">**PR_DISPLAY_NAME** and **PR_DISPLAY_TYPE** associate data with the new recipient.</span></span> <span data-ttu-id="606db-139">**PR_DISPLAY_NAME**包含的字符串标识新的收件人，并且**PR_DISPLAY_TYPE**包含一个标识图标显示时带有行的类型的常量。</span><span class="sxs-lookup"><span data-stu-id="606db-139">**PR_DISPLAY_NAME** contains a character string that identifies the new recipient and **PR_DISPLAY_TYPE** contains a constant that identifies the type of icon to be displayed with the row.</span></span> <span data-ttu-id="606db-140">邮件用户的模板已设置为 DT_MAILUSER; 其**PR_DISPLAY_TYPE**列通讯组列表的模板已设置为 DT_DISTLIST 其**PR_DISPLAY_TYPE**列。</span><span class="sxs-lookup"><span data-stu-id="606db-140">Templates for messaging users have their **PR_DISPLAY_TYPE** column set to DT_MAILUSER; templates for distribution lists have their **PR_DISPLAY_TYPE** column set to DT_DISTLIST.</span></span> 
  
 <span data-ttu-id="606db-141">**PR_ENTRYID**是要用于创建一个新收件人的模板的项标识符。</span><span class="sxs-lookup"><span data-stu-id="606db-141">**PR_ENTRYID** is the entry identifier of the template to be used to create a new recipient.</span></span> <span data-ttu-id="606db-142">此条目标识符可以传递给将来[IAddrBook::NewEntry](iaddrbook-newentry.md)、 [IAddrBook::OpenEntry](iaddrbook-openentry.md)和[IABContainer::CreateEntry](iabcontainer-createentry.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="606db-142">This entry identifier can be passed to future [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), and [IABContainer::CreateEntry](iabcontainer-createentry.md) calls.</span></span> <span data-ttu-id="606db-143">容器设置为默认的邮件用户模板与**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) 和**PR_ENTRYID**列中的默认通讯组列表及其行及其行的**PR_ENTRYID**列到**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) 模板。</span><span class="sxs-lookup"><span data-stu-id="606db-143">Containers set the **PR_ENTRYID** column of their row for the default messaging user template to **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and the **PR_ENTRYID** column of their row for the default distribution list template to **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="606db-144">**PR_DEPTH**用于支持一次性表中的条目的分层显示，通过指示的模板的缩进级别。</span><span class="sxs-lookup"><span data-stu-id="606db-144">**PR_DEPTH** is used to support the hierarchical display of the entries in a one-off table by indicating the level of indentation for the template.</span></span> <span data-ttu-id="606db-145">尽管一次性表可以显示为平面列表或分层显示，后者是最好和通讯簿提供程序应支持它的适当地设置每个行的**PR_DEPTH**列。</span><span class="sxs-lookup"><span data-stu-id="606db-145">Although one-off tables can be displayed either as a flat list or a hierarchical display, the latter is preferable and address book providers should support it by setting the **PR_DEPTH** column for each row appropriately.</span></span> <span data-ttu-id="606db-146">**PR_DEPTH**是从零开始;值为 0，在其**PR_DEPTH**列中的行不缩进。</span><span class="sxs-lookup"><span data-stu-id="606db-146">**PR_DEPTH** is zero-based; rows with a value of 0 in their **PR_DEPTH** column are not indented.</span></span> <span data-ttu-id="606db-147">**PR_DEPTH**的值越高的更多行是缩进。</span><span class="sxs-lookup"><span data-stu-id="606db-147">The higher the value of **PR_DEPTH**, the more the row is indented.</span></span> <span data-ttu-id="606db-148">例如，具有**PR_DEPTH**设置为 1 行是缩进一个制表时**PR_DEPTH**设置为 3 行缩进的三个选项卡。</span><span class="sxs-lookup"><span data-stu-id="606db-148">For example, rows with **PR_DEPTH** set to 1 are indented one tab while rows with **PR_DEPTH** set to 3 are indented three tabs.</span></span> 
  
 <span data-ttu-id="606db-149">**PR_SELECTABLE**用于指示表中的行是否表示可以选择和用于创建一个新收件人的模板。</span><span class="sxs-lookup"><span data-stu-id="606db-149">**PR_SELECTABLE** is used to indicate whether a row in the table represents a template that can be selected and used to create a new recipient.</span></span> <span data-ttu-id="606db-150">尽管大多数一次性表中行执行代表模板，提供程序可以包括非模板行。</span><span class="sxs-lookup"><span data-stu-id="606db-150">Although most rows in a one-off table do represent templates, providers can include non-template rows.</span></span> <span data-ttu-id="606db-151">例如，提供程序可能需要组织一次性表按模板类型，包括在显示但不能用于收件人创建的类别行。</span><span class="sxs-lookup"><span data-stu-id="606db-151">For example, a provider might want to organize the one-off table by template type, including a category row that appears in the display but is not used for recipient creation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="606db-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="606db-152">See also</span></span>



[<span data-ttu-id="606db-153">MAPI 表</span><span class="sxs-lookup"><span data-stu-id="606db-153">MAPI Tables</span></span>](mapi-tables.md)
