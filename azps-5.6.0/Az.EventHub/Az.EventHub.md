---
Module Name: Az.EventHub
Module Guid: 5728d353-7ad5-42d8-b00a-46aaecf07b91
Download Help Link: https://docs.microsoft.com/powershell/module/az.eventhub
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
ms.openlocfilehash: 1f609980fe6806f4918fb53daa0600a244c4ac94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912857"
---
# Az.EventHub 模組
## 描述
本主題顯示 Azure 事件中樞 PowerShell 資源管理器 Cmdlet 說明。

## Az.EventHub Cmdlet
### [Add-AzEventHubIPRule](Add-AzEventHubIPRule.md)
新增單一 IP 規則至給定命名空間的 NetworkRuleSet

### [Add-AzEventHubVirtualNetworkRule](Add-AzEventHubVirtualNetworkRule.md)
為給定命名空間新增單一 VirtualNetworkRule 到 NetworkRuleSet

### [Get-AzEventHub](Get-AzEventHub.md)
獲得單一事件中樞的詳細資訊，或獲得事件中樞清單。

### [Get-AzEventHubAuthorizationRule](Get-AzEventHubAuthorizationRule.md)
獲得授權規則的詳細資訊，或獲得授權規則清單。

### [Get-AzEventHubCluster](Get-AzEventHubCluster.md)
獲得單一專用事件中樞組的詳細資訊，或獲得特定資源組中專屬事件中樞組的清單。

### [Get-AzEventHubClustersAvailableRegion](Get-AzEventHubClustersAvailableRegion.md)
獲得提供專用事件中樞集區集的地區清單

### [Get-AzEventHubConsumerGroup](Get-AzEventHubConsumerGroup.md)
獲得指定的事件中樞消費者群組詳細資料，或獲得事件中樞中的消費者群組清單。

### [Get-AzEventHubGeoDRConfiguration](Get-AzEventHubGeoDRConfiguration.md)
針對主要或 (命名空間，) 復原組選的別名

### [Get-AzEventHubKey](Get-AzEventHubKey.md)
獲得指定事件中樞授權規則的主鍵詳細資料。

### [Get-AzEventHubNamespace](Get-AzEventHubNamespace.md)
獲得事件中樞命名空間的詳細資訊，或獲得目前 Azure 訂閱中所有事件中樞命名空間的清單。

### [Get-AzEventHubNetworkRuleSet](Get-AzEventHubNetworkRuleSet.md)
瞭解目前 Azure 訂閱中命名空間的事件中樞 NetworkruleSet 詳細資料。

### [New-AzEventHub](New-AzEventHub.md)
建立新事件中樞。

### [New-AzEventHubAuthorizationRule](New-AzEventHubAuthorizationRule.md)
為命名空間或事件中心建立新事件中樞授權規則。

### [New-AzEventHubAuthorizationRuleSASToken](New-AzEventHubAuthorizationRuleSASToken.md)
產生適用于 Azure eventhub 授權規則的 SAS tolen 命名空間/eventhub。

### [New-AzEventHubCluster](New-AzEventHubCluster.md)
在指定資源群組和位置中建立新專屬的 Eventhub 群組

### [New-AzEventHubConsumerGroup](New-AzEventHubConsumerGroup.md)
為指定的事件中樞建立新的消費者群組。

### [New-AzEventHubGeoDRConfiguration](New-AzEventHubGeoDRConfiguration.md)
建立新的別名 (復原組) 

### [New-AzEventHubKey](New-AzEventHubKey.md)
為指定的事件中樞授權規則建立新的主鍵或次要金鑰。

### [New-AzEventHubNamespace](New-AzEventHubNamespace.md)
建立事件中樞命名空間。

### [Remove-AzEventHubIPRule](Remove-AzEventHubIPRule.md)
將單一 IP 規則移除至給定命名空間的 NetworkRuleSet

### [Remove-AzEventHub](Remove-AzEventHub.md)
移除指定的事件中樞。

### [Remove-AzEventHubVirtualNetworkRule](Remove-AzEventHubVirtualNetworkRule.md)
移除命名空間 NetworkRuleSet 的單一專用 VirtualNetworkRule

### [Remove-AzEventHubNetworkRuleSet](Remove-AzEventHubNetworkRuleSet.md)
移除給定命名空間的 NetworkRuleSet

### [Remove-AzEventHubAuthorizationRule](Remove-AzEventHubAuthorizationRule.md)
移除指定的事件中樞授權規則。

### [Remove-AzEventHubCluster](Remove-AzEventHubCluster.md)
從 ResourceGroup 刪除指定的 Dedicated Eventhub 群

### [Remove-AzEventHubConsumerGroup](Remove-AzEventHubConsumerGroup.md)
刪除指定的事件中樞消費者群組。

### [Remove-AzEventHubGeoDRConfiguration](Remove-AzEventHubGeoDRConfiguration.md)
刪除復原 (的別名) 

### [Remove-AzEventHubNamespace](Remove-AzEventHubNamespace.md)
移除指定的事件中樞命名空間。

### [Set-AzEventHub](Set-AzEventHub.md)
更新指定的事件中樞。

### [Set-AzEventHubAuthorizationRule](Set-AzEventHubAuthorizationRule.md)
更新事件中樞上指定的授權規則。

### [Set-AzEventHubCluster](Set-AzEventHubCluster.md)
更新給定組群的標記

### [Set-AzEventHubConsumerGroup](Set-AzEventHubConsumerGroup.md)
更新指定的事件中樞消費者群組。

### [Set-AzEventHubGeoDRConfigurationBreakPair](Set-AzEventHubGeoDRConfigurationBreakPair.md)
此作業會停用災害復原，並停止從主要命名空間複製到次要命名空間的變更

### [Set-AzEventHubGeoDRConfigurationFailOver](Set-AzEventHubGeoDRConfigurationFailOver.md)
會調用 GEO DR 容錯移轉，並重新指定別名以指向次要命名空間

### [Set-AzEventHubNamespace](Set-AzEventHubNamespace.md)
更新指定的事件中樞命名空間。

### [Set-AzEventHubNetworkRuleSet](Set-AzEventHubNetworkRuleSet.md)
更新目前 Azure 訂閱中給定命名空間的 NetworkruleSet。

### [Test-AzEventHubName](Test-AzEventHubName.md)
檢查指定 NameSpace 名稱或別名 (DR 組) 

