---
title: 远程数据访问解决方案
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef617f91aa6f36969932a4d8f2914df2de935787
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998159"
---
# <a name="solutions-for-remote-data-access"></a>远程数据访问解决方案

**适用于**： Access 2013、 Office 2013

## <a name="the-issue"></a>问题

应用程序可以通过 ADO 直接访问并修改数据源（有时称为双层系统）。例如，如果应用程序与包含数据的数据源连接，那么这就是双层系统中的直接连接。

但是，您可能要通过如 Microsoft Internet 信息服务 (IIS) 中间间接访问数据源。 这种安排有时称为三层系统。 IIS 是一种客户端/服务器系统，为本地（或客户端）应用程序通过 Internet 或 Intranet 调用远程（或服务器）程序提供了有效的方式。 服务器程序获取数据源的访问权，并可以选择对获得的数据进行处理。

例如，intranet 网页包含在 Microsoft Visual Basic Scripting Edition (VBScript) 中，将连接到 IIS 编写的应用程序。 IIS 检索数据，并采用某种方式对数据进行处理，然后将处理过的信息返回给应用程序。

在本例中，应用程序始终都不与数据源直接连接，与数据源直接连接的是 IIS。且 IIS 通过 ADO 来访问数据。

> [!NOTE]
> 不需要基于 Internet 或 intranet 上的客户端/服务器应用程序 (即，基于 web 的) — 它可以包含单独的局域网上编译的程序。 但是，典型情况是基于 web 的应用程序。

由于某些可视控件（如网格、复选框或列表）可能使用返回的信息，因此可视控件必须能方便地使用返回的信息。

您需要一个简单而有效的应用程序编程接口，以支持三层系统，并像在双层系统中检索数据那样轻松地返回信息。远程数据服务 (RDS) 就是这样的接口。

## <a name="the-solution"></a>解决方案

RDS 定义编程模型 — 活动需要访问和更新数据源的顺序 — 即可通过中间，如 Internet 信息服务 (IIS) 中的数据访问。 编程模型中囊括了 RDS 的全部功能。

