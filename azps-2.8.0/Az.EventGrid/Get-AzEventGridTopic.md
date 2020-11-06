---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2bae39bb6a3e0c08a86118ce9ed8f9c6fadf82c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612475"
---
# Get-AzEventGridTopic

## 摘要
取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。

## 句法

### ResourceGroupNameParameterSet (預設) 
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。
如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。
如果未提供主題名稱，則會傳回主題的清單。 此清單中傳回的元素數目由 Top 參數控制。 如果未指定 Top 值或 $null，則清單將會包含所有主題專案。 否則，Top 會指出清單中要傳回的元素數目上限。
如果仍有更多主題可供使用，則會在下一個呼叫中使用 NextLink 中的值，以取得下一個主題頁面。
最後，ODataQuery 參數是用來執行搜尋結果篩選。 篩選查詢遵循 OData 語法，只使用 Name 屬性。 支援的作業包括： CONTAINS、等於 (等) 、ne (不等) ，以及（或）。

## 示例

### 範例1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。

### 範例2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。

### 範例3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題（ \` \` 無分頁）。

### 範例4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

如果資源群組 MyResourceGroupName 中有任何 \` \` 滿足 $odataFilter 查詢的) ，請列出前10個事件格線 (主題。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要取得下一頁 (的主題) ，使用者應該重新呼叫 Get-AzEventGridTopic 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

### 範例5
```powershell
PS C:\> Get-AzEventGridTopic
```

在不分頁的情況下，列出訂閱中的所有事件格線主題。

### 範例6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

如果訂閱中有任何滿足 $odataFilter 查詢的) ，請列出前10個事件格線主題 (。 如果有更多結果可供使用，$result。NextLink 不會 $null。 若要取得下一頁 (的主題) ，使用者應該重新呼叫 Get-AzEventGridTopic 並使用結果。從先前的呼叫取得的 NextLink。 當結果為來電時，呼叫者應該停止。NextLink 會變成 $null。

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

### -名稱
EventGrid 主題名稱。

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
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
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
代表事件格線主題的資源識別碼。

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -上方
要取得的資源數目上限。 有效值介於1到100。 如果已指定 top 值，但仍有更多結果，結果將會包含下一個頁面的連結，以在 NextLink 中查詢。 如果未指定 Top 值，就會一次傳回完整的資源清單。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

## 輸出

### PSTopic 中的 EventGrid。

### PSTopicListInstance 中的 EventGrid。

## 筆記

## 相關連結
