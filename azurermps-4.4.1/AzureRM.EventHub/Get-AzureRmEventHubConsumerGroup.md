---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456680"
---
# Get-AzureRmEventHubConsumerGroup

## 摘要
取得指定事件中樞消費者群組的詳細資料，或取得事件中樞中的消費者群組清單。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## 說明
Get-AzureRmEventHubConsumerGroup Cmdlet 會取得指定事件中樞消費者群組的詳細資料，或指定事件中樞中的消費者群組清單。
如果提供消費者群組的名稱，則會傳回單一消費者群組詳細資料的詳細資料。
如果未提供消費者群組的名稱，則會傳回指定事件中樞中的消費者群組清單。

## 示例

### 範例1
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

\` \` 在事件中心 MyEventHubName 中取得消費者群組 MyConsumerGroupName，該活動中心已 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。

### 範例2
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

在事件中心 MyEventHubName 中取得消費者群組的清單，該使用者群組 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。

## 參數

### -ResourceGroupName
資源組名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHub
EventHub Name。

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
ConsumerGroup [名稱]。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -命名空間
命名空間名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 輸入

### System.object

## 輸出

### [System.object]。清單 ' 1 [ConsumerGroupAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））

## 筆記

## 相關連結

