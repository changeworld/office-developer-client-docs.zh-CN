---
title: ActiveX 数据对象 (ADO) 术语表
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93f60d38ba68e18b427af3d907a3a41e655c7a32
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465842"
---
# <a name="ado-glossary"></a>ADO 术语表

**适用于**： Access 2013 |Office 2013

## <a name="a"></a>A

**绝对 URL**

Internet 或 intranet 指定的资源的所在位置的完全限定的 URL。 请参阅**URL**和**相对 URL**。

**ActiveX 控件**

自注册，进程内通常具有 visual 元素在设计时或运行的时的 COM 组件。 ActiveX 控件还能够与活动文档容器，如 Microsoft Internet Explorer 进行通信。

**ADISAPI （高级数据 Internet 服务器应用程序编程接口）**

ISAPI DLL 提供分析、 自动化控件、 **Recordset**封送，和 MIME 打包。 ADISAPI 组件适用于通过提供 Internet 信息服务 (IIS) API。 请参阅**ISAPI**。

**聚合函数**

在查询中，如 COUNT、 AVG 或 STDEV 的计算值表的列中使用的所有行的函数。 在编写表达式和编程中，您可以使用 SQL 聚合函数 （包括上面列出的三个） 和域聚合函数来确定各种统计信息。

**alias**

授予对列或表达式中的 SQL SELECT 语句，通常较短或更有意义的替代名称。 例如，BobSales 是以下的 SELECT 语句中的别名:"以从 SalesDB BobSales 选择 wr 销售"。 别名可用于动态分配要控制在**DataControl**对象的绑定列。

**单元线程**

线程的模型其中对对象的所有呼叫都发生在一个线程 COM。 在单元线程，COM 同步，并将封送呼叫。 另请参阅**COM**。

**异步操作**

返回到调用程序控件，而无需等待操作完成操作。 操作已完成之前，请继续执行代码。 请参阅**同步操作**。

返回顶部

## <a name="b"></a>B

**绑定项**

表中的字段和变量之间的映射。 在 Visual c + + 的 ADO 扩展， **Recordset**字段映射到 C/c + + 变量。

**位掩码**

一个数值，它适用于与其他数值，由位值比较通常要标记参数或返回值中的选项。 通常使用按位的逻辑运算符，如**And**和**或**在 Visual Basic 中，执行此比较**&** 和**|** c + + 中。

例如，ADO **FieldAttributeEnum**值可为位掩码来确定字段的属性。 假设您要确定是否可更新字段。 使用以下表达式在 Visual Basic 中，您无法为此测试：  
  

如果结果为 TRUE，则可更新字段。

**bookmark**

唯一标识中的一组行的行，以便用户可以迅速导航至其标记。

**业务对象**

执行一组定义的操作，如数据验证或业务规则逻辑的对象。 业务对象通常位于中间层。

**业务规则**

验证编辑、 登录校验、 数据库查找、 策略和构成开展业务的企业的方式的算法变换的组合。 也称为为*业务逻辑*。

返回顶部

## <a name="c"></a>C

**计算的表达式**

一个表达式不是常量，但其值取决于其他值。 要进行求值计算的表达式必须获取并计算从其他源，通常在其他字段或行中的值。

**章**

对行的范围从数据源的引用。 在 ADO 中，一章通常是另一个**记录集**的引用。

章节列使定义*的父子*关系其中*父*是**Recordset** ，其中包含的章节列和*子***记录集**由中的一章。

**chapter-alias**

引用追加到父对象的列别名。

**字符集**

映射到其数值字符的一组。 例如，Unicode 是一个 16 位字符集能够对所有已知的字符进行编码和用作全球的字符编码标准。

**子**

相关的一侧的分层关系。 子元素是具有之上的另一个节点的层次结构中的节点 （接近根目录）。 请参阅**子别名**、**父子关系**和**父**。

**child-alias**

引用子别名。 请参阅**别名**，**子**。

**CLSID （类标识符）**

全局唯一标识符 (UUID) 标识的 COM 组件。 每个 COM 组件具有其 CLSID Windows 注册表中，以便可以由其他应用程序加载它。 请参阅**ProgID**， **COM**。

