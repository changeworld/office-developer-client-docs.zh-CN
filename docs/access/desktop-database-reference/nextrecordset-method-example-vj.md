---
title: NextRecordset 方法示例 (VJ++)
TOCTitle: NextRecordset method example (VJ++)
ms:assetid: 1803ce0e-43a6-0571-5703-525f1d2e29ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248930(v=office.15)
ms:contentKeyID: 48543457
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 930abda7c7efcc0c223f56547e016f8732ffa276
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873629"
---
# <a name="nextrecordset-method-example-vj"></a>NextRecordset 方法示例 (VJ++)


**适用于**： Access 2013、 Office 2013

本示例使用 [NextRecordset](nextrecordset-method-ado.md) 方法来查看记录集中的数据，该方法使用由三个单独的 **SELECT** 语句构成的复合命令语句。

```java 
 
// BeginNextRecordsetJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class NextRecordsetX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 NextRecordsetX(); 
 System.exit(0); 
 } 
 // NextRecordsetX Function 
 static void NextRecordsetX() 
 { 
 // Define ADO Object 
 Recordset rstCompound = null; 
 
 // Declarations 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 String strCnn; 
 int intCount; 
 int intDisplayRecords = 15; 
 int intRecordCount; 
 
 try 
 { 
 // Open compound recordset. 
 strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 rstCompound = new Recordset(); 
 rstCompound.open("select * from Authors;" + 
 "select * from stores;" + 
 "select * from jobs", strCnn, AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY,AdoEnums.CommandType.TEXT); 
 
 // Display results from each select statement. 
 intCount=1; 
 
 while (rstCompound != null) 
 { 
 System.out.println( 
 "Contents of recordset #" + intCount + "\n"); 
 intRecordCount = 0; 
 
 while(!rstCompound.getEOF()) 
 { 
 System.out.println( 
 rstCompound.getField(0).getString()+" " + 
 rstCompound.getField(1).getString()); 
 intRecordCount++; 
 
 rstCompound.moveNext(); 
 if ( intRecordCount == intDisplayRecords) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 intRecordCount = 0; 
 } 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 rstCompound = rstCompound.nextRecordset(); 
 
 intCount++; 
 } 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a recordset. check for the null pointer first 
 if(rstCompound!=null) 
 { 
 PrintProviderError(rstCompound.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 catch(java.lang.NullPointerException ne) 
 { 
 System.out.println("Error Description: " + ne.getMessage()); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstCompound != null) 
 if (rstCompound.getState() == 1) 
 rstCompound.close(); 
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
// EndNextRecordsetJ 
```

