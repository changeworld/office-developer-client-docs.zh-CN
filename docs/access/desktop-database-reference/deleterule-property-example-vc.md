---
title: DeleteRule 属性示例 (VC++)
TOCTitle: DeleteRule property example (VC++)
ms:assetid: 364efee7-d579-57df-aeb0-fa352a72d704
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249122(v=office.15)
ms:contentKeyID: 48544164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97e2e1d9a9c801fc7982ec9bdd84e060a03ceccf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875481"
---
# <a name="deleterule-property-example-vc"></a>DeleteRule 属性示例 (VC++)


**适用于**： Access 2013、 Office 2013

本示例演示 [Key](deleterule-property-adox.md) 对象的 [DeleteRule](key-object-adox.md) 属性。代码将追加一个新 [Table](table-object-adox.md)，然后定义一个新主键，同时将 **DeleteRule** 设置为 **adRICascade** 。

```cpp 
 
// BeginDeleteRuleCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void DeleteRuleX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 DeleteRuleX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// DeleteRuleX Function // 
// // 
////////////////////////////////////////////////////////// 
void DeleteRuleX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _KeyPtr m_pKeyPrimary = NULL; 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTblNew = NULL; 
 
 // Define string variables. 
 _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data source = 'c:\\Program Files\\Microsoft Office" 
 "\\Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pKeyPrimary.CreateInstance(__uuidof(Key))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 TESTHR(hr = m_pTblNew.CreateInstance(__uuidof(Table))); 
 
 // Connect the catalog. 
 m_pCatalog->PutActiveConnection(strcnn); 
 
 // Name new table. 
 m_pTblNew->Name = "NewTable"; 
 
 // Append a numeric and a text field to new table. 
 m_pTblNew->Columns->Append("NumField",adInteger,20); 
 m_pTblNew->Columns->Append("TextField",adVarWChar,20); 
 
 // Append the new table. 
 m_pCatalog->Tables->Append(_variant_t((IDispatch*)m_pTblNew)); 
 printf("Table 'NewTable' is added.\n"); 
 
 // Define the Primary key. 
 m_pKeyPrimary->Name = "NumField"; 
 m_pKeyPrimary->Type = adKeyPrimary; 
 m_pKeyPrimary->RelatedTable = "Customers"; 
 m_pKeyPrimary->Columns->Append("NumField",adInteger,20); 
 m_pKeyPrimary->Columns->GetItem("NumField")->RelatedColumn = 
 "CustomerId"; 
 m_pKeyPrimary->DeleteRule = adRICascade; 
 
 //to pass an optional column parameter to Key's Apppend method 
 _variant_t vOptional; 
 vOptional.vt = VT_ERROR; 
 vOptional.scode = DISP_E_PARAMNOTFOUND; 
 
 // Append the primary key. 
 m_pCatalog->Tables->GetItem("NewTable")->Keys->Append( 
 _variant_t((IDispatch*)m_pKeyPrimary), 
 adKeyPrimary,vOptional,L"",L""); 
 
 // Delete the table as this is a demonstration. 
 m_pCatalog->Tables->Delete(m_pTblNew->Name); 
 printf("Table 'NewTable' is deleted.\n"); 
 } 
 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 
 catch(...) 
 { 
 cout << "Error occured in include files...."<< endl; 
 } 
} 
// EndDeleteRuleCpp 
```

