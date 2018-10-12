---
title: WillConnect 事件 (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5493593998bf5484bd2247b32e114809b805fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468870"
---
# <a name="willconnect-event-ado"></a>WillConnect 事件 (ADO)


**适用于**： Access 2013 |Office 2013


**WillConnect** 事件在连接启动之前调用。

## <a name="syntax"></a>语法

WillConnect*ConnectionString*，*用户 Id*，*密码*、*选项*、 *adStatus*、 *pConnection*

## <a name="parameters"></a>参数

  - *ConnectionString*

  - **字符串型** ，包含挂起的连接的连接信息。

  - *用户 Id*

  - **字符串型** ，包含挂起的连接的用户名。

  - *Password*

  - **字符串型** ，包含挂起的连接的密码。

  - *Options*

  - **长整型**值，指示提供程序应如何对 *ConnectionString* 求值。您仅有的选项为 **adAsyncOpen**。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    调用此事件时，默认情况下该参数设置为 **adStatusOK** 。如果此事件无法请求取消挂起的操作，则该参数设置为 **adStatusCantDeny** 。
    
    在此事件返回之前，将该参数设置为 **adStatusUnwantedEvent** 可以阻止随后进行通知。将该参数设置为 **adStatusCancel** 将请求导致取消此通知的连接操作。

  - *pConnection*

  - 为其应用该事件通知的 [Connection](connection-object-ado.md) 对象。 **WillConnect** 事件处理程序对 **Connection** 的参数所做的更改对 **Connection** 将没有效果。

## <a name="remarks"></a>备注

调用 **WillConnect** 时，*ConnectionString*、*UserID*、*Password* 和 *Options* 参数设置为由导致该事件的操作（挂起的连接）建立的值，且这些值可以在事件返回之前更改。**WillConnect** 可以返回取消挂起的连接的请求。

取消此事件时，将调用*adStatus*参数设置为**adStatusErrorsOccurred** **ConnectComplete** 。
