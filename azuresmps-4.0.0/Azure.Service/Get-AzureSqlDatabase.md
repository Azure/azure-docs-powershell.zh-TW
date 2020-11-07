---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967744"
---
# Get-AzureSqlDatabase

## 摘要
檢索一或多個資料庫。

## 句法

### ByConnectionCoNtext (預設) 
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabase** Cmdlet 會從 Azure sql 資料庫伺服器中檢索 Azure sql database 的一個或多個實例。
您可以使用 **AzureSqlDatabaseServerCoNtext** Cmdlet 所建立的 Azure SQL Database server 連接內容來指定伺服器。
或者，如果您指定 Azure SQL 資料庫伺服器名稱，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證訪問伺服器的要求。

如果您沒有指定資料庫， **AzureSqlDatabase** Cmdlet 會傳回指定伺服器中的所有資料庫。

檢索能還原的已丟棄資料庫：

使用 *RestorableDropped* 參數來檢索可還原的已刪除資料庫。
若要傳回所有可還原的中斷資料庫，請使用不含 *DatabaseName* 和 *DatabaseDeletionDate* 的 *RestorableDropped* 參數。
若要傳回特定的可還原已刪除的資料庫，請使用 *RestorableDropped* 參數及 *DatabaseName* 和 *DatabaseDeletionDate* 參數。
使用 *DatabaseName* 參數來檢索特定的可還原刪除的資料庫時，您也必須包含 *DatabaseDeletionDate* 參數，且指定的 *DatabaseDeletionDate* 值必須包含毫秒，才能符合所需的資料庫。

**AzureSqlDatabase** Cmdlet 會傳回伺服器上所有可還原的已丟棄資料庫，或傳回與 *DatabaseName* 和 *DatabaseDeletionDate* 相符的特定資料庫。
若要傳回符合不同準則的可還原中斷資料庫（例如，所有可還原的特定名稱資料庫），您必須傳回所有可還原的已刪除資料庫，然後在用戶端上篩選結果。

## 示例

### 範例1：在伺服器上檢索所有資料庫
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

這個命令會在伺服器上檢索名為 lpqd0zbr8y 的所有資料庫。

### 範例2：在伺服器上檢索所有能還原的已丟棄資料庫
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

這個命令會在名為 lpqd0zbr8y 的伺服器上，檢索所有能還原的中斷資料庫。

### 範例3：從連接內容所指定的伺服器中檢索資料庫
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

這個命令會從 $CoNtext 連接內容指定的伺服器中檢索名為 Database01 的資料庫。

### 範例4：將資料庫物件儲存在變數中
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

這個命令會從伺服器（名為 lpqd0zbr8y）中檢索名為 Database01 的資料庫。
該命令會將資料庫物件儲存在 $Database 01 變數中。

### 範例5：取回還原的已刪除資料庫
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

這個命令會從伺服器（名為 lpqd0zbr8y）中檢索已從11/9/2012 刪除的可還原已刪除的 Database01 資料庫。
這個命令會將結果儲存在 $DroppedDB 變數中。

### 範例6：在伺服器上檢索所有能還原的中斷資料庫並篩選結果
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

這個命令會在名為 lpqd0zbr8y 的伺服器上檢索所有可還原的中斷資料庫，然後將結果篩選為僅限名為 ContactDB 的資料庫。

## 參數

### -ConnectionCoNtext
指定要從中檢索資料庫的伺服器連接內容。

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -資料庫
指定代表此 Cmdlet 所檢索之資料庫的物件。

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
指定刪除的日期和時間。
如果您指定 *RestorableDropped* 參數，請指定此參數，以根據刪除日期和時間來檢索可還原的已刪除資料庫。

*DatabaseDeletionDate* 參數必須包含毫秒，以符合所需資料庫的時間。
指定不含毫秒的值會產生資料庫找不到的結果。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
指定此 Cmdlet 所檢索之資料庫的名稱。

```yaml
Type: String
Parameter Sets: (All)
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

### -RestorableDropped
表示此 Cmdlet 會傳回 *RestorableDroppedDatabase* 物件，而不是 *資料庫* 物件。
您可以使用 *DatabaseDeletionDate* 參數來選取特定的可還原已刪除的資料庫。

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

### -RestorableDroppedDatabase
指定代表此 Cmdlet 所檢索之可還原已刪除資料庫的物件。

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerName
指定包含此 Cmdlet 所檢索之資料庫的伺服器名稱。
此 Cmdlet 會使用目前的 Azure 訂閱來存取伺服器。

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### SqlDatabase.. Database （WindowsAzure）

### SqlDatabase. RestorableDroppedDatabase （WindowsAzure）

## 輸出

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
如果您沒有指定 *RestorableDropped* 參數，此 Cmdlet 會傳回 *資料庫* 物件。

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
如果您指定 *RestorableDropped* 參數，這個 Cmdlet 會傳回 *RestorableDroppedDatabase* 物件。

## 筆記

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[新-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[新-AzureSqlDatabaseServerCoNtext](./New-AzureSqlDatabaseServerContext.md)

[移除-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


