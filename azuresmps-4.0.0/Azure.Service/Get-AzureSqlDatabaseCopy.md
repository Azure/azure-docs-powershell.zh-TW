---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967741"
---
# Get-AzureSqlDatabaseCopy

## 摘要
檢查複製關聯的狀態。

## 句法

### ByServerNameOnly (預設) 
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseCopy** Cmdlet 會檢查一或多個活動複本關聯的狀態。
在執行 Start-AzureSqlDatabaseCopy 或 Stop-AzureSqlDatabaseCopy Cmdlet 之後，請執行這個 Cmdlet。
您可以檢查特定的複本關聯性、所有複製關聯，或是複製關聯的篩選清單，例如特定目標伺服器上的所有複本。
您可以在裝載來源或目標資料庫的伺服器上執行這個 Cmdlet。

這個 Cmdlet 是同步的。
這個 Cmdlet 會封鎖 Azure PowerShell 主控台，直到它傳回 status 物件為止。

*PartnerServer* 和 *PartnerDatabase* 參數是選擇性的。
如果您沒有指定任何一個參數，這個 Cmdlet 會傳回結果表格。
若只要查看特定資料庫的狀態，請同時指定這兩個參數。

## 示例

### 範例1：取得資料庫的複製狀態
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，取得名為 [訂單] 的資料庫狀態。
*PartnerServer* 參數會將這個命令限制在 bk0b8kf658 伺服器。

### 範例2：取得伺服器上所有複本的狀態 serverGet 伺服器上所有複本的狀態
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

這個命令會取得伺服器上名為 lpqd0zbr8y 的所有活動複本狀態。

## 參數

### -資料庫
指定代表來源 Azure SQL 資料庫的物件。
這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
指定代表資料庫的物件。
這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。
這個參數接受管線輸入。

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定源資料庫的名稱。
這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
指定次要資料庫的名稱。
如果在 sys.dm_database_copies 動態管理檢視中找不到這個資料庫，這個 Cmdlet 會傳回一個空的狀態物件。

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
指定主持目標資料庫的伺服器名稱。
如果在 sys.dm_database_copies 動態管理檢視中找不到這個伺服器，這個 Cmdlet 會傳回一個空的狀態物件。

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
指定資料庫複本所在之伺服器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### WindowsAzure. SqlDatabase. DatabaseCopy

### SqlDatabase.. Database （WindowsAzure）

## 輸出

### WindowsAzure. SqlDatabase. DatabaseCopy

## 筆記
* 驗證：此 Cmdlet 需要以憑證為基礎的驗證。 如需如何使用以憑證為基礎的驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL 資料庫 Cmdlet](./Azure.SQLDatabase.md)

[開始-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[停止 AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


