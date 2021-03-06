---
title: GetString 方法示例 (VJ++)
TOCTitle: GetString method example (VJ++)
ms:assetid: 83d5ab6d-a092-f8ed-81e7-b93922cda93d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249573(v=office.15)
ms:contentKeyID: 48546018
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e94bc5d10f3824dbc63f35706c27f7c6a8e43d8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878183"
---
# <a name="getstring-method-example-vj"></a>GetString 方法示例 (VJ++)


**适用于**： Access 2013、 Office 2013

本示例演示 [GetString](getstring-method-ado.md) 方法。

假设您正在调试某个数据访问问题，并且需要一种快速、简便的方法来显示较小 [Recordset](recordset-object-ado.md) 的当前内容。

```java 
 
// BeginGetStringJ 
// The WFC class includes the ADO objects. 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class GetStringX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 GetStringX (); 
 System.exit(0); 
 } 
 
 // GetStringX function 
 static void GetStringX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 String strOutput; 
 
 try 
 { 
 // Get the user input for state. 
 System.out.println( 
 "Enter a state (CA, IN, KS, MD, MI, OR, TN, UT): "); 
 String strState = in.readLine().trim(); 
 String strQuery = 
 "SELECT au_fname, au_lname, address, city FROM Authors " + 
 "WHERE state = '" + strState + "'"; 
 
 // Open recordset with data from Authors table. 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.open(strQuery, 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 if (rstAuthors.getRecordCount() > 0) 
 { 
 // Use all defaults: get all rows, TAB column delimiter, 
 // CARRIAGE RETURN 
 // row delimiter, empty-string null delimiter. 
 strOutput = 
 rstAuthors.getString(AdoEnums.StringFormat.CLIPSTRING, 
 rstAuthors.getRecordCount(), 
 "\t ", 
 "\n", 
 "").trim(); 
 System.out.println("\nState = '" + strState + "'" + 
 "\n\n" + 
 "Name Address City" + 
 "\n"); 
 System.out.println(strOutput); 
 } 
 else 
 System.out.println("\nNo rows found for state = '" + 
 strState + "'\n"); 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndGetStringJ 
```

