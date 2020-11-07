---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966872"
---
# Start-AzureSqlDatabaseRestore

## 摘要
執行資料庫的時間點還原。

## 句法

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseRestore** Cmdlet 會執行基本、標準或 Premium 資料庫的時間點還原。
Azure SQL 資料庫會保留基本的資料庫備份7天、標準的14天，以及35天的 Premium。
[還原] 作業會建立新的資料庫。
如果源資料庫未刪除， *SourceDatabaseName* 和 *TargetDatabaseName* 參數必須具有不同的值。

Azure SQL Database 目前不支援跨伺服器還原。
來源和目標伺服器名稱必須相同。

## 示例

### 範例1：將指定為物件的資料庫還原到某個時間點
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

第一個命令會在名為 Server01 的伺服器上取得名為 Database17 的資料庫物件，然後將它儲存在 $Database 變數中。

第二個命令會將資料庫還原至特定的時間點。
該命令會指定新資料庫的名稱。

### 範例2：將名稱指定的資料庫還原到某個時間點
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

這個命令會將名為 Database17 的資料庫還原至特定時間點。
該命令會指定新資料庫的名稱。

### 範例3：將已刪除的資料庫指定為物件至某個時間點
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

第一個命令會在名為 Server01 的伺服器上，為名為 Database01 的資料庫取得資料庫物件。
命令會指定 *RestorableDropped* 參數。
因此，此 Cmdlet 會取得可復原的中斷資料庫，並將指定的還原點。
該命令會將該資料庫物件儲存在 $Database 變數中。

第二個命令會還原 $Database 指定的刪除的資料庫。
該命令會指定新資料庫的名稱。

## 參數

### -PointInTime
指定要還原資料庫的還原點。
當還原作業完成時，資料庫會還原為此參數指定之日期和時間的狀態。
根據預設，針對此設定為目前時間的即時資料庫，而針對刪除的資料庫，此 Cmdlet 會使用刪除資料庫的時間。

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
表示此 Cmdlet 會還原可復原的已刪除資料庫。

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
指定此 Cmdlet 所還原之資料庫的名稱。

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
指定刪除資料庫的日期和時間。
當您指定時間來符合實際資料庫刪除時間時，您必須包含毫秒數。

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
指定此 Cmdlet 還原之實際資料庫的名稱。

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
指定代表此 Cmdlet 還原之可復原的已刪除資料庫的物件。
若要取得 **RestorableDroppedDatabase** 物件，請使用 Get-AzureSqlDatabase Cmdlet，並指定 *RestorableDropped* 參數。

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
指定源資料庫處於即時及正在執行的伺服器名稱，或在刪除之前執行源資料庫的伺服器名稱。

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
指定還原作業所建立之新資料庫的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
指定此 Cmdlet 要還原資料庫的伺服器名稱。

Azure SQL Database 目前不支援跨伺服器還原。
來源和目標伺服器名稱必須相同。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### SqlDatabase. RestorableDroppedDatabase （WindowsAzure）

### SqlDatabase.. Database （WindowsAzure）

## 輸出

### SqlDatabase. RestoreDatabaseOperation （WindowsAzure）

## 筆記
* 您必須使用 [以認證為基礎的驗證] 才能執行此 Cmdlet。 在執行此 Cmdlet 的電腦上執行下列命令： 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 相關連結

[Azure SQL 資料庫](https://azure.microsoft.com/en-us/services/sql-database/)

[建立資料庫還原要求](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Azure SQL 資料庫的作業](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)


