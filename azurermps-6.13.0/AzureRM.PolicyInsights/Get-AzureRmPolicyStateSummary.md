---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447302"
---
# Get-AzureRmPolicyStateSummary

## 摘要
取得資源的最新原則規範狀態摘要。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### SubscriptionScope (預設) 
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
取得各種作用中的最新原則合規性狀態編號摘要視圖，細分為原則指派與原則定義。 它只包含不相容的原則狀態。

## 示例

### 範例1：取得目前訂閱範圍中的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。

### 範例2：取得指定訂閱範圍中的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

取得指定訂閱內所有資源之最後一天產生之最新原則規範狀態的摘要視圖。

### 範例3：取得管理群組範圍中的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

取得指定管理群組內所有資源之最後一天產生之最新原則合規性狀態的摘要視圖。

### 範例4：取得目前訂閱之資源群組範圍中的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

取得在目前會話內容) 的訂閱中，在最後一天內為指定資源 (群組中的所有資源所產生之最新原則相容性狀態的摘要視圖。

### 範例5：取得指定訂閱之資源群組範圍中的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

取得指定之資源群組中的所有資源在最後一天內所產生之最新原則規範狀態的摘要視圖， (于指定的訂閱) 中。

### 範例6：取得資源的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

取得指定資源最後一天產生之最新原則合規性狀態的摘要視圖。

### 範例7：取得目前訂閱中原則集定義的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得目前會話內容) 中的所有資源在) 租使用者的最後一天中所產生之最新原則符合性狀態的摘要視圖， (在訂閱中存在的指定原則集定義 (。

### 範例8：取得指定訂閱中原則集定義的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則集定義 (所影響的 (。

### 範例9：取得目前訂閱中原則定義的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得目前會話內容中的租使用者中的所有資源在前一天內所產生之最新原則相容性狀態的摘要視圖，) 在目前會話內容) 中存在於訂閱中之原則定義 (所影響的 (。

### 範例10：取得指定訂閱中原則定義的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則定義 (所影響的 (。

### 範例11：取得目前訂閱中原則指派的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得目前會話內容中，在所有資源的最後一天所產生的最新原則相容性狀態的摘要視圖，) 在目前會話內容) 中的訂閱中， (在訂閱中存在的特定原則指派 (。

### 範例12：取得指定訂閱中原則指派的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得在目前會話內容的租使用者中的所有資源所產生之最新原則相容性狀態的摘要視圖，) 在指定的訂閱) 中存在的指定原則指派 (所影響的 (。

### 範例13：取得目前訂閱之指定資源群組中原則指派的最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

取得 [ () 目前會話內容] 中的 [資源] 群組中存在於 [目前會話內容]) 中之 [資源] 群組中的所有 (資源所產生之最新原則規範狀態的摘要視圖。

### 範例14：在目前的訂閱範圍中取得最新不相容原則狀態摘要，並使用 Top 查詢選項
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。 此命令會根據不符合的資源計數以遞減順序，在結果中排序原則指派摘要，而且只會取得這些原則指派摘要的前5個。

### 範例15：取得目前訂閱範圍中的最新不相容原則狀態摘要，使用 From 和 To 查詢選項
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

取得在針對目前會話內容中訂閱之所有資源指定之日期範圍內所產生之最新原則合規性狀態的摘要視圖。

### 範例16：使用篩選查詢選項，在目前的訂閱範圍中取得最新不相容原則狀態摘要
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

取得目前會話內容中訂閱中所有資源在最後一天產生之最新原則合規性狀態的摘要視圖。
此命令會根據原則定義動作來限制篩選所傳回的結果 (包括拒絕或審核動作) 以及資源位置 (排除 eastus 位置) 。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### PolicyStateSummary 中的 PolicyInsights。

## 筆記

## 相關連結

[AzureRmPolicyState](./Get-AzureRmPolicyState.md)