**客户端层**

分布式系统通常将数据提交给和处理来自用户，有时也称为*前端*输入的逻辑图层。 通常情况下，客户端层请求从基于输入服务器的数据，然后设置格式，并显示结果。 请参阅**中间层**、**层的数据源**和**分布式应用程序**。

**COM （组件对象模型）**

使对象来实现互操作，而不考虑其开发语言或其所在的计算机上的网络环境中的一种二进制标准。 基于 COM 的技术包括 ActiveX 控件、 自动化和对象链接和嵌入 (OLE)。 COM 允许对象公开其功能的其他组件和主机应用程序。 它定义同时对象如何公开本身和各个进程和各个网络这种公开的工作原理。 COM 还定义对象的生命周期。

**COM 组件**

二进制文件 — 例如.dll、.ocx 和某些.exe 文件 — 提供对象支持 COM 标准的。 此类文件包含代码的一个或多个类工厂、 COM 类、 注册表项的机制，加载代码，等等。

**比较运算符**

运算符，比较两个表达式，返回一个布尔值。

条件参数的可能表示为"\>"（大于），"\<"（小于），"="（等于），"\>="（大于或等于），"\<="（小于或等于），"\<\>"（不等于），或"like"（模式匹配）。

**component**

一个对象，封装数据和代码，并提供了一套合理指定可公开访问服务。

**复合文件**

COM 实现结构化存储文件。 复合文件将单独对象存储在单一的结构化组成的文件，两个主要元素： 存储对象和 stream 对象。 在一起，它们的功能类似文件中的文件系统。 有关详细信息，请参阅复合的 Microsoft Platform SDK 中的文件。

一个物理文件中绑定在一起的单个文件数。 好像它是一个物理文件，可以访问复合文件中的每个单独的文件。

**常量**

一个数字或字符串的值，不会更改。 可以而不是实际值在代码中使用命名的 ADO 枚举 （枚举常量），例如， **adUseClient**是其值为 3 的常量。 (Const adUseClient = 3)。 请参阅**枚举**。

**游标**

一个数据库元素，控制记录导航、 数据，可更新性和其他用户对数据库所做的更改的可见性。

返回顶部

## <a name="d"></a>D

**数据绑定**

相关联的对象或控件的数据源的应用程序的过程。 与数据源关联的控件称为*数据绑定控件*。

数据绑定控件的内容相关联的数据库中的值。 例如，更新**Recordset**中的行时，可以更新绑定到**Recordset**对象的网格控件。 当**Recordset**中检索新值时，新值显示在网格中。

**数据提供程序**

公开到 ADO 应用程序的数据的软件直接或通过服务提供商。 请参阅**服务提供程序**。

**数据定形**

哪些利用 （称为**形状语言**） 的正式语法来定义一个专用的**Recordset**对象 （称为**已构形 Recordset**） 的包含而不仅仅是数据，但是还引用的其他**Recordset**对象的技术和/ 或计算基于这些**Recordset**对象的值。

**数据源层**

代表运行 DBMS，例如 SQL Server 数据库的计算机的分布式系统逻辑层。 **客户端层**，**中间层**，**分布式应用程序**，请参阅。

**DCOM**

允许 COM 组件相互直接通过网络线路协议。 请参阅**COM**，**组件**。

**DDL （数据定义语言）**

这些的定义，而不是操作，数据在 SQL 语句。 创建或修改与 DDL 数据库的架构。 例如， **CREATE TABLE**、 **CREATE INDEX**、**授予**、 和**取消**是 SQL DDL 语句。

**默认流**

文本或二进制流 （由**Stream**对象），其中使用某些 OLE DB 提供程序，如 Microsoft OLE DB Provider for Internet Publishing 时与**Record**或**Recordset**对象相关联。 默认流通常包含网站的根目录的文件 （如 HTML 代码） 的内容。

**分布式应用程序**

编写，以便通过网络可以跨多台计算机划分处理程序。 通常，分布式应用程序划分为演示文稿、 业务逻辑和数据存储区层或*层*。 请参阅**客户端层**、**中间层**和**数据源层**。

**断开连接的记录集**

