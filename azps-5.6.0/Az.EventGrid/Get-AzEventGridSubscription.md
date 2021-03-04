---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912013"
---
# Get-AzEventGridSubscription

## 簡介
獲得事件訂閱的詳細資訊，或獲得目前 Azure 訂閱中所有事件訂閱的清單。

## 語法

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

## 描述
此Get-AzEventGridSubscription Cmdlet 會獲得指定的事件格線訂閱詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。
如果提供事件訂閱名稱，系統即會返回單一事件格線訂閱的詳細資訊。
如果未提供事件訂閱名稱，會返回所有事件訂閱的清單。 此清單所返回的元素數目是由 Top 參數控制。 如果未指定頂端值或$null，清單會包含所有事件訂閱專案。 否則，Top 會指出清單中要返回的元素數目上限。
如果仍有更多活動訂閱可用，則 NextLink 中的值應該用於下一個通話中，以取得活動訂閱的下一頁。
最後，ODataQuery 參數是用來執行搜尋結果的篩選。 篩選查詢只會使用 Name 屬性遵循 OData 語法。 支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。

## 例子

### 範例 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

在資源群組 MyResourceGroupName 中，為 Topic1 建立的事件訂閱 \` \` \` \` \` EventSubscription1 詳細資料 \` 。

### 範例 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

在資源群組 \` \` \` \` \` MyResourceGroupName 中，針對主題主題 1 建立的事件訂閱 EventSubscription1 詳細資料，包括完整端點 URL ，如果它是 \` Web一型事件訂閱。

### 範例 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

在資源群組 \` \` \` MyResourceGroupName 中取得為主題 1 建立的所有事件訂閱清單，而不 \` 分頁。

### 範例 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

在資源群組 \` \` \` MyResourceGroupName) 中 (主題 1 建立的主題 1 時，列出前 10 個事件訂閱，$odataFilter \` 查詢。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

為資源群組 \` MyResourceGroupName 建立的事件訂閱 EventSubscription1 \` \` 詳細資料 \` 。

### 範例 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

瞭解目前選取的 Azure 訂閱所建立的事件訂閱 \` EventSubscription1 \` 詳細資料。

### 範例 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

在資源群組 MyResourceGroupName 下建立的所有全域事件訂閱清單，而不 \` \` 分頁。

### 範例 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

如果資源群組 MyResourceGroupName (，請列出前 5 個事件訂閱，) 資源群組 MyResourceGroupName 下建立的任何專案，$odataFilter \` \` 查詢。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

在目前選取的 Azure 訂閱下建立的所有全域事件訂閱清單，而不分頁。

### 範例 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出前 15 個全域事件訂閱 (如果) 目前選取的 Azure 訂閱所建立的任何訂閱，$odataFilter查詢。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

在指定的 westus2 資源群組 MyResourceGroupName 下建立的所有地區事件訂閱清單，而不 \` \` \` \` 分頁。

### 範例 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

列出前 15 個區域事件訂閱 (如果資源群組 MyResourceGroupName) 于指定的位置 \` westus2 中建立，以滿足 $odataFilter \` \` \` 查詢。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

獲得為指定的 EventHub 命名空間建立的所有事件訂閱清單，而不分頁。

### 範例 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

如果為指定的 EventHub 命名空間建立 (，請) 前 25 個事件訂閱，$odataFilter查詢。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

為指定的主題類型建立的所有事件訂閱清單， (EventHub 命名空間) 指定位置中，而不分頁。

### 範例 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

在滿足 $odataFilter 查詢的指定位置中 () 為指定主題類型 (EventHub 命名空間) 建立的任何活動訂閱清單前 15 個事件訂閱。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

### 範例 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

無需分頁，即可獲得為特定資源群組建立的所有事件訂閱清單。

### 範例 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

針對滿足查詢的特定資源 (建立) ，請列出前 100 個$odataFilter訂閱。 如果有更多的結果可用，$result。NextLink 將不會$null。 為了取得活動訂閱 () 頁面，使用者預期會重新撥打Get-AzEventGridSubscription並使用結果。從上一個通話取得 NextLink。 結果時，來電者應該停止。NextLink 會變成$null。

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

### -DomainInputObject
EventGrid 網域物件。

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

### -DomainName
EventGrid 功能變數名稱。

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
EventGrid 網域主題物件。

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
EventGrid 網域主題名稱。

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
活動訂閱的名稱

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
包含活動訂閱目的地的完整端點 URL。

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
EventGrid Topic 物件。

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
位置

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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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

### -頂端
用來篩選清單結果的 OData 查詢。 目前僅允許在 Name 屬性上篩選。支援的操作包括：CONTAINS、eq (表示等於) 、ne (不等於) 、AND 和 NOT。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.EventGrid.models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]

## 輸出

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## 筆記

## 相關連結
