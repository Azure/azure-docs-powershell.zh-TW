---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 8ac0be356aa1f10df2543e65e03eae302e1d6454
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621272"
---
# Get-AzPolicyState

## 摘要
取得資源的原則合規性狀態。

## 句法

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
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
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

## 說明
取得資源的原則合規性狀態。 您可以在不同的範圍中查詢原則狀態記錄。 根據指定的時間間隔 (預設為 [最後一天]) ，可以查詢最新的原則狀態或所有原則狀態轉移。 您可以對結果進行篩選、群組和群組匯總的計算。

## 示例

### 範例1：在目前的訂閱範圍中取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。

### 範例2：在指定的訂閱範圍中取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

針對指定訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。

### 範例3：取得目前訂閱範圍中的所有原則狀態
```powershell
PS C:\> Get-AzPolicyState -All
```

取得所有的歷史原則狀態記錄 (，包括在目前會話內容中訂閱中所有資源的最後一天所產生的最新) 。

### 範例4：取得管理群組範圍中的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

針對指定管理群組中的所有資源，取得最後一天產生的最新原則狀態記錄。

### 範例5：在目前訂閱的資源群組範圍中取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

取得在目前會話內容) 的訂閱中，在最後一天內為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。

### 範例6：在指定訂閱的資源群組範圍中取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

取得指定的 [訂閱]) 中，在最後一天為指定資源群組中的所有資源所產生的最新原則狀態記錄 (。

### 範例7：取得資源的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

取得指定資源最後一天產生的最新原則狀態記錄。

### 範例8：在目前的訂閱中取得原則集定義的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得目前會話內容中的所有資源在最後一天中產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中的原則集定義 (所影響的 (。

### 範例9：取得指定訂閱中原則集定義的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則集定義 (所影響。

### 範例10：取得目前訂閱中原則定義的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之原則定義 (所影響的 (。

### 範例11：針對指定訂閱中的原則定義取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則定義 (所影響。

### 範例12：取得目前訂閱中原則指派的最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得目前會話內容中的所有資源在最後一天內所產生的最新原則狀態記錄，) 在目前會話內容) 中存在於訂閱中之 (的原則指派 (所影響。

### 範例13：針對指定訂閱中的原則指派取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得在目前會話內容的租使用者中，在最後一天所產生的所有資源 (的最新原則狀態記錄，) 在指定的訂閱) 中存在的指定原則指派 (所影響。

### 範例14：針對目前訂閱中指定的資源群組中的原則指派取得最新原則狀態
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得目前會話內容的所有 (資源在最後一天中所產生的最新原則狀態記錄，) 目前會話內容) 中的 [資源] 群組中存在的指定原則指派 (所影響。

### 範例15：使用 OrderBy、Top 及 Select 查詢選項，在目前的訂閱範圍中取得最新的原則狀態
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。 命令會依時間戳記與原則指派名稱屬性來排序結果，且只會取得那些順序中所列的前5名。
它也會選取，只列出每一筆記錄的資料行子集。

### 範例16：在目前的訂閱範圍中取得最新原則狀態，使用 From 和 To 查詢選項
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

取得在目前會話內容的訂閱中，在指定的日期範圍內產生的最新原則狀態記錄。

### 範例17：使用篩選查詢選項，在目前的訂閱範圍中取得最新的原則狀態
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。
此命令會根據原則定義動作所傳回的結果加以限制， (包括拒絕或審核動作) 、相容性狀態 (只包含不相容狀態) 與資源位置 (排除 eastus 位置) 。

### 範例18：在目前的訂閱範圍中取得最新原則狀態，並套用指定資料列計數匯總
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

取得目前會話內容中訂閱之所有資源在最後一天內產生的最新原則狀態記錄數。
命令只會傳回原則狀態記錄的計數，在 AdditionalProperties 屬性內傳回。

### 範例19：在目前的訂閱範圍中取得最新原則狀態，並套用 [使用匯總指定群組]
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。 此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。
根據原則指派、原則集定義及原則定義來分組結果，然後計算每個群組中傳回的記錄數（在 AdditionalProperties 屬性內傳回）。
它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。

### 範例20：在目前的訂閱範圍中取得最新的原則狀態，並套用指定不含匯總的群組
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。 此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。
它會根據資源識別碼來分組結果。這會產生與至少一個原則不相容的訂閱中所有資源的清單。

### 範例21：在目前的訂閱範圍中取得最新原則狀態，並套用指定多重群組
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

針對目前會話內容中訂閱中的所有資源，取得最後一天產生的最新原則狀態記錄。 此命令會根據符合規範狀態的篩選所傳回的結果來限制 (只包含不相容的狀態) 。
它會先根據原則指派、原則集定義、原則定義及資源識別碼，將結果分組。接著，它會進一步將此群組的結果與與資源識別碼不同的屬性組成群組，並計算在 AdditionalProperties 屬性內傳回的每個群組中的記錄數。
它會依計數匯總以遞減順序來排序結果，而且只會取得那些順序中所列的前5位。
這會產生最多不相容資源數的前5個原則。

## 參數

### -全部
在指定的時間間隔內，取得所有原則狀態，而不是最新的。

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

### -套用
使用 OData 符號將運算式套用至匯總。

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

### -篩選
使用 OData 符號篩選運算式。

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
ISO 8601 格式化的時間戳記，指定要查詢間隔的開始時間。
如果未指定，則預設為「To」參數值減去1天。

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
使用 OData 符號排序運算式。
一或多個以逗號分隔的欄名稱，其中包含 [desc "預設) 或" asc " (。

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
原則作業名稱。

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
原則定義名稱。

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
原則集定義名稱。

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
資源組名稱。

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
[資源識別碼]。

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
選取 [使用 OData 符號的運算式]。
一或多個以逗號分隔的欄名稱。
將每筆記錄的欄限制為僅限所要求的資料行。

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
訂閱 ID。

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
ISO 8601 格式化的時間戳記，指定要查詢間隔的結束時間。
如果未指定，則預設為要求的時間。

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

### -上方
要傳回的最大記錄數。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PolicyState 中的 PolicyInsights。

## 筆記

## 相關連結

[AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
