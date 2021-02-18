---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405613"
---
# Stop-AzureSqlDatabaseCopy

## 簡介
終止連續的複製關係。

## 語法

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

## 描述
**Stop-AzureSqlDatabaseCopy** Cmdlet 會終止連續的複製關係。
此 Cmdlet 會停止源資料庫與次要或目標資料庫之間的資料移動，然後將次要資料庫的狀態變更為獨立線上資料庫。

有兩種方法可以結束連續的複製關係、終止或計畫終止，以及可能的資料遺失強制終止。
在主管源資料庫的伺服器上，您可以在終止或強制終止模式中執行此 Cmdlet。
在主託管次要資料庫的伺服器上，您必須使用強制終止模式。

計畫終止會等到您執行 Cmdlet 時源資料庫上的所有已提交交易複製到次要資料庫。
強制終止不會等待複製任何未解決的已提交交易，而且可能會導致次要資料庫中的資料遺失。

當複製狀態為擱置中時，只有強制終止可以成功結束連續的複製關係。
如果複製狀態為擱置中，則不支援未強制終止。

## 例子

### 範例 1：終止連續的複製關係
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

此命令會終止名為 lpqd0zbr8y 伺服器上名為 Orders 的資料庫之連續複製關係。
名為 bk0b8kf658 的伺服器主託管次要資料庫。

### 範例 2：因應性終止連續的複製關係
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

第一個命令會針對名為 lpqd0zbr8y 的伺服器上名為 Orders 的資料庫，獲得資料庫的資料庫複製關係。

第二個命令會終止來自主託管次要資料庫之伺服器的連續複製關係。

## 參數

### -資料庫
指定代表來源 Azure SQL Database 的物件。
此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。

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
此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。
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
指定資料庫的名稱。
此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。

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

### -ForcedTermination
表示此 Cmdlet 會導致連續的複製關係強制終止。
強制終止可能會導致資料遺失。
若要在主管目標資料庫的伺服器上執行此 Cmdlet，您必須指定此參數。
若要在主管源資料庫的伺服器上執行此 Cmdlet，如果次要資料庫無法使用，您必須指定此參數。

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
如果您指定名稱，該名稱必須與源資料庫的名稱相符。

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
指定主託管目標資料庫的伺服器名稱。

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
執行 Cmdlet 之前，系統會提示您確認。

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

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 輸出

### 沒有

## 筆記
* 驗證：此 Cmdlet 需要憑證式驗證。 有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 **New-AzureSqlDatabaseServerCoNtext** Cmdlet。
* 限制：在主託管次要資料庫的伺服器上，僅支援強制終止。
* 終止對前次要資料庫的影響：終止後，次要資料庫會變成獨立資料庫。 如果次要資料庫的樹種已完成，則終止之後，此資料庫會開啟以完全存取。 如果源資料庫是讀寫資料庫，則前次要資料庫也會變成讀寫資料庫。

  如果目前進行中種樹，就會中止播下，而託管次要資料庫的伺服器上永遠不會顯示前次要資料庫。

* 您可以將源資料庫設定為唯讀模式。 這可確保來源資料庫和次要資料庫在終止後同步處理，並確保在終止期間不會提交任何交易。 終止完成後，將來源設定回讀寫模式。 或者，您也可以將前次要資料庫設為讀寫模式。
* 監控：若要驗證連續複製關係的來源和目標作業狀態，請使用 **Get-AzureSqlDatabaseOperation** Cmdlet。

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[停止資料庫複製](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


