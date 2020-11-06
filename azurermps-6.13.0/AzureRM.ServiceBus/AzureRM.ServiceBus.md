---
Module Name: AzureRM.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/AzureRM.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/AzureRM.ServiceBus.md
ms.openlocfilehash: e7ee7c94e704305803f47223e8974bbf3f5b1bdd
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611254"
---
# AzureRM 模組
## 說明
本主題顯示 Azure 服務匯流排 Cmdlet 的說明主題。

## AzureRM 的 Cmdlet
### [完成-AzureRmServiceBusMigration](Complete-AzureRmServiceBusMigration.md)
Cmdlet 將 [從標準到 premium] 命名空間的遷移設定為完成，而標準命名空間的連線字串現在指向 [Premium 命名空間]

### [AzureRmServiceBusAuthorizationRule](Get-AzureRmServiceBusAuthorizationRule.md)
針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得指定授權規則的描述) 。 

### [AzureRmServiceBusGeoDRConfiguration](Get-AzureRmServiceBusGeoDRConfiguration.md)
檢索主要或次要命名空間的別名 (災害復原設定) 

### [AzureRmServiceBusKey](Get-AzureRmServiceBusKey.md)
針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得) 的主要及次要連接字串。

### [AzureRmServiceBusMigration](Get-AzureRmServiceBusMigration.md)
檢索命名空間的 MigrationConfiguration

### [AzureRmServiceBusNamespace](Get-AzureRmServiceBusNamespace.md)
取得資源群組中指定服務匯流排命名空間的描述。

### [AzureRmServiceBusOperation](Get-AzureRmServiceBusOperation.md)
清單支援的未列作業

### [AzureRmServiceBusQueue](Get-AzureRmServiceBusQueue.md)
傳回指定服務匯流排佇列的描述。

### [AzureRmServiceBusRule](Get-AzureRmServiceBusRule.md)
針對特定主題的訂閱建立新規則。 

### [AzureRmServiceBusSubscription](Get-AzureRmServiceBusSubscription.md)
傳回指定主題的訂閱描述。

### [AzureRmServiceBusTopic](Get-AzureRmServiceBusTopic.md)
傳回指定服務匯流排主題的描述。

### [新-AzureRmServiceBusAuthorizationRule](New-AzureRmServiceBusAuthorizationRule.md)
針對指定的服務匯流排指定命名空間或佇列或主題，建立新的授權規則。

### [新-AzureRmServiceBusGeoDRConfiguration](New-AzureRmServiceBusGeoDRConfiguration.md)
 (災害復原設定建立新的別名) 

### [新-AzureRmServiceBusKey](New-AzureRmServiceBusKey.md)
重新生成服務匯流排命名空間或佇列或主題的主要或次要連線字串。

### [新-AzureRmServiceBusNamespace](New-AzureRmServiceBusNamespace.md)
建立新的服務匯流排命名空間。

### [新-AzureRmServiceBusQueue](New-AzureRmServiceBusQueue.md)
在指定的服務匯流排命名空間中建立服務匯流排佇列。

### [新-AzureRmServiceBusRule](New-AzureRmServiceBusRule.md)
針對特定主題的訂閱建立新規則。 

### [新-AzureRmServiceBusSubscription](New-AzureRmServiceBusSubscription.md)
建立指定服務匯流排主題的訂閱。

### [新-AzureRmServiceBusTopic](New-AzureRmServiceBusTopic.md)
在指定的服務匯流排命名空間中建立新的服務匯流排主題。

### [移除-AzureRmServiceBusAuthorizationRule](Remove-AzureRmServiceBusAuthorizationRule.md)
從指定的資源群組中移除服務匯流排命名空間或佇列或主題的授權規則。

### [移除-AzureRmServiceBusGeoDRConfiguration](Remove-AzureRmServiceBusGeoDRConfiguration.md)
刪除 (災害復原設定的別名) 

### [移除-AzureRmServiceBusMigration](Remove-AzureRmServiceBusMigration.md)
Cmdlet 會刪除標準至 Premium 命名空間的遷移配置

### [移除-AzureRmServiceBusNamespace](Remove-AzureRmServiceBusNamespace.md)
從指定的資源群組中移除命名空間。 

### [移除-AzureRmServiceBusQueue](Remove-AzureRmServiceBusQueue.md)
從指定的服務匯流排命名空間中移除佇列。

### [移除-AzureRmServiceBusRule](Remove-AzureRmServiceBusRule.md)
移除指定訂閱的指定規則。

### [移除-AzureRmServiceBusSubscription](Remove-AzureRmServiceBusSubscription.md)
從指定的服務匯流排命名空間移除主題的訂閱。

### [移除-AzureRmServiceBusTopic](Remove-AzureRmServiceBusTopic.md)
從指定的服務匯流排命名空間中移除主題。

### [Set-AzureRmServiceBusAuthorizationRule](Set-AzureRmServiceBusAuthorizationRule.md)
針對指定的服務匯流排命名空間或佇列或主題更新指定的授權規則描述。

### [Set-AzureRmServiceBusGeoDRConfigurationBreakPair](Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md)
這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間

### [Set-AzureRmServiceBusGeoDRConfigurationFailOver](Set-AzureRmServiceBusGeoDRConfigurationFailOver.md)
調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間

### [Set-AzureRmServiceBusNamespace](Set-AzureRmServiceBusNamespace.md)
更新現有服務匯流排命名空間的描述。

### [Set-AzureRmServiceBusQueue](Set-AzureRmServiceBusQueue.md)
更新指定服務匯流排命名空間中服務匯流排佇列的描述。

### [Set-AzureRmServiceBusRule](Set-AzureRmServiceBusRule.md)
針對指定的訂閱更新指定的規則描述。

### [Set-AzureRmServiceBusSubscription](Set-AzureRmServiceBusSubscription.md)
更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。

### [Set-AzureRmServiceBusTopic](Set-AzureRmServiceBusTopic.md)
更新指定服務匯流排命名空間中服務匯流排主題的描述。

### [開始-AzureRmServiceBusMigration](Start-AzureRmServiceBusMigration.md)
建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移

### [停止 AzureRmServiceBusMigration](Stop-AzureRmServiceBusMigration.md)
終止從標準到 premium 命名空間之間的遷移

### [Test-AzureRmServiceBusName](Test-AzureRmServiceBusName.md)
檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性)  

