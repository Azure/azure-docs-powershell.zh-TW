---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: a20ecc91cd2597eb3ce846da2e43e3da861b12fd
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611210"
---
# Az 模組
## 說明
本主題顯示 Azure 服務匯流排 Cmdlet 的說明主題。

## Az 的 Cmdlet
### [完成-AzServiceBusMigration](Complete-AzServiceBusMigration.md)
Cmdlet 將 [從標準到 premium] 命名空間的遷移設定為完成，而標準命名空間的連線字串現在指向 [Premium 命名空間]

### [AzServiceBusAuthorizationRule](Get-AzServiceBusAuthorizationRule.md)
針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得指定授權規則的描述) 。 

### [AzServiceBusGeoDRConfiguration](Get-AzServiceBusGeoDRConfiguration.md)
檢索主要或次要命名空間的別名 (災害復原設定) 

### [AzServiceBusKey](Get-AzServiceBusKey.md)
針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得) 的主要及次要連接字串。

### [AzServiceBusMigration](Get-AzServiceBusMigration.md)
檢索命名空間的 MigrationConfiguration

### [AzServiceBusNamespace](Get-AzServiceBusNamespace.md)
取得資源群組中指定服務匯流排命名空間的描述。

### [AzServiceBusOperation](Get-AzServiceBusOperation.md)
清單支援的未列作業

### [AzServiceBusQueue](Get-AzServiceBusQueue.md)
傳回指定服務匯流排佇列的描述。

### [AzServiceBusRule](Get-AzServiceBusRule.md)
針對特定主題的訂閱建立新規則。 

### [AzServiceBusSubscription](Get-AzServiceBusSubscription.md)
傳回指定主題的訂閱描述。

### [AzServiceBusTopic](Get-AzServiceBusTopic.md)
傳回指定服務匯流排主題的描述。

### [新-AzServiceBusAuthorizationRule](New-AzServiceBusAuthorizationRule.md)
針對指定的服務匯流排指定命名空間或佇列或主題，建立新的授權規則。

### [新-AzServiceBusGeoDRConfiguration](New-AzServiceBusGeoDRConfiguration.md)
 (災害復原設定建立新的別名) 

### [新-AzServiceBusKey](New-AzServiceBusKey.md)
重新生成服務匯流排命名空間或佇列或主題的主要或次要連線字串。

### [新-AzServiceBusNamespace](New-AzServiceBusNamespace.md)
建立新的服務匯流排命名空間。

### [新-AzServiceBusQueue](New-AzServiceBusQueue.md)
在指定的服務匯流排命名空間中建立服務匯流排佇列。

### [新-AzServiceBusRule](New-AzServiceBusRule.md)
針對特定主題的訂閱建立新規則。 

### [新-AzServiceBusSubscription](New-AzServiceBusSubscription.md)
建立指定服務匯流排主題的訂閱。

### [新-AzServiceBusTopic](New-AzServiceBusTopic.md)
在指定的服務匯流排命名空間中建立新的服務匯流排主題。

### [移除-AzServiceBusAuthorizationRule](Remove-AzServiceBusAuthorizationRule.md)
從指定的資源群組中移除服務匯流排命名空間或佇列或主題的授權規則。

### [移除-AzServiceBusGeoDRConfiguration](Remove-AzServiceBusGeoDRConfiguration.md)
刪除 (災害復原設定的別名) 

### [移除-AzServiceBusMigration](Remove-AzServiceBusMigration.md)
Cmdlet 會刪除標準至 Premium 命名空間的遷移配置

### [移除-AzServiceBusNamespace](Remove-AzServiceBusNamespace.md)
從指定的資源群組中移除命名空間。 

### [移除-AzServiceBusQueue](Remove-AzServiceBusQueue.md)
從指定的服務匯流排命名空間中移除佇列。

### [移除-AzServiceBusRule](Remove-AzServiceBusRule.md)
移除指定訂閱的指定規則。

### [移除-AzServiceBusSubscription](Remove-AzServiceBusSubscription.md)
從指定的服務匯流排命名空間移除主題的訂閱。

### [移除-AzServiceBusTopic](Remove-AzServiceBusTopic.md)
從指定的服務匯流排命名空間中移除主題。

### [Set-AzServiceBusAuthorizationRule](Set-AzServiceBusAuthorizationRule.md)
針對指定的服務匯流排命名空間或佇列或主題更新指定的授權規則描述。

### [Set-AzServiceBusGeoDRConfigurationBreakPair](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間

### [Set-AzServiceBusGeoDRConfigurationFailOver](Set-AzServiceBusGeoDRConfigurationFailOver.md)
調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間

### [Set-AzServiceBusNamespace](Set-AzServiceBusNamespace.md)
更新現有服務匯流排命名空間的描述。

### [Set-AzServiceBusQueue](Set-AzServiceBusQueue.md)
更新指定服務匯流排命名空間中服務匯流排佇列的描述。

### [Set-AzServiceBusRule](Set-AzServiceBusRule.md)
針對指定的訂閱更新指定的規則描述。

### [Set-AzServiceBusSubscription](Set-AzServiceBusSubscription.md)
更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。

### [Set-AzServiceBusTopic](Set-AzServiceBusTopic.md)
更新指定服務匯流排命名空間中服務匯流排主題的描述。

### [開始-AzServiceBusMigration](Start-AzServiceBusMigration.md)
建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移

### [停止 AzServiceBusMigration](Stop-AzServiceBusMigration.md)
{{填入摘要}}

### [Test-AzServiceBusName](Test-AzServiceBusName.md)
檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性)  

