---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967291"
---
# Start-AzureSqlDatabaseCopy

## 摘要
啟動 Azure SQL 資料庫的複製作業。

## 句法

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

## 說明
**AzureSqlDatabaseCopy** Cmdlet 會啟動一次性複製作業或特定 Azure SQL 資料庫的連續複製作業。
這個 Cmdlet 不是事務性的。

原始資料庫是源資料庫。
複本是次要或目標資料庫。
針對連續複本，來源和目標資料庫不能位於同一個伺服器上，而且主持來源和目標資料庫的伺服器必須屬於相同的訂閱。

如果您沒有指定 *ContinuousCopy* 參數，這個 Cmdlet 會建立來源資料庫的一次性複本。
收到回應時，仍可進行該作業。
您可以使用 Get-AzureSqlDatabaseCopy 或 Get-AzureSqlDatabaseOperation Cmdlet 來監視作業。

如果您指定 *ContinuousCopy* ，這個 Cmdlet 會建立源資料庫的連續複本。
收到回應時，作業將會進行中。
您可以使用 **AzureSqlDatabaseCopy** 或 **AzureSqlDatabaseOperation** 來監視作業。

您可以建立連續複本做為線上或離線資料庫。
線上連續複本是用來設定 Azure SQL Database 的作用中 Geo-Replication https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 。
離線連續副本是用來設定 Azure SQL Database 的標準 Geo-Replication https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 。

## 示例

### 範例1：排程連續資料庫複製
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，排程一個名為 [訂單] 的資料庫連續複本。
該命令會在伺服器上建立名為 bk0b8kf658 的目標資料庫。

### 範例2：在同一個伺服器上建立一次性複本
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，建立名為「訂單」的單一時間複本。
該命令會在同一台伺服器上建立名為 OrdersCopy 的複本。

### 範例3：排程連續離線資料庫複本
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，排程一個名為 [訂單] 的資料庫連續複本。
這個命令會在伺服器上建立名為 bk0b8kf658 的離線目標資料庫。

## 參數

### -ContinuousCopy
表示資料庫複本將是複本資料庫 (的連續複本) 。
在同一個伺服器中不支援連續複製。
如果未指定此參數，則會執行一次性複本。
若是一次性複本，來源與夥伴資料庫必須在同一個伺服器上。

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
指定代表來源 Azure SQL 資料庫的物件。
這個參數接受管線輸入。

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

### -Force
強制執行命令，而不要求使用者確認。

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

### -OfflineSecondary
指定連續複製是一個被動複本，而不是使用中的複本。
如果源資料庫是標準版本的資料庫，則需要此參數。
如果指定此參數，則也必須指定 *ContinuousCopy* 。

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
如果您指定 *ContinuousCopy* 參數， *PartnerDatabase* 的值必須與源資料庫的名稱相符。
如果您沒有指定 *ContinuousCopy* ，您必須指定目標資料庫的名稱，這可能與源資料庫名稱不同。

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
指定主持目標資料庫的伺服器名稱。
此伺服器必須與源資料庫伺服器位於相同的 Azure 訂閱中。

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
指定源資料庫所在之伺服器的名稱。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### SqlDatabase.. Database （WindowsAzure）

## 輸出

### WindowsAzure. SqlDatabase. DatabaseCopy

## 筆記
* 驗證：此 Cmdlet 需要以憑證為基礎的驗證。 如需如何使用以憑證為基礎的驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。
* 監視：若要檢查伺服器上作用中的一或多個連續複本關聯的狀態，請使用 **AzureSqlDatabaseCopy** Cmdlet。 若要確認連續複製關聯之來源和目標上的作業狀態，請使用 **AzureSqlDatabaseOperation** Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[開始資料庫複製](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL 資料庫 Cmdlet](./Azure.SQLDatabase.md)

[AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[停止 AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


