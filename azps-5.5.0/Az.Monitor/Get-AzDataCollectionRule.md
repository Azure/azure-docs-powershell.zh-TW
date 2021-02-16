---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129111"
---
# Get-AzDataCollectionRule

## 摘要
取得資料收集規則 (s) 。

## 句法

### BySubscription (預設) 
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### ByResourceGroup
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### ByName
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### ByResourceId
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## 說明
**AzDataCollectionRule** Cmdlet 會取得一或多個資料收集規則。

資料收集規則 (DCR) 定義進入 Azure 監視器的資料，並指定要傳送或儲存資料的位置。 以下是完整的 [DCR 概述文章](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)。

## 示例

### 範例1：依訂閱識別碼取得資料收集規則
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

這個命令會列出目前訂閱的所有資料收集規則。

### 範例2：取得指定資源群組的資料收集規則
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

這個命令會列出指定資源群組的資料收集規則。

### 範例3：取得資料集合規則
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

這個命令會列出一個 (清單，其中只有一個元素) 資料收集規則。

### 範例4：依規則識別碼取得資料收集規則
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

這個命令會列出一個 (清單，其中只有一個元素) 資料收集規則。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleName
資源的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleId
資源的識別碼。

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource

## 筆記

## 相關連結

[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[移除-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[新-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[更新-AzDataCollectionRule](./Update-AzDataCollectionRule.md)
