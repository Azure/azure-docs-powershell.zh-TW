---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911362"
---
# Get-AzPolicyStateSummary

## 簡介
獲得資源的最新政策合規性狀態摘要。

## 語法

### SubscriptionScope (預設) 
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
從不同範圍中，以摘要方式查看最新的政策合規性狀態號碼，細分為政策指派和策略定義。 它只包含不符合規定狀態。

## 例子

### 範例 1：取得目前訂閱範圍中最新的不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary
```

在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。

### 範例 2：取得指定訂閱範圍中最新的不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

針對指定訂閱內的所有資源，獲得過去一天產生的最新政策合規性狀態摘要視圖。

### 範例 3：在管理群組範圍中取得最新的不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

針對指定管理群組內的所有資源，獲得過去一天產生的最新政策合規性狀態摘要視圖。

### 範例 4：取得目前訂閱中資源群組範圍中最新的不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

針對訂閱中指定資源群組內的所有資源 ，于最後一天產生的最新政策合規性狀態摘要 (目前會話內容中的) 。

### 範例 5：取得指定訂閱中資源群組範圍中最新的不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

針對指定訂閱訂閱中指定資源群組內的所有資源，于最後一天產生的最新 (狀態摘要) 。

### 範例 6：取得資源的最新不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

獲得指定資源最後一天所產生之最新政策合規性狀態摘要視圖。

### 範例 7：取得目前訂閱中之策略集定義的最新不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

針對租使用者內所有資源 (在目前的會話內容中) 受目前會話內容中訂閱中指定的策略集定義 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要視圖) 。

### 範例 8：取得指定訂閱中之策略集定義的最新不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

針對租使用者內所有資源 ， (在目前的會話內容中) 受指定訂閱 (中指定的策略集定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。

### 範例 9：取得目前訂閱中之策略定義的最新不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

針對租使用者內所有資源 (在目前的會話內容中) 受目前會話內容中存在於訂閱中的指定政策定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。

### 範例 10：取得指定訂閱中之策略定義的最新不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

針對租使用者內所有資源 (在目前的會話內容中) 受指定訂閱 (中指定的策略定義 (影響的所有資源，獲得最後一天產生的最新政策合規性狀態摘要) 。

### 範例 11：取得目前訂閱中之策略工作分派的最新不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

針對租使用者內所有資源 (目前會話內容中) 受目前會話內容中存在於訂閱中的指定策略指派 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要) 。

### 範例 12：取得指定訂閱中之策略工作分派的最新不相容性政策狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

針對租使用者內所有資源 (在目前的會話內容中) 受指定訂閱 (中指定的策略指派影響之所有資源 ，最後一天產生的最新政策合規性狀態摘要) 。

### 範例 13：取得目前訂閱中指定資源群組中之策略工作分派的最新不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

針對租使用者內所有資源 (目前會話內容中) 受目前會話內容中訂閱中資源群組中指定的策略指派 (影響的所有資源，最後一天產生的最新政策合規性狀態摘要視圖) 。

### 範例 14：使用 Top 查詢選項，取得目前訂閱範圍中最新的不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。 該命令會以不相容的資源計數遞減順序排序結果中的策略工作分派摘要，並且只會佔用那些策略工作分派摘要的前 5 個。

### 範例 15：取得目前訂閱範圍中最新的不相容性政策狀態摘要，以及 From 和 To 查詢選項
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

在目前的會話內容中，為訂閱內所有資源指定的日期範圍內產生的最新政策合規性狀態摘要視圖。

### 範例 16：使用篩選查詢選項，取得目前訂閱範圍中最新的不符合規定狀態摘要
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

在目前的會話內容中，針對訂閱內的所有資源，獲得最後一天產生的最新政策合規性狀態摘要視圖。
命令會限制根據策略定義動作篩選的結果 (包括拒絕或稽核動作) ，而資源位置 (排除 eastus 位置) 。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -篩選
使用 OData 標記法篩選運算式。

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

### -從
ISO 8601 格式化的時間戳記，指定查詢間隔的開始時間。
未指定時，預設為 "To" 參數值減 1 天。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
管理組名。

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyAssignmentName
策略工作分派名稱。

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
策略定義名稱。

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
策略集定義名稱。

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名。

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
資源識別碼。

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
訂閱識別碼。

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
ISO 8601 格式化的時間戳記，指定查詢間隔的結束時間。
未指定時，預設為要求時間。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -頂端
要退回的記錄數目上限。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.PolicyInsights.models.PolicyStateSummary

## 筆記

## 相關連結

[Get-AzPolicyState](./Get-AzPolicyState.md)