**Recordset**对象不再具有连接到服务器的 live 客户端缓存中。 如果原始数据源需要访问再次由于某种原因，如更新数据，必须重新建立连接。 但是，集合、 属性和已断开连接的**Recordset**的方法仍可。

**DLL （动态链接库）**

包含一个或多个函数的已经编译的文件的链接，并分开存放使用它们的过程。 操作系统将 Dll 映射到调用进程的地址空间时正在启动过程，或运行时。

**DML （数据操作语言）**

这些操作，而不是定义，数据的在 SQL 语句。 数据库中的值是选择，使用 DML 修改。 例如，**插入**、**更新**、**删除**和**选择**是 SQL DML 语句。

**文档源提供程序**

提供用于管理文件夹和文档的特殊类。 在由**Record**对象表示文档或文档的文件夹由**Recordset**对象时，文档源提供程序使用填充唯一的一组字段来描述特征的文档，这些对象而不是实际文档本身。 请参阅**资源记录**。

**DSN （数据源名称）**

用于连接到特定的 ODBC 数据库应用程序的信息的集合。 ODBC 驱动程序经理使用此信息来创建与数据库的连接。 DSN 可以存储在文件 （文件 DSN） 或 Windows 注册表 （计算机 DSN） 中。

**动态属性**

特定于数据提供程序或游标服务的属性。 对象的**Properties**集合自动填充这些 （"动态"）。 对象具有任何动态属性，直到连接到通过特定数据提供程序的数据源。 请参阅还**数据提供程序**，**光标**。

返回顶部

## <a name="e-i"></a>E-I

**枚举**

命名常量的列表。 不需要唯一枚举的值。 但是每个值的名称必须是唯一定义枚举的位置范围内。 在 ADO 中枚举用于数值参数和返回值，将添加到 ADO 代码含义和屏蔽 （这可能会更改版本到版本） 的数值从开发人员。 例如，若要打开静态**记录集**，请使用**为 adOpenStatic**枚举值：  
  

也称为*枚举常量*。 请参阅**常量**。

**事件**

一个对象，可以为其编写代码以响应由识别的操作。 可以通过执行命令、 事务完成、 recordset 导航和数据更新等其他操作生成事件。 请参阅**事件处理程序**。

**事件处理程序**

事件处理程序是在事件发生时执行的代码。 请参阅**事件**。

**handler**

管理常规且相对简单条件或操作，如错误恢复或数据管理例程。

**分层记录集**

包含另一个**记录集****记录集**。 另请参阅**数据定形**，**章节**。

有关详细信息，请参阅[访问分层记录集中的行](accessing-rows-in-a-hierarchical-recordset.md)

**层次结构**

一般情况下，层次结构是具有一个顶点的排名的结构级别和附属级别。 在 ADO 中，分层**记录集**用于表示记录和一章之间的父子关系。 此外在 ADO 中， **Record**和**Stream**对象可用于访问分层树结构，如文件夹和文档。 ADO MD 还包括**Hierarchy**对象表示的 OLAP 多维数据集中的维度的级别之间的关系。 请参阅**分层记录集**，**父子关系**、**章节**和**树**。

**ISAPI （Internet 服务器应用程序编程接口）**

对于 Internet 服务器，如 Windows NT Server/Windows 2000 服务器运行 Microsoft Internet 信息服务 (IIS) 的功能集。

返回顶部

## <a name="k-m"></a>K-M

**key**

一列或表格中的列唯一标识行;通常用于索引表。

**封送处理**

打包、 发送，和解接口方法参数跨线程或进程边界的过程。

**中间层**

中的用户界面或 Web 客户端和数据库之间的分布式系统的逻辑层。 这通常是其中业务对象进行实例化。 中间层是业务规则和函数的生成和运行时信息的集合。 它们通过它可以经常发生更改，并因此封装到物理独立于应用程序逻辑本身的组件的业务规则实现这一点。 也称为为*应用程序服务器层*。 请参阅**分布式应用程序**、**客户端层**和**数据源层**。

**MIME （多用途 Internet 邮件扩展）**

