---
title: Provider 和 DefaultDatabase 属性示例 (VC++)
TOCTitle: Provider and DefaultDatabase Properties Example (VC++)
ms:assetid: 21c38be4-3906-cee8-b77b-300f1226392a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248995(v=office.15)
ms:contentKeyID: 48543687
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0aa8bcc1af7efda16fc6d8e23ce0bf8a3e04005d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25467078"
---
# <a name="provider-and-defaultdatabase-properties-example-vc"></a>Provider 和 DefaultDatabase 属性示例 (VC++)


**适用于**： Access 2013 |Office 2013

本示例演示 [Provider](provider-property-ado.md) 属性，将打开三个使用不同提供程序的 [Connection](connection-object-ado.md) 对象。它还使用 [DefaultDatabase](defaultdatabase-property-ado.md) 属性来设置 Microsoft ODBC Provider 的默认数据库。

```cpp 
 
// BeginProviderCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProviderX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProviderX(); 
 
 ::CoUninitialize(); 
} 
 
///////////////////////////////// 
// // 
// ProviderX Function // 
// // 
///////////////////////////////// 
 
void ProviderX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection1 = NULL; 
 _ConnectionPtr pConnection2 = NULL; 
 _ConnectionPtr pConnection3 = NULL; 
 
 try 
 { 
 // Open a Connection using the Microsoft ODBC provider. 
 TESTHR(pConnection1.CreateInstance(__uuidof(Connection))); 
 pConnection1->ConnectionString = "driver={SQL Server};" 
 "server='MySqlServer';user id='MyUserId';password='MyPassword';"; 
 pConnection1->Open("","","",adConnectUnspecified); 
 pConnection1->DefaultDatabase = "pubs"; 
 
 // Display the provider 
 printf("\n\nConnection1 provider: %s \n\n", 
 (LPCSTR)pConnection1->Provider); 
 
 // Open a connection using the OLE DB Provider for Microsoft Jet. 
 TESTHR(pConnection2.CreateInstance(__uuidof(Connection))); 
 pConnection2->Provider = "Microsoft.Jet.OLEDB.4.0"; 
 
 char *sConn = "c:\\Program Files\\Microsoft Office\\Office\\" 
 "Samples\\Northwind.mdb"; 
 
 pConnection2->Open(sConn,"admin","",NULL); 
 
 // Display the provider 
 printf("Connection2 provider: %s \n\n",(LPCSTR)pConnection2-> 
 Provider); 
 
 // Open a Connection using the Microsoft SQL Server provider. 
 TESTHR(pConnection3.CreateInstance(__uuidof(Connection))); 
 pConnection3->Provider = "sqloledb"; 
 pConnection3->Open("Data Source='MySqlServer';Initial Catalog='pubs';", 
 "MyUserId","MyPassword",NULL); 
 
 // Display the provider. 
 printf("Connection3 provider: %s\n\n",(LPCSTR)pConnection3-> 
 Provider); 
 } 
 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintProviderError(pConnection1); 
 if(pConnection2) PrintProviderError(pConnection2); 
 if(pConnection3) PrintProviderError(pConnection3); 
 PrintComError(e); 
 } 
 
 if (pConnection1) 
 if (pConnection1->State == adStateOpen) 
 pConnection1->Close(); 
 if (pConnection2) 
 if (pConnection2->State == adStateOpen) 
 pConnection2->Close(); 
 if (pConnection3) 
 if (pConnection3->State == adStateOpen) 
 pConnection3->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0;i < nCount;i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////////////////// 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print COM errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
// EndProviderCpp 
```
