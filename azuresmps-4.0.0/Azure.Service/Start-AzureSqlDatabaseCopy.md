---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413059"
---
# Start-AzureSqlDatabaseCopy

## 簡介
啟動 Azure SQL 資料庫的複製作業。

## 語法

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Start-AzureSqlDatabaseCopy** Cmdlet 會啟動一次複製作業或特定 Azure SQL Database 的連續複製作業。
此 Cmdlet 並非專案。

原始資料庫是源資料庫。
此副本是次要或目標資料庫。
對於連續的複製，來源和目標資料庫不能位於同一個伺服器上，而主託管來源和目標資料庫的伺服器必須是相同訂閱的一部分。

如果您未指定 *ContinuousCopy* 參數，此 Cmdlet 會建立源資料庫的一次副本。
收到回應時，作業可能仍在進行中。
您可以使用 Cmdlet 或 Cmdlet Get-AzureSqlDatabaseCopy或Get-AzureSqlDatabaseOperation作業。

如果您指定 *ContinuousCopy，* 此 Cmdlet 會建立源資料庫的連續副本。
收到回應時，作業將會進行中。
您可以使用 **Get-AzuresqlDatabaseCopy** 或 **Get-AzureSqlDatabaseOperation 監控作業**。

您可以將連續的複製建立為線上或離線資料庫。
線上連續副本可用來設定 Azure SQL database Geo-Replication活動資料庫 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 。
離線連續副本可用來設定 Azure SQL database Geo-Replication標準資料夾 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 。

## 例子

### 範例 1：排程連續資料庫副本
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

此命令會在伺服器上排程名為 lpqd0zbr8y 的 Orders 資料庫的連續副本。
該命令會在伺服器上建立名為 bk0b8kf658 的目標資料庫。

### 範例 2：在同一個伺服器上建立一次副本
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

此命令會在伺服器上名為 lpqd0zbr8y 的 Orders 建立一次資料庫的一次副本。
該命令會在同一個伺服器上建立名為 OrdersCopy 的複製。

### 範例 3：排程連續離線資料庫副本
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

此命令會在伺服器上排程名為 lpqd0zbr8y 的 Orders 資料庫的連續副本。
此命令會在伺服器上建立一個名為 bk0b8kf658 的離線目標資料庫。

## 參數

### -ContinuousCopy
表示資料庫複本為複本資料庫 (複本) 。
同一伺服器不支援連續複製。
如果未指定此參數，則執行一次複製。
對於一次複製，來源和合作夥伴資料庫必須位於同一個伺服器上。

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -資料庫
指定代表來源 Azure SQL Database 的物件。
此參數接受管線輸入。

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
指定源資料庫的名稱。

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -強制
強制執行命令，但不要求使用者確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Offline2010
指定連續的複製為被動副本，而不是使用中複製。
如果源資料庫是 Standard edition 資料庫，則此參數為必填項。
如果指定此參數，則必須同時指定 *ContinuousCopy。*

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
指定目標資料庫的名稱。
如果您指定 *ContinuousCopy* 參數 *，PartnerDatabase* 的值必須與源資料庫的名稱相符。
如果您未指定 *ContinuousCopy，* 則必須指定目標資料庫的名稱，此名稱可能會與源資料庫名稱不同。

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
指定主託管目標資料庫的伺服器名稱。
此伺服器必須與源資料庫伺服器在同一個 Azure 訂閱中。

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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
指定源資料庫所在的伺服器名稱。

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

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 輸出

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## 筆記
* 驗證：此 Cmdlet 需要憑證式驗證。 有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。
* 監控：若要檢查伺服器上一或多個連續的複製關係狀態，請使用 **Get-AzureSqlDatabaseCopy** Cmdlet。 若要驗證連續複製關係的來源和目標作業狀態，請使用 **Get-AzureSqlDatabaseOperation** Cmdlet。

## 相關連結

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[啟動資料庫複製](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