Internet 协议最初开发的丰富内容的电子邮件的 exchange 允许跨异构网络、 计算机和电子邮件环境。 实际上，MIME 也已采用并扩展非邮件应用程序。

MIME 是允许二进制数据的发布和阅读 Internet 上的标准。 包含二进制数据的文件的标头包含数据; 的 MIME 类型这将通知客户端程序 (Web 浏览器和邮件包，例如)，他们将需要多于它们处理直线文本以不同方式处理数据。 例如，包含 JPEG 图形 Web 文档的标头中包含特定于 JPEG 文件格式的 MIME 类型。 如果有的话，这样，浏览器以显示其 JPEG 查看器中，使用的文件。

返回顶部

## <a name="n-o"></a>N-O

**节点**

一个分层树结构中的元素。 节点可能根目录中或另一个节点的子级。 节点也可以是多个子元素的父对象。 请参阅**层次结构**、**树**、**根**、**子**和**父**。

**对象变量**

包含对对象的引用的变量。 例如，objCustomObject 是指向 CustomObject 类型的对象的变量：  
  
是指向 CustomObject 类型的对象的变量：  
  
设置 objCustomObject = CreateObject (adodb。Recordset)

**ODBC （开放式数据库连接）**

用于连接到各种数据源标准的编程语言接口。 这通常通过控制面板中，可以分配数据源名称 (Dsn) 使用特定的 ODBC 驱动程序访问。

**OLE DB**

一组公开来自各种源使用数据的接口 OLE DB 接口提供了使用统一访问存储在不同信息源的数据的应用程序。 这些接口支持 DBMS 功能适用于数据源，使其能够共享它的数据量。 另请参阅**COM**。

**开放式锁定**

一种类型的其中均包含一个或多个记录，其中包括正在编辑的记录的数据页锁定向其他用户不可用仅时更新记录后使用**Update**方法，但位于之前和之后在调用**Update**.

**LockType**参数或属性设置为**adLockOptimistic**或**adLockBatchOptimistic**打开**Recordset**对象时，使用开放式锁定。 请参阅**保守的锁定**。

**序号值**

数字顺序中的项的位置。 一个 ADO 集合，集合中的第一个项目的序号值为零 (0)。 下一项是一个 （1），依次类推。

返回顶部

## <a name="p"></a>P

**参数化的命令**

查询或命令，它使您能够执行命令前设置参数值。 例如，SQL 字符串也可以通过嵌入参数标记中的 SQL 字符串参数化 (指定？ 字符)。 然后，应用程序指定的每个参数的值，并执行命令。

**父**

分层关系的控制一端。 层次结构中，在父层次结构中有一个或多个直接位于其下方的子节点。 请参阅**父别名**、**父子关系**和**子**。

**parent-alias**

用于引用父别名。 请参阅**别名**，**父**。

**父子关系**

中的父对象是更高版本和直接与一个或多个子相关联的一级层次结构中的关系。 子元素是一个级别较低，并且必须具有一个父。 请参阅**父**，**子**。

**保留**

若要将数据保存在永久的状态，例如将**Recordset**保存到文件中。

**保守式锁定**

一种锁定类型中包含一个或多个记录，其中包括正在编辑的记录的页是对其他用户，以确保更新将进行不可用。 保守锁定行为由 OLE DB 提供程序定义。 通常情况下，记录锁定后编辑和**Update**方法完成之前保持为不可用。

**LockType**参数或属性设置为**adLockPessimistic**打开**Recordset**对象时，会启用保守式锁定。 另请参阅**开放式锁定**。

**池**

优化性能基于使用预先分配的资源，如对象或数据库连接的集合。 它是从比创建新资源池绘制现有资源更有效。

**ProgID （编程标识符）**

COM 应用程序映射到 Windows 注册表的唯一名称。 ADO 连接的 ProgID 是"ADODB。连接"。 请参阅**CLSID**， **COM**。

**代理**

特定于接口的对象，提供参数封送处理和所需的客户端调用运行在不同的执行环境中，如在不同线程上或另一个进程中一个 application 对象的通信。 代理位于与客户端和通信与相应的存根位于所调用 application 对象。 请参阅**存根**。

返回顶部

