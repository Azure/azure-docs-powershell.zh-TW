---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402417"
---
# Get-AzureSqlDatabaseCopy

## 簡介
檢查複製關係的狀態。

## 語法

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

## 描述
**Get-AzureSqlDatabaseCopy** Cmdlet 會檢查一或多個使用中複製關係的狀態。
執行此 Cmdlet 之後，Start-AzureSqlDatabaseCopy或Stop-AzureSqlDatabaseCopy Cmdlet。
您可以檢查特定的複本關係、所有複製關係或篩選的複製關係清單，例如特定目標伺服器上的所有複本。
您可以在主管來源或目標資料庫的伺服器上執行此 Cmdlet。

此 Cmdlet 是同步的。
Cmdlet 會區塊 Azure PowerShell 主控台，直到它返回狀態物件。

*PartnerServer 和* *PartnerDatabase* 參數為選擇性。
如果您未指定任一參數，此 Cmdlet 會返回結果表。
若要只查看特定資料庫的狀態，請指定這兩個參數。

## 例子

### 範例 1：取得資料庫的複製狀態
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

此命令會在伺服器上獲得名為 lpqd0zbr8y 的 Orders 資料庫狀態。
*PartnerServer* 參數將此命令限制為 bk0b8kf658 伺服器。

### 範例 2：取得伺服器上所有複本的狀態取得伺服器上所有複本的狀態
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

此命令會在伺服器上獲得所有使用中複本的狀態，名稱為 lpqd0zbr8y。

## 參數

### -資料庫
指定代表來源 Azure SQL Database 的物件。
此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。

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
此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。
此參數接受管線輸入。

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
此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。

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
如果在動態管理sys.dm_database_copies找不到此資料庫，此 Cmdlet 會返回空白的狀態物件。

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
指定主託管目標資料庫的伺服器名稱。
如果在動態管理sys.dm_database_copies找不到此伺服器，此 Cmdlet 會返回空白的狀態物件。

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
如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。

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
指定資料庫副本所在的伺服器名稱。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 輸出

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## 筆記
* 驗證：此 Cmdlet 需要憑證式驗證。 有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


