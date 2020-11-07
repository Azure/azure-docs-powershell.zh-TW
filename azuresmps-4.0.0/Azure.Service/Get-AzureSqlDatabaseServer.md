---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967017"
---
# Get-AzureSqlDatabaseServer

## 摘要
取得有關 Azure SQL 資料庫伺服器的資訊。

## 句法

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseServer** Cmdlet 會在目前的訂閱中取得 Azure SQL Database Server 實例的相關資訊。
如果您依名稱指定伺服器，這個 Cmdlet 會傳回包含該伺服器相關資訊的物件。
否則，Cmdlet 會傳回所有伺服器的相關資訊。

## 示例

### 範例1：取得所有伺服器的相關資訊
```
PS C:\> Get-AzureSqlDatabaseServer
```

這個命令會傳回目前訂閱中所有 Azure SQL Database Server 實例的相關資訊。

### 範例2：取得特定伺服器的相關資訊
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

這個命令會傳回名為 lpqd0zbr8y 伺服器的相關資訊。

## 參數

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
指定此 Cmdlet 移除的伺服器名稱。
指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext

## 輸出

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## 筆記

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[清單伺服器](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[新-AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[移除-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