## <a name="r"></a>R

**相对 URL**

在 Internet 或 intranet 其位置是相对于指定的绝对 URL 或等效的 ADO Connection 对象的起始点指定的资源部分限定的 URL。 实际上，串联绝对和相对 Url consitute 完整 URL。 请参阅**URL**和**绝对 URL**。

**远程数据源**

数据源已存在另一台计算机，而不是本地系统上 （客户端应用程序运行位置）。

**资源记录**

包含字段的定义和文件夹或文档的描述文档源提供程序中的记录。 文档本身不包含在资源记录，但通常可以访问的默认流或包含 URL 的资源记录中的字段。 请参阅还**文档源提供程序**，**默认流**， **URL**。

**根**

中的顶层一个分层树结构。 根节点没有父，但可能有子级。 请参阅**层次结构**、**树**、**父**和**子**。

**行集**

一组数据源，所有具有相同的字段架构中的行。 行集可以表示表中的所有或某些字段。 行集还可以表示由查询或两个或多个表的联接创建的虚拟表。 在 ADO 中，由**Recordset**对象表示行集。

返回顶部

## <a name="s"></a>S

**架构**

数据库的数据库管理系统 (DBMS)，通常使用由 DBMS 提供的数据定义语言生成的说明。 架构定义的数据库，如表、 列和属性的属性。

**scope**

参考 （英文） 的对象或变量或视图或表中的记录区域的区域。 例如，可以仅在其中定义的过程中引用本地变量。 Public 变量是可从任意位置的应用程序中访问。 对象，如当前数据库，位于范围，它们是否中定义的搜索路径。 可以使用多个命令中的范围子句中指定记录的范围。

**服务提供商**

通过生成和使用数据，并增加 ADO 应用程序中的功能来封装服务的软件。 不直接公开数据提供程序，而不显示，它提供了一种服务，如查询处理。 服务提供程序可以处理数据提供程序提供的数据。 请参阅**数据提供程序**。

**定形的 Recordset**

**记录集**已专门定义其列到其他**Recordset**对象和/或其他**Recordset**对象所基于的计算的值包含而不仅仅是数据，但还 （称为章节） 的引用。

**同级**

任何两个或多个层次结构中节点上层次结构中相同的级别。 层次结构中的根节点具有没有同级。

**存储的过程**

如 SQL 语句和可选的控制流语句的代码的预编译的集合存储在名称下，并作为一个整体。 存储的过程存储在数据库;他们可以通过从应用程序的一个呼叫执行，并允许用户声明的变量、 条件执行和其他功能强大的编程功能。

**存根**

特定于接口的对象，提供参数封送处理和通信所需的应用程序对象从运行在不同的执行环境中，如在不同线程上或另一个进程中的客户端接收呼叫。 存根位于 application 对象，并具有与客户端调用它所在的相应代理进行通信。 另请参阅**代理**。

**子节点**

请参阅**子级**。

**同步操作**

下一步操作可能会启动之前完成的代码由启动的操作。 请参阅**异步操作**。

返回顶部

## <a name="t-w"></a>T-W

**树**

表示元素 （节点） 之间的分层关系的结构。 在顶级 （根） 树的没有一个节点。 下方根目录中，可以有多个子级。 每个子反过来可能其他子级，因此分支像树的父对象。 包含文档和其他文件夹的文件夹是树状结构中的典型示例。 请参阅**层次结构**、**节点**、**根**、**子**和**父**。

**URL （统一资源定位器）**

指定驻留在 Internet 或 intranet 上的资源的位置。 完整的 URL 包含配色方案 （如 FTP、 HTTP、 mailto、 文件，等等） 后, 跟一个冒号和一个服务器名称，资源 （如文档、 图片或其他文件） 的完整路径。 Url 的一些示例包括：  
  
https://www.domain.com/default.html  
ftp://ftp.server.somewhere/ftp.file  
  
ftp://ftp.server.somewhere/ftp.file  
file://Server/Share/File.doc

另请参阅**绝对 URL**和**相对 URL**。

**Web 服务器**

提供 Web 服务和页 intranet 和 Internet 用户的计算机。

返回顶部
