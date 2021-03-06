---
title: CursorType、LockType 和 EditMode 属性示例 (VJ++)
TOCTitle: CursorType, LockType, and EditMode properties example (VJ++)
ms:assetid: bfe87584-4909-8974-b207-4a0c363c5155
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249932(v=office.15)
ms:contentKeyID: 48547497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 126d52af8a83e23b3298b8f0fb4600e603832a15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873948"
---
# <a name="cursortype-locktype-and-editmode-properties-example-vj"></a>CursorType、LockType 和 EditMode 属性示例 (VJ++)


**适用于**： Access 2013、 Office 2013

此示例演示如何在打开 [Recordset](cursortype-property-ado.md) 前设置 [CursorType](locktype-property-ado.md) 和 [LockType](recordset-object-ado.md) 属性。它还演示在各种情况下 [EditMode](editmode-property-ado.md) 属性的值。若要运行此过程，必须使用 EditModeOutput 函数。

```java 
 
// BeginEditModeJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class EditModeX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 EditModeX (); 
 System.exit(0); 
 } 
 
 // EditModeX function 
 
 static void EditModeX () 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 // Open recordset with data from Employees table. 
 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstEmployees = new Recordset(); 
 rstEmployees.setActiveConnection(cnConn1); 
 rstEmployees.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 rstEmployees.setCursorType(AdoEnums.CursorType.STATIC); 
 rstEmployees.setLockType(AdoEnums.LockType.BATCHOPTIMISTIC); 
 rstEmployees.open("employee", cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TABLE); 
 
 // Show the EditMode property under different editing states. 
 
 rstEmployees.addNew(); 
 rstEmployees.getField("emp_id").setString("T-T55555M"); 
 rstEmployees.getField("fname").setString("temp_fname"); 
 rstEmployees.getField("lname").setString("temp_lname"); 
 EditModeOutput("After AddNew:", rstEmployees.getEditMode()); 
 rstEmployees.updateBatch(); 
 EditModeOutput("After Update:", rstEmployees.getEditMode()); 
 rstEmployees.getField("fname").setString("test"); 
 EditModeOutput("After Edit:", rstEmployees.getEditMode()); 
 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Delete new record because this is a demonstration. 
 cnConn1.execute( 
 "DELETE FROM employee WHERE emp_id = 'T-T55555M'"); 
 
 // Cleanup objects before exit. 
 rstEmployees.close(); 
 cnConn1.close(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (cnConn1==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
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
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
 } 
 } 
 
 // EditModeOutput Function 
 
 static void EditModeOutput(String strTemp, int intEditMode) 
 { 
 String strMessage=""; 
 // Print report based on the value of the EditMode 
 // property. 
 
 System.out.println("\n" + strTemp); 
 strMessage ="\n\tEditMode = "; 
 switch(intEditMode) 
 { 
 case AdoEnums.EditMode.NONE : 
 strMessage+="adEditNone"; 
 break; 
 case AdoEnums.EditMode.INPROGRESS : 
 strMessage+="adEditInProgress"; 
 break; 
 case AdoEnums.EditMode.ADD : 
 strMessage+="adEditAdd"; 
 break; 
 default : 
 break; 
 } 
 System.out.println(strMessage); 
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
// EndEditModeJ 
```

