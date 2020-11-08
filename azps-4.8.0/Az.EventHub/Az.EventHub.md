---
Module Name: Az.EventHub
Module Guid: 5728d353-7ad5-42d8-b00a-46aaecf07b91
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.eventhub
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
ms.openlocfilehash: 55b29c8e78039c97b867ae39556b5d9a2383bd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136420"
---
# Az （EventHub）模組
## 說明
本主題顯示 Azure 事件中心 PowerShell 資源管理器 Cmdlet 的說明。

## Az Cmdlet
### [附加 AzEventHubIPRule](Add-AzEventHubIPRule.md)
在指定命名空間的 NetworkRuleSet 中新增單一 IP 規則

### [附加 AzEventHubVirtualNetworkRule](Add-AzEventHubVirtualNetworkRule.md)
針對指定的命名空間新增單一 VirtualNetworkRule 至 NetworkRuleSet

### [AzEventHub](Get-AzEventHub.md)
取得單一事件中心的詳細資料，或取得事件中心的清單。

### [AzEventHubAuthorizationRule](Get-AzEventHubAuthorizationRule.md)
取得授權規則的詳細資料，或取得授權規則清單。

### [AzEventHubCluster](Get-AzEventHubCluster.md)
取得單一專用事件中心群集的詳細資料，或取得指定 Resourcegroup 中專用事件中樞群集的清單。

### [AzEventHubClustersAvailableRegion](Get-AzEventHubClustersAvailableRegion.md)
取得可使用專用事件中心群組的地區清單

### [AzEventHubConsumerGroup](Get-AzEventHubConsumerGroup.md)
取得指定事件中樞消費者群組的詳細資料，或取得事件中樞中的消費者群組清單。

### [AzEventHubGeoDRConfiguration](Get-AzEventHubGeoDRConfiguration.md)
檢索主要或次要命名空間的別名 (災害復原設定) 

### [AzEventHubKey](Get-AzEventHubKey.md)
取得指定事件中心授權規則的主要金鑰詳細資料。

### [AzEventHubNamespace](Get-AzEventHubNamespace.md)
取得事件中心命名空間的詳細資料，或取得目前 Azure 訂閱中所有事件中心命名空間的清單。

### [AzEventHubNetworkRuleSet](Get-AzEventHubNetworkRuleSet.md)
取得目前 Azure 訂閱中的命名空間事件中心 NetworkruleSet 的詳細資料。

### [新-AzEventHub](New-AzEventHub.md)
建立新的事件中樞。

### [新-AzEventHubAuthorizationRule](New-AzEventHubAuthorizationRule.md)
為 namespace 或 eventhub 建立新的事件中心授權規則。

### [新-AzEventHubAuthorizationRuleSASToken](New-AzEventHubAuthorizationRuleSASToken.md)
針對命名空間/eventhub 的 Azure eventhub 授權規則產生 SAS tolen。

### [新-AzEventHubCluster](New-AzEventHubCluster.md)
在指定的資源群組和位置中建立新的專用 Eventhub 群集

### [新-AzEventHubConsumerGroup](New-AzEventHubConsumerGroup.md)
針對指定的事件中心建立新的消費者群組。

### [新-AzEventHubGeoDRConfiguration](New-AzEventHubGeoDRConfiguration.md)
 (災害復原設定建立新的別名) 

### [新-AzEventHubKey](New-AzEventHubKey.md)
針對指定的事件中心授權規則，建立新的主要或次要金鑰。

### [新-AzEventHubNamespace](New-AzEventHubNamespace.md)
建立事件中樞命名空間。

### [移除-AzEventHubIPRule](Remove-AzEventHubIPRule.md)
移除單一 IP 規則至指定命名空間的 NetworkRuleSet

### [移除-AzEventHub](Remove-AzEventHub.md)
移除指定的事件中樞。

### [移除-AzEventHubVirtualNetworkRule](Remove-AzEventHubVirtualNetworkRule.md)
移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule

### [移除-AzEventHubNetworkRuleSet](Remove-AzEventHubNetworkRuleSet.md)
移除指定命名空間的 NetworkRuleSet

### [移除-AzEventHubAuthorizationRule](Remove-AzEventHubAuthorizationRule.md)
移除指定的事件中心授權規則。

### [移除-AzEventHubCluster](Remove-AzEventHubCluster.md)
從 ResourceGroup 中刪除指定的專用 Eventhub 群集

### [移除-AzEventHubConsumerGroup](Remove-AzEventHubConsumerGroup.md)
刪除指定的事件中樞消費者群組。

### [移除-AzEventHubGeoDRConfiguration](Remove-AzEventHubGeoDRConfiguration.md)
刪除 (災害復原設定的別名) 

### [移除-AzEventHubNamespace](Remove-AzEventHubNamespace.md)
移除指定的事件中樞命名空間。

### [Set-AzEventHub](Set-AzEventHub.md)
更新指定的事件中樞。

### [Set-AzEventHubAuthorizationRule](Set-AzEventHubAuthorizationRule.md)
更新事件中樞上的指定授權規則。

### [Set-AzEventHubCluster](Set-AzEventHubCluster.md)
更新指定群集的標記

### [Set-AzEventHubConsumerGroup](Set-AzEventHubConsumerGroup.md)
更新指定的事件中樞消費者群組。

### [Set-AzEventHubGeoDRConfigurationBreakPair](Set-AzEventHubGeoDRConfigurationBreakPair.md)
這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間

### [Set-AzEventHubGeoDRConfigurationFailOver](Set-AzEventHubGeoDRConfigurationFailOver.md)
調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間

### [Set-AzEventHubNamespace](Set-AzEventHubNamespace.md)
更新指定的事件中樞命名空間。

### [Set-AzEventHubNetworkRuleSet](Set-AzEventHubNetworkRuleSet.md)
更新目前 Azure 訂閱中指定命名空間的 NetworkruleSet。

### [Test-AzEventHubName](Test-AzEventHubName.md)
檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) 

