---
title: CacheSize 属性示例 (VJ++)
TOCTitle: CacheSize property example (VJ++)
ms:assetid: f51cbf17-2944-91ea-b233-18a897ab8f1f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250248(v=office.15)
ms:contentKeyID: 48548704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 714b20aad4c03e5e5735d38dd6e4202a4c732844
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881809"
---
# <a name="cachesize-property-example-vj"></a>CacheSize 属性示例 (VJ++)


**适用于**： Access 2013、 Office 2013

此示例使用 [CacheSize](cachesize-property-ado.md) 属性显示在使用和不使用 30 条记录大小的缓存的情况下执行一个操作时的性能差异。

```java 
 
// BeginCacheSizeJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class CacheSizeX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 CacheSizeX(); 
 System.exit(0); 
 } 
 
 // CacheSizeX function 
 
 static void CacheSizeX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstRoySched = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 long timeStart; 
 long timeEnd; 
 float timeNoCache; 
 float timeCache; 
 int intLoop; 
 String strTemp; 
 
 try 
 { 
 // Open the RoySched table. 
 rstRoySched = new Recordset(); 
 rstRoySched.open("roysched", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Enumerate the Recordset object twice and record 
 // the elapsed time. 
 
 timeStart = System.currentTimeMillis(); 
 for ( intLoop = 0; intLoop < 2; intLoop++) 
 { 
 rstRoySched.moveFirst(); 
 while (!rstRoySched.getEOF()) 
 { 
 // Execute a simple operation for the 
 // performance test. 
 strTemp = rstRoySched.getField("title_id").getString(); 
 rstRoySched.moveNext(); 
 } 
 
 } 
 
 timeEnd = System.currentTimeMillis(); 
 timeNoCache =(float)(timeEnd - timeStart)/1000f; 
 
 // Cache records in groups of 30 records. 
 rstRoySched.moveFirst(); 
 rstRoySched.setCacheSize(30); 
 timeStart = System.currentTimeMillis(); 
 
 // Enumerate the Recordset object twice and record 
 // the elapsed time. 
 for ( intLoop = 0; intLoop < 2; intLoop++) 
 { 
 rstRoySched.moveFirst(); 
 while (!rstRoySched.getEOF()) 
 { 
 // Execute a simple operation for the 
 // performance test. 
 
 strTemp = rstRoySched.getField("title_id").getString(); 
 rstRoySched.moveNext(); 
 } 
 
 } 
 
 timeEnd = System.currentTimeMillis(); 
 timeCache = (float)(timeEnd - timeStart)/1000f; 
 
 // Display performance results. 
 System.out.println("\nCaching Performance Results:"); 
 System.out.println("\n\tNo Cache: " + timeNoCache + " seconds"); 
 System.out.println("\n\t30-record cache: " + timeCache + 
 " seconds"); 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstRoySched.getActiveConnection()==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstRoySched != null) 
 { 
 PrintProviderError(rstRoySched.getActiveConnection()); 
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
 if (rstRoySched != null) 
 if (rstRoySched.getState() == 1) 
 rstRoySched.close(); 
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
 
// EndCacheSizeJ 
```

