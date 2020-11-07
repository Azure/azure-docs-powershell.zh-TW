---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 6ec4e3163d1bcd388ef0b4b8813ece89a41bfd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792638"
---
# Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy

## 摘要
設定 [備份短期保留原則]。

## 句法

### PolicyByResourceInstanceDatabaseSet (預設) 
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PolicyByInputObjectSet
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PolicyByResourceIdSet
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。
原則是在時間點還原備份的保留期間（以天數為單位）。

## 示例

### 範例1
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

這個命令會將 database01 至35天的短期保留原則設定為。

### 範例2
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

這個命令會透過 database01 到資料庫物件中的 [管道]，來設定到35天的短期限保留原則。

### 範例3
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

這個命令會在已刪除的資料庫物件中，為以 [DB1] 命名的所有已刪除資料庫設定短期保留原則。 注意：您只能減少已刪除資料庫的保留期間。

## 參數

### -DatabaseName
要為其檢索備份之 Azure SQL 實例資料庫的名稱。

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeletionDate
要為其檢索備份的 Azure SQL 實例資料庫的刪除日期，以毫秒為單位 (（例如 2016-02-23T00：21： 22.847 Z) 

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要取得/設定原則的即時或刪除資料庫物件。

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstanceName
資料庫所在之 Azure SQL 託管實例的名稱。

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
短期保留原則資源識別碼。

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionDays
備份保留天數。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### AzureSqlManagedDatabaseBaseModel 中的 [ManagedDatabase]

### System.object

## 輸出

### AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]

## 筆記

## 相關連結
