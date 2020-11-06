---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447918"
---
# Restore-AzureRmSqlDatabase

## 摘要
還原 SQL 資料庫。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### FromPointInTimeBackup
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedDatabaseBackup
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromGeoBackup
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### FromLongTermRetentionBackup
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**Restore-AzureRmSqlDatabase** Cmdlet 會從地域冗余備份、備份已刪除的資料庫、長時間保留備份或即時資料庫中的時間點，復原 SQL 資料庫。
已還原的資料庫會建立為新資料庫。

您可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性 SQL 資料庫。

## 示例

### 範例1：從某個時間點還原資料庫
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。

第二個命令會從指定的時間點備份將 $Database 中的資料庫還原到名為 RestoredDatabase 的資料庫。

### 範例2：從某個時間點將資料庫還原到彈性池
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。

第二個命令會將 $Database 中的資料庫從指定的時間點備份還原到名為 elasticpool01 的彈性池中名為 RestoredDatabase 的 SQL 資料庫。

### 範例3：還原已刪除的資料庫
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。
第二個命令會使用 [Restore AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) Cmdlet，從已刪除的資料庫備份開始還原。 如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。

### 範例4：將已刪除的資料庫還原成彈性池
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。
第二個命令會使用 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)從已刪除的資料庫備份開始還原。 如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。

### 範例5： Geo-Restore 資料庫
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。

第二個命令會在 $GeoBackup 到名為 RestoredDatabase 的 SQL 資料庫時還原備份。

## 參數

### -DeletionDate
將刪除日期指定為 **DateTime** 物件。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Edition
指定 SQL 資料庫的版本。
此參數可接受的值為：

- 所有
- 佳
- 空白
- 標準
- 倉庫
- 空閒

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ElasticPoolName
指定要放入 SQL 資料庫的彈性池的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FromDeletedDatabaseBackup
表示此 Cmdlet 會從已刪除的 SQL 資料庫備份還原資料庫。
您可以使用 Get-AzureRMSqlDeletedDatabaseBackup Cmdlet 來取得已刪除之 SQL 資料庫的備份。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromGeoBackup
表示此 Cmdlet 會從地域冗余備份還原 SQL 資料庫。
您可以使用 Get-AzureRMSqlDatabaseGeoBackup Cmdlet 來取得地域冗余備份。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromLongTermRetentionBackup
表示此 Cmdlet 會從長期保留備份還原 SQL 資料庫。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromPointInTimeBackup
表示此 Cmdlet 會從時間點備份還原 SQL 資料庫。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PointInTime
指定要將 SQL 資料庫還原至其中的時間點（以 **DateTime** 物件表示）。
若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。

將此參數與 *FromPointInTimeBackup* 參數搭配使用。

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 指派 SQL 資料庫的資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
指定要還原的資源識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
指定 SQL 資料庫伺服器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
指定服務目標的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetDatabaseName
指定要還原到的資料庫的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AzureSqlDatabaseModel （.Sql）的。

## 筆記

## 相關連結

[從中斷中復原 Azure SQL 資料庫](https://go.microsoft.com/fwlink/?LinkId=746882)

[從使用者錯誤復原 Azure SQL 資料庫](https://go.microsoft.com/fwlink/?LinkId=746944)

[AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[AzureRMSqlDatabaseGeoBackup](./Get-AzureRMSqlDatabaseGeoBackup.md)

[AzureRMSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)

