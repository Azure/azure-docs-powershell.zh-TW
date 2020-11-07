---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967849"
---
# Stop-AzureSqlDatabaseCopy

## 摘要
終止連續複製關聯。

## 句法

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseCopy** Cmdlet 會終止連續複製關聯。
這個 Cmdlet 會停止源資料庫與次要或目標資料庫之間的資料移動，然後將次要資料庫的狀態變更為獨立的線上資料庫。

您可以透過兩種方式來結束連續複製關聯、終止或計畫終止及強制終止（可能會造成資料遺失）。
在託管來源資料庫的伺服器上，您可以在終止或強制終止模式下執行此 Cmdlet。
在裝載次要資料庫的伺服器上，您必須使用強制終止模式。

已計畫的終止會等到源資料庫上的所有已提交事務（在您執行 Cmdlet 時）已複製到次要資料庫為止。
強制終止並不會等待複製任何未完成的已提交事務，而且可能會在次要資料庫中造成可能的資料遺失。

當複製狀態為 [擱置中] 時，只有強制終止才能成功結束連續複製關聯。
如果複製狀態為 [擱置中]，則不支援不強制的終止。

## 示例

### 範例1：終止連續複製關聯
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，終止名為 [訂單] 的資料庫連續複製關聯。
名為 bk0b8kf658 的伺服器會託管次要資料庫。

### 範例2：強行終止連續複製關聯
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

第一個命令會取得名為 lpqd0zbr8y 的伺服器上名為 [訂單] 的資料庫複製關係。

第二個命令會強制終止託管次要資料庫之伺服器的連續複製關聯。

## 參數

### -資料庫
指定代表來源 Azure SQL 資料庫的物件。
這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。

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
這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。
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
指定資料庫的名稱。
這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。

```yaml
Type: String
Parameter Sets: ByDatabaseName
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

### -ForcedTermination
表示此 Cmdlet 會導致連續複製關聯的強制終止。
強制終止可能會造成資料遺失。
若要在託管目標資料庫的伺服器上執行此 Cmdlet，您必須指定此參數。
若要在託管來源資料庫的伺服器上執行這個 Cmdlet，如果次要資料庫無法使用，您必須指定此參數。

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

### -PartnerDatabase
指定次要資料庫的名稱。
如果您指定名稱，則它必須符合源資料庫的名稱。

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
指定主持目標資料庫的伺服器名稱。

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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

### WindowsAzure. SqlDatabase. DatabaseCopy

### SqlDatabase.. Database （WindowsAzure）

## 輸出

### 所有

## 筆記
* 驗證：此 Cmdlet 需要以憑證為基礎的驗證。 如需如何使用憑證式驗證來設定目前訂閱的範例，請參閱 **AzureSqlDatabaseServerCoNtext** Cmdlet。
* 限制：在託管次要資料庫的伺服器上，只支援強制終止。
* 在前一個次要資料庫上終止的影響：終止之後，次要資料庫成為獨立的資料庫。 如果在次要資料庫上已完成播種，則在終止之後，就會開啟此資料庫以供完全存取。 如果來源資料庫是讀寫資料庫，則前者的次要資料庫也會成為讀寫資料庫。

  如果正在進行衍生作業，則會中止播種，而前者在託管次要資料庫的伺服器上永遠不會顯示。

* 您可以將源資料庫設為唯讀模式。 這可保證在終止後，來源和次要資料庫已同步處理，並確保終止期間不會提交任何事務。 終止結束後，請將來源設回到讀寫模式。 或者，您也可以將先前的次要資料庫設定為讀寫模式。
* 監視：若要確認連續複製關聯之來源和目標上的作業狀態，請使用 **AzureSqlDatabaseOperation** Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[停止資料庫複製](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL 資料庫 Cmdlet](./Azure.SQLDatabase.md)

[AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[開始-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


