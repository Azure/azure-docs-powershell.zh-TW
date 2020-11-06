---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453520"
---
# Get-AzureRmEventGridTopic

## 摘要
取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ResourceGroupNameParameterSet (預設) 
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzureRmEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。
如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。
如果未提供主題名稱，則會傳回主題的清單。

## 示例

### 範例1
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。

### 範例2
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。

### 範例3
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題 \` \` 。

### 範例4
```
PS C:\> Get-AzureRmEventGridTopic
```

列出訂閱中的所有事件格線主題。

## 參數

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object
PSTopic 中的 EventGrid。

## 輸出

### PSTopic 中的 EventGrid。
[System.object]。清單 ' 1 [EventGrid. PSTopicListInstance，EventGrid，版本 = 1.0.0.0，Culture = 非特定，PublicKeyToken = null]] （限）

## 筆記

## 相關連結

