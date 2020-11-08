---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128186"
---
# Get-AzEventGridSubscription

## 摘要
取得事件訂閱的詳細資料，或取得目前 Azure 訂閱中的所有事件訂閱清單。

## 句法

### EventSubscriptionTopicNameParameterSet (預設) 
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzEventGridSubscription Cmdlet 會取得指定事件格線訂閱的詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。
如果提供了事件訂閱名稱，則會傳回單一事件格線訂閱的詳細資料。
如果未提供事件訂閱名稱，則會傳回所有事件訂閱的清單。 此清單中傳回的元素數目由 Top 參數控制。 如果未指定 Top 值或 $null，則清單將會包含所有事件訂閱專案。 否則，Top 會指出清單中要傳回的元素數目上限。
如果仍有更多事件訂閱可用，則會在下一個呼叫中使用 NextLink 中的值，以取得事件訂閱的下一個頁面。
最後，ODataQuery 參數是用來執行搜尋結果篩選。 篩選查詢遵循 OData 語法，只使用 Name 屬性。 支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。

## 示例

### 範例1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

取得 \` \` \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的 \` \` 事件訂閱 EventSubscription1 詳細資料。

### 範例2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` \` \` ，包括完整的端點 URL （如果它是以 webhook 為基礎的事件訂閱）。

### 範例3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

取得 \` \` 在沒有分頁的資源群組 MyResourceGroupName 中為主題 Topic1 所建立的所有事件訂閱清單 \` \` 。

### 範例4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

如果針對 \` \` 資源群組 \` MyResourceGroupName 中 \` 滿足 $odataFilter 查詢的主題 Topic1 建立任何) ，請列出前10個事件訂閱 (。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

取得 \` \` 針對資源群組 MyResourceGroupName 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` 。

### 範例6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

取得 \` \` 目前所選 Azure 訂閱所建立之事件訂閱 EventSubscription1 的詳細資料。

### 範例7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

取得在未分頁的資源群組 MyResourceGroupName 下所建立的所有全域事件訂閱清單 \` \` 。

### 範例8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

如果在 [資源群組 MyResourceGroupName] 下建立 \` \` 滿足 $odataFilter 查詢的任何) ，請列出前5個事件訂閱 (。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例9
```powershell
PS C:\> Get-AzEventGridSubscription
```

取得目前選取的 Azure 訂閱（不分頁）下所建立的所有全域事件訂閱清單。

### 範例10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出前15個全域事件訂閱 (如果在目前所選的 Azure 訂閱中建立的任何) 都符合 $odataFilter 查詢。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

取得在 \` \` 未分頁的指定位置 westus2 中，在 [資源群組 MyResourceGroupName] 下所建立的所有區域事件訂閱清單 \` \` 。

### 範例12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出前15個地區性事件訂閱 (如果在 [資源群組] MyResourceGroupName 中建立的任何) \` \` \` \` ，都必須符合 $odataFilter 查詢的指定位置 westus2。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

取得不需分頁的指定 EventHub 命名空間所建立的所有事件訂閱清單。

### 範例14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出前25個事件訂閱 (如果針對指定的 EventHub 命名空間所建立的任何) （滿足 $odataFilter 查詢）。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

取得在指定位置中針對指定的主題類型 (EventHub 命名空間) 中所建立之所有事件訂閱的清單（不需要分頁）。

### 範例16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

清單前15個事件訂閱 (如果針對指定的主題類型建立的任何) ， (EventHub 命名空間) 于指定位置中，以滿足 $odataFilter 查詢。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

取得針對特定資源群組（不分頁）所建立的所有事件訂閱清單。

### 範例18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出第一個100事件訂閱 (如果針對滿足 $odataFilter 查詢的特定資源群組所建立的任何) 。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要在下一頁 (s 的事件訂閱) ，使用者應該重新呼叫 Get-AzEventGridSubscription 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

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

### -DomainInputObject
EventGrid Domain 物件。

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -功能變數名稱
EventGrid [功能變數名稱]。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid [網域] 主題物件。

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
EventGrid [網域主題名稱]。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
事件訂閱的名稱

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
包含事件訂閱目的地的完整端點 URL。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid 主題物件。

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
位於

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
要取得的下一頁資源連結。 當仍有更多資源可供查詢時，會使用第一個 Get-AzEventGrid Cmdlet 呼叫來取得此值。

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
用來篩選清單結果的 OData 查詢。 目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
已建立事件訂閱之資源的識別碼。

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -上方
用來篩選清單結果的 OData 查詢。 目前只允許在 Name 屬性上使用篩選。支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid 主題名稱。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType 名稱

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### PSTopic 中的 EventGrid。

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

## 輸出

### PSEventSubscription 中的 EventGrid。

## 筆記

## 相關連結
