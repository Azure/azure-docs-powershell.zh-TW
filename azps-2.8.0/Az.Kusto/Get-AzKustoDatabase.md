---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612051"
---
# Get-AzKustoDatabase

## 摘要
列出群集中的所有 Kusto 資料庫，或取得特定的 Kusto 資料庫。

## 句法

### ByClusterOrResourceGroupOrSubscription (預設) 
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByInputObject
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
列出群集中的所有 Kusto 資料庫，或取得特定的 Kusto 資料庫。

## 示例

### 範例 1-依名稱列出群集中的所有 Kusto 資料庫

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

上述命令會傳回在資源群組 "testrg" 中找到的 [mykustocluster] 群集中的所有 Kusto 資料庫。

### 範例 2-依管道列出群集中的所有 Kusto 資料庫

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

上述命令會在使用 Cmdlet 的資源群組 "testrg" 中，找到名為 "mykustocluster" 的 Kusto 群集 `Get-AzKustoCluster` ，並將結果輸送至 `Get-AzKustoDatabase` Cmdlet，以列出該群集中的所有資料庫。

### 範例 3-依名稱取得特定的 Kusto 資料庫

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

上述命令會傳回在資源群組 "testrg" 中找到的群集 "mykustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。

## 參數

### -ClusterName
資料庫所在之群集的名稱。

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
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

### -InputObject
Kusto [群集物件]。

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
資料庫的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
使用者想要在其上取得群集的資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Kusto [群集 ResourceID]。

```yaml
Type: System.String
Parameter Sets: ByResourceId
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

### System.object

### PSKustoCluster 中的 Kusto。

## 輸出

### PSKustoDatabase 中的 Kusto。

## 筆記

## 相關連結
