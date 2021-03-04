---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911365"
---
# Get-AzPolicyState

## 簡介
為資源獲取政策合規性狀態。

## 語法

### SubscriptionScope (預設) 
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
為資源獲取政策合規性狀態。 可以在各種範圍中查詢策略狀態記錄。 根據指定的時間間隔 (預設為最後一天) ，可以查詢最新的政策狀態或所有政策狀態轉換。 結果可以篩選、分組，也可以計算群組匯總。

## 例子

### 範例 1：取得目前訂閱範圍中的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。

### 範例 2：取得指定訂閱範圍中的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

為指定訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。

### 範例 3：取得目前訂閱範圍的所有策略狀態
```powershell
PS C:\> Get-AzPolicyState -All
```

在所有歷史政策狀態記錄中 (包括) 目前會話內容中，訂閱內所有資源最後一天產生的最新記錄。

### 範例 4：取得管理群組範圍中的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

為指定管理群組內的所有資源，獲得過去一天產生的最新政策狀態記錄。

### 範例 5：取得目前訂閱中資源群組範圍中的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

在訂閱的目前會話內容中，針對指定資源群組內的所有資源， (過去一天產生的最新) 。

### 範例 6：取得指定訂閱中資源群組範圍中的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

針對指定資源群組內的所有資源，于最後一天產生的最新 (指定訂閱) 。

### 範例 7：取得資源的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

為指定的資源，獲得最後一天產生的最新政策狀態記錄。

### 範例 8：取得目前訂閱中之策略集定義的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

在目前的會話內容中 (租使用者內的所有資源) 受目前會話內容中之訂閱中指定的 (定義影響) ，最後一天產生的最新政策狀態記錄。

### 範例 9：取得指定訂閱中之策略集定義的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

針對目前會話內容中租使用者內的所有資源 (過去一天產生的最新政策狀態記錄) 受指定訂閱環境中指定的 (定義影響) 。

### 範例 10：取得目前訂閱中之策略定義的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

在目前的會話內容中 (租使用者內的所有資源) 會受目前會話內容中存在於訂閱中的指定 (影響，而最後一天產生的所有資源的最新政策狀態記錄) 。

### 範例 11：取得指定訂閱中之策略定義的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

在租使用者目前的會話內容中， (在租使用者內的所有資源) 在前一天產生的最新政策狀態記錄 (會受指定訂閱) 中指定的) 。

### 範例 12：取得目前訂閱中之策略工作分派的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

在目前的會話內容中 (租使用者內的所有資源) 在前一天產生的最新政策狀態記錄 (會受目前會話內容中訂閱中指定的) 。

### 範例 13：取得指定訂閱中之策略指派的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

在目前的會話內容中 (租使用者內的所有資源) 會受指定訂閱環境中指定的 (影響 (產生的最新政策狀態記錄) 。

### 範例 14：取得目前訂閱中指定資源群組中之策略工作分派的最新政策狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

在目前的會話內容中 (租使用者內的所有資源 ，) 會受目前會話內容中訂閱中資源群組中指定的 (影響，而最後一天產生的最新政策狀態記錄) 。

### 範例 15：使用 OrderBy、Top 和 Select 查詢選項，取得目前訂閱範圍中的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。 命令會按時間戳記和策略工作分派名稱屬性排序結果，並僅取用該順序所列的前 5 個。
它也選取只列出每一個記錄的欄子集。

### 範例 16：取得目前訂閱範圍中的最新策略狀態，以及從和到查詢選項
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

在目前的會話內容中，為訂閱內的所有資源，在日期範圍內產生的最新政策狀態記錄。

### 範例 17：使用篩選查詢選項，取得目前訂閱範圍中的最新策略狀態
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。
命令會根據策略定義動作 (包含拒絕或稽核動作) 、合規性狀態 (僅包含不符合規範的狀態) 和資源位置 (排除 eastus 位置) 來限制篩選的結果。

### 範例 18：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定列計數匯總
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

在目前的會話內容中，為訂閱內的所有資源，獲得最後一天產生的最新政策狀態記錄數目。
該命令僅會返回在 AdditionalProperties 屬性內所返回之策略狀態記錄的計數。

### 範例 19：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定群組與匯總
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。 命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。
它會根據策略指派、策略集定義和策略定義將結果組成群組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。
它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。

### 範例 20：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定群組而不匯總
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。 命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。
它會根據資源識別碼將結果分組。這會在訂閱內產生至少一個不符合一個政策之所有資源的清單。

### 範例 21：取得目前訂閱範圍中的最新原則狀態，使用 Apply 指定多個群組
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### 範例 22：取得最新的策略狀態，包括資源的策略評估詳細資料
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

在目前的會話內容中，為訂閱內的所有資源，于最後一天產生的最新政策狀態記錄。 命令會根據合規性狀態限制篩選所 (只包含不符合規範的狀態) 。
它會根據策略指派、策略集定義、策略定義和資源識別碼，先將結果組成群組。接著，它會使用資源識別碼以外的相同屬性進一步將此群組的結果分組，並計算每個群組中的記錄數目，此數目是在 AdditionalProperties 屬性內所返回。
它會根據計數匯總以遞減順序排序結果，而且只會取用該順序中列出的前 5 個結果。
這會產生最符合規範資源的前 5 個策略。

## 參數

### -全部
在指定的時間間隔內，取得所有政策狀態，而不是只取得最新的狀態。

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

### -Apply
使用 OData 標記法將運算式適用于匯總。

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

### -展開
使用 OData 標記法展開運算式。

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### -OrderBy
使用 OData 標記法排序運算式。
一或多個以逗號分隔的欄名稱，以及預設 (或'asc) 名稱。

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

### -選取
使用 OData 標記法選取運算式。
一或多個以逗號分隔的欄名稱。
將每一個記錄上的欄限制為只有要求的記錄。

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

### Microsoft.Azure.Commands.PolicyInsights.models.PolicyState

## 筆記

## 相關連結

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
