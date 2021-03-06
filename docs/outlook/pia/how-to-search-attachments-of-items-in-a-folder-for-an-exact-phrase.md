---
title: 在文件夹中项的附件内搜索完全匹配的某短语
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 915ddd65e8227f6cc720c4494ed1767deed121b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406153"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>在文件夹中项的附件内搜索完全匹配的某短语

此代码示例在收件箱中项的附件内搜索完全匹配的字符串“office”。

## <a name="example"></a>示例

此代码示例使用 DAV 搜索和定位 (DASL) 语法来指定查询。 为了构造筛选器，此代码示例先检查默认存储中是否已启用“即时搜索”，以确定是否使用 **ci\_phrasematch** 关键字在所有附件中搜索完全匹配的短语“office”。 然后，此代码示例将筛选器应用于收件箱的 [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) 方法，并获取 [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) 对象中的结果。 接下来，此代码示例显示 **Table** 中每个返回项的主题。

此代码示例使用命名空间表示法 https://schemas.microsoft.com/mapi/proptag/0x0EA5001E 指定项的 **Attachments** 属性。 使用 **ci\_phrasematch** 关键字的语法为：

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

如果使用 Visual Studio 测试此代码示例，必须先添加对 Microsoft Outlook 15.0 对象库组件的引用，并在导入 **Microsoft.Office.Interop.Outlook** 命名空间时指定 Outlook 变量。 不得将 **Imports** 或 **using** 语句直接添加到此代码示例中的函数前面，这两个语句必须后跟公共类声明。 下面几段代码行展示了如何在 Visual Basic 和 C\# 中执行导入和分配操作。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a>另请参阅

- [搜索和筛选](search-and-filter.md)

