---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: 7f5c2658b32b0bf713dc131474eca30e57955187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916357"
---
# Az.ServiceBus 模組
## 描述
本主題顯示 Azure Service Bus Cmdlet 的說明主題。

## Az.ServiceBus Cmdlet
### [Complete-AzServiceBusMigration](Complete-AzServiceBusMigration.md)
Cmdlet 將標準命名空間的移轉設定為完成，標準命名空間的連接字串現在會指向進一步命名空間

### [Get-AzServiceBusAuthorizationRule](Get-AzServiceBusAuthorizationRule.md)
獲得指定命名空間或佇列或主題或 GeoDR 組 (別名的指定授權規則) 。 

### [Get-AzServiceBusGeoDRConfiguration](Get-AzServiceBusGeoDRConfiguration.md)
針對主要或 (命名空間，) 復原組選的別名

### [Get-AzServiceBusKey](Get-AzServiceBusKey.md)
在 GeoDR 組配置中，為指定命名空間或佇列或主題或別名 (主要和次要) 。

### [Get-AzServiceBusMigration](Get-AzServiceBusMigration.md)
為命名空間取回 MigrationConfiguration

### [Get-AzServiceBusNamespace](Get-AzServiceBusNamespace.md)
在資源群組中，為指定的 Service Bus 命名空間獲得描述。

### [Get-AzServiceBusOperation](Get-AzServiceBusOperation.md)
清單支援的 ServiceBus Operations

### [Get-AzServiceBusQueue](Get-AzServiceBusQueue.md)
會針對指定的服務母線佇列，返回描述。

### [Get-AzServiceBusRule](Get-AzServiceBusRule.md)
為給定主題訂閱建立新規則。 

### [Get-AzServiceBusSubscription](Get-AzServiceBusSubscription.md)
會針對指定的主題，返回訂閱描述。

### [Get-AzServiceBusTopic](Get-AzServiceBusTopic.md)
會針對指定的 Service Bus 主題，返回描述。

### [New-AzServiceBusAuthorizationRule](New-AzServiceBusAuthorizationRule.md)
為指定的 Service Bus 指定命名空間或佇列或主題建立新授權規則。

### [New-AzServiceBusAuthorizationRuleSASToken](New-AzServiceBusAuthorizationRuleSASToken.md)
產生 AZURE serviucebus 授權規則的 SAS tolen 命名空間/佇列/topic。 

### [New-AzServiceBusGeoDRConfiguration](New-AzServiceBusGeoDRConfiguration.md)
建立新的別名 (復原組) 

### [New-AzServiceBusKey](New-AzServiceBusKey.md)
重新產生 Service Bus 命名空間或佇列或主題的主要或次要連接字串。

### [New-AzServiceBusNamespace](New-AzServiceBusNamespace.md)
建立一個新的 Service Bus 命名空間。

### [New-AzServiceBusQueue](New-AzServiceBusQueue.md)
在指定的 Service Bus 命名空間中建立服務母線佇列。

### [New-AzServiceBusRule](New-AzServiceBusRule.md)
為給定主題訂閱建立新規則。 

### [New-AzServiceBusSubscription](New-AzServiceBusSubscription.md)
建立指定 Service Bus 主題的訂閱。

### [New-AzServiceBusTopic](New-AzServiceBusTopic.md)
在指定的 Service Bus 命名空間中建立新 Service Bus 主題。

### [Remove-AzServiceBusAuthorizationRule](Remove-AzServiceBusAuthorizationRule.md)
從指定的資源群組移除 Service Bus 命名空間或佇列或主題的授權規則。

### [Remove-AzServiceBusGeoDRConfiguration](Remove-AzServiceBusGeoDRConfiguration.md)
刪除復原 (的別名) 

### [Remove-AzServiceBusMigration](Remove-AzServiceBusMigration.md)
Cmdlet 會刪除標準到進一步命名空間的移轉組

### [Remove-AzServiceBusNamespace](Remove-AzServiceBusNamespace.md)
從指定的資源群組移除命名空間。 

### [Remove-AzServiceBusQueue](Remove-AzServiceBusQueue.md)
從指定的 Service Bus 命名空間移除佇列。

### [Remove-AzServiceBusRule](Remove-AzServiceBusRule.md)
移除指定訂閱的指定規則。

### [Remove-AzServiceBusSubscription](Remove-AzServiceBusSubscription.md)
從指定的 Service Bus 命名空間移除主題的訂閱。

### [Remove-AzServiceBusTopic](Remove-AzServiceBusTopic.md)
從指定的 Service Bus 命名空間移除主題。

### [Set-AzServiceBusAuthorizationRule](Set-AzServiceBusAuthorizationRule.md)
更新指定 Service Bus 命名空間或佇列或主題的指定授權規則描述。

### [Set-AzServiceBusGeoDRConfigurationBreakPair](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
此作業會停用災害復原，並停止從主要命名空間複製到次要命名空間的變更

### [Set-AzServiceBusGeoDRConfigurationFailOver](Set-AzServiceBusGeoDRConfigurationFailOver.md)
會調用 GEO DR 容錯移轉，並重新指定別名以指向次要命名空間

### [Set-AzServiceBusNamespace](Set-AzServiceBusNamespace.md)
更新現有 Service Bus 命名空間的描述。

### [Set-AzServiceBusQueue](Set-AzServiceBusQueue.md)
更新指定 Service Bus 命名空間中服務母線佇列的描述。

### [Set-AzServiceBusRule](Set-AzServiceBusRule.md)
更新指定訂閱的指定規則描述。

### [Set-AzServiceBusSubscription](Set-AzServiceBusSubscription.md)
更新指定 Service Bus 命名空間中 Service Bus 主題的訂閱描述。

### [Set-AzServiceBusTopic](Set-AzServiceBusTopic.md)
更新指定 Service Bus 命名空間中 Service Bus 主題的描述。

### [Start-AzServiceBusMigration](Start-AzServiceBusMigration.md)
建立新的移移組，並開始將實體從標準命名空間移為進級命名空間

### [Stop-AzServiceBusMigration](Stop-AzServiceBusMigration.md)
{{Fill in The Synopsis}}

### [Test-AzServiceBusName](Test-AzServiceBusName.md)
檢查指定 NameSpace 名稱或別名 (DR 組)  

