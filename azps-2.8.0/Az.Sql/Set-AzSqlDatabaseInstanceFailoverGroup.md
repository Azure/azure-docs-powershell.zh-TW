---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792599"
---
# Set-AzSqlDatabaseInstanceFailoverGroup

## 摘要
修改實例容錯移轉群組的配置。

## 句法

### SetIFGDefault (預設) 
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 從資源識別碼設定實例容錯移轉群組
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 從 AzureSqlInstanceFailoverGroupModel 實例定義設定實例容錯移轉群組
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這個命令會修改實例容錯移轉群組的配置。

應使用實例容錯移轉群組的主要區域來執行命令。

在實例容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。

## 示例

### 範例1
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

透過 [容錯移轉] 群組中的管道，將實例容錯移轉群組的容錯移轉原則設定為「手動」。

## 參數

### -AllowReadOnlyFailoverToPrimary
在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。
尚不支援此功能。

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
實例容錯移轉群組的容錯移轉原則。

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要設定的實例容錯移轉群組物件

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
要從中取得實例容錯移轉群組的本機區功能變數名稱稱。

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
實例容錯移轉群組的名稱。

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
要設定之實例容錯移轉群組的資源識別碼。

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]
System.object

## 輸出

### AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]

## 筆記

## 相關連結
