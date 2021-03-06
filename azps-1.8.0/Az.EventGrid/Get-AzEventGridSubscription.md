---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622326"
---
# Get-AzEventGridSubscription

## 摘要
取得事件訂閱的詳細資料，或取得目前 Azure 訂閱中的所有事件訂閱清單。

## 句法

### EventSubscriptionTopicNameParameterSet (預設) 
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzEventGridSubscription Cmdlet 會取得指定事件格線訂閱的詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。
如果提供了事件訂閱名稱，則會傳回單一事件格線訂閱的詳細資料。
如果未提供事件訂閱名稱，則會傳回所有事件訂閱的清單。

## 示例

### 範例1
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

取得 \` \` \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的 \` \` 事件訂閱 EventSubscription1 詳細資料。

### 範例2
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` \` \` ，包括完整的端點 URL （如果它是以 webhook 為基礎的事件訂閱）。

### 範例3
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 所建立的所有活動訂閱 \` 清單 \` 。

### 範例4
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

取得 \` \` 針對資源群組 MyResourceGroupName 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` 。

### 範例5
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

取得 \` \` 目前所選 Azure 訂閱所建立之事件訂閱 EventSubscription1 的詳細資料。

### 範例6
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

取得在資源群組 MyResourceGroupName 下所建立的所有全域事件訂閱 \` 清單 \` 。

### 範例7
```
PS C:\> Get-AzEventGridSubscription
```

取得在目前選取的 Azure 訂閱中建立的所有全域事件訂閱清單。

### 範例8
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

取得在 \` \` 指定位置 westus2 中的 [資源群組 MyResourceGroupName] 下所建立的所有區域事件訂閱清單 \` \` 。

### 範例9
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

取得針對指定 EventHub 命名空間所建立之所有事件訂閱的清單。

### 範例10
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

取得在指定位置 (EventHub 命名空間) 中為指定主題類型所建立的所有事件訂閱清單。

### 範例11
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

取得針對特定資源群組所建立的所有事件訂閱清單。

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

### -EventSubscriptionName
事件訂閱的名稱

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
包含事件訂閱目的地的完整端點 URL。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
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

### -TopicName
EventGrid 主題名稱。

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
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
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### PSTopic 中的 EventGrid。

## 輸出

### PSEventSubscription 中的 EventGrid。

## 筆記

## 相關連結
