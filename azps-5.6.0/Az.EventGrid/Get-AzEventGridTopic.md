---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912005"
---
# Get-AzEventGridTopic

## 簡介
獲得事件格線主題的詳細資訊，或獲得目前 Azure 訂閱中所有事件格線主題的清單。

## 語法

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

## 描述
此Get-AzEventGridTopic Cmdlet 會獲得指定事件格線主題的詳細資訊，或目前 Azure 訂閱中所有事件格線主題的清單。
如果提供主題名稱，則會返回單一事件格線主題的詳細資訊。
如果未提供主題名稱，會返回主題清單。 此清單所返回的元素數目是由 Top 參數控制。 如果未指定頂端值或$null，清單會包含所有主題專案。 否則，Top 會指出清單中要返回的元素數目上限。
如果仍有更多主題可用，則 NextLink 中的值應該用於下一個通話中，以取得下一頁的主題。
最後，ODataQuery 參數是用來執行搜尋結果的篩選。 篩選查詢只會使用 Name 屬性遵循 OData 語法。 支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。

## 例子

### 範例 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

在資源群組 \` \` \` MyResourceGroupName 中，獲得事件格線主題 Topic1 的詳細資訊 \` 。

### 範例 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

在資源群組 \` \` \` MyResourceGroupName 中，獲得事件格線主題 Topic1 的詳細資訊 \` 。

### 範例 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

在資源群組 MyResourceGroupName 中列出所有事件格線主題， \` \` 而不分頁。

### 範例 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

在資源群組 MyResourceGroupName (，列出前 10 個事件格線主題) 滿足該查詢$odataFilter \` \` 主題。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得下一頁 () ，使用者預期會重新撥打Get-AzEventGridTopic並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 5
```powershell
PS C:\> Get-AzEventGridTopic
```

在訂閱中列出所有事件格線主題，而不分頁。

### 範例 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

如果訂閱中有任何符合 (查詢) ，請列出前 10 個事件格線主題$odataFilter主題。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得下一頁 () ，使用者預期會重新撥打Get-AzEventGridTopic並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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
這是要取得之資源下一頁的連結。 當仍有更多資源可供查詢Get-AzEventGrid Cmdlet 呼叫時，會取得此值。

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
用來篩選清單結果的 OData 查詢。 目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。

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
資源組名。

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

### -頂端
要取得的資源數量上限。 有效的值介於 1 到 100 之間。 如果已指定頂端值，且仍有更多結果可用，則結果會包含下一頁的連結，可在 NextLink 中查詢。 如果未指定 Top 值，將會一次返回完整的資源清單。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]

## 輸出

### Microsoft.Azure.Commands.EventGrid.models.PSTopic

### Microsoft.Azure.Commands.EventGrid.models.PSTopicListInstance

## 筆記

## 相關連結
