---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: df7b0803952a7a972d2c68ef2d8e7ec61d42c5e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621269"
---
# Start-AzPolicyRemediation

## 摘要
針對原則指派建立及啟動原則修正。

## 句法

### ByName (預設) 
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzPolicyRemediation** Cmdlet 會針對特定原則指派建立原則修正。 修正範圍或其下方的所有不相容資源都會修正。 只有「deployIfNotExists」效果的原則支援修正。

## 示例

### 範例1：在訂閱範圍中啟動修正
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

這個命令會在訂閱「我的訂閱」中針對指定原則指派建立新的原則修正。

### 範例2：使用選用篩選在管理群組範圍中啟動修正
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

這個命令會針對指定原則指派，在管理群組 ' mg1」中建立新的原則修正。 只有 ' westus」或「eastus」位置的資源會修正。

### 範例3：在原則集定義指派的資源群組範圍中啟動修正
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

這個命令會針對指定原則指派，在資源群組 ' myRG ' 中建立新的原則修正。 原則指派指派原則集定義 (也稱為「方案」) 。 原則定義參考 ID 會指出應修正計畫中的哪個原則。

### 範例4：啟動修正並等待其在背景完成
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

這個命令會針對指定原則指派，在訂閱「我的訂閱」中啟動新的原則修正。 在返回最終修正狀態之前，它會等到修正程式完成為止。

## 參數

### -AsJob
在背景中執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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

### -LocationFilter
應包含在修正中的資源位置。
不會修正位於這些位置的資源。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementGroupName
管理群組識別碼。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
資源名稱。

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

### -PolicyAssignmentId
原則指派識別碼。
例如.
'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.

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

### -PolicyDefinitionReferenceId
取得要修正之個別定義的原則定義參考 ID。
當原則指派指派策略集定義時，需要。

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

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
[資源識別碼]。

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -範圍
資源範圍。
例如.
'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### System.object []

## 輸出

### PSRemediation 中的 PolicyInsights。

## 筆記

## 相關連結
