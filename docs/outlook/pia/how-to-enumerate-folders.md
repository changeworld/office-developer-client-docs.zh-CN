---
title: 枚举文件夹
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406251"
---
# <a name="enumerate-folders"></a>枚举文件夹

此代码示例展示了如何通过循环访问文件夹集合来枚举文件夹。

## <a name="example"></a>示例

> [!NOTE] 
> 下面的代码示例摘录自 [Microsoft Office Outlook 2007 应用程序编程](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)。

在下面的代码示例中，EnumerateFoldersInDefaultStore 先使用 [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) 方法来获取默认存储的根文件夹。 然后，它对根文件夹调用 EnumerateFolders 方法。 EnumerateFolders 需要使用根文件夹，并浏览根文件夹所表示的默认存储的文件夹。 EnumerateFolders 先使用 [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) 属性来获取根 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) 对象的子文件夹。 然后，此代码示例递归调用 EnumerateFolders，以枚举层次结构中的所有文件夹。 最后，EnumerateFolders 将每个 **Folder** 的 [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) 属性写入 [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) 集合的跟踪侦听器中。

如果使用 Visual Studio 测试此代码示例，必须先添加对 Microsoft Outlook 15.0 对象库组件的引用，并在导入 **Microsoft.Office.Interop.Outlook** 命名空间时指定 Outlook 变量。 不得将 **using** 语句直接添加到此代码示例中的函数前面，这个语句必须后跟公共类声明。 下面的代码行展示了如何在 C\# 中执行导入和分配操作。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>另请参阅

- [文件夹](folders.md)

