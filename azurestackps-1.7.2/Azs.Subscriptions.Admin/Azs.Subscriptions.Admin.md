---
Module Name: Azs.Subscriptions.Admin
Module Guid: 60c5ab08-9482-4a99-b973-141ac294c07a
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 973fea5c015e35efaf36d98634235b273a447140
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/17/2019
ms.locfileid: "93611384"
---
# Azs 訂閱. 系統管理模組
## 說明
AzureStack 訂閱操作員模組的預覽版本。  此模組提供管理方案、優惠及訂閱的操作員功能

## Azs 訂閱. 系統管理 Cmdlet
### [附加 AzsPlanToOffer](Add-AzsPlanToOffer.md)
將計畫連結至優惠。

### [AzsDelegatedProvider](Get-AzsDelegatedProvider.md)
取得 delegatedProviders 清單。

### [AzsDelegatedProviderManagedOffer](Get-AzsDelegatedProviderManagedOffer.md)
取得委派提供者的提供方案清單。

### [AzsDirectoryTenant](Get-AzsDirectoryTenant.md)
列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。

### [AzsLocation](Get-AzsLocation.md)
取得所有 AzureStack 位置的清單。

### [AzsManagedOffer](Get-AzsManagedOffer.md)
取得提供者清單做為運算子。

### [AzsOfferDelegation](Get-AzsOfferDelegation.md)
取得委派優惠清單。

### [AzsOfferMetric](Get-AzsOfferMetric.md)
取得優惠指標。

### [AzsPlan](Get-AzsPlan.md)
列出所有訂閱的所有方案。

### [AzsPlanMetric](Get-AzsPlanMetric.md)
取得計畫度量單位。

### [AzsSubscriptionPlan](Get-AzsSubscriptionPlan.md)
取得訂閱可存取的所有取得方案集合。

### [AzsSubscriptionsQuota](Get-AzsSubscriptionsQuota.md)
取得位置的訂閱資源提供者配額清單。

### [AzsUserSubscription](Get-AzsUserSubscription.md)
取得使用者訂閱清單做為操作員。

### [移動流覽 AzsSubscription](Move-AzsSubscription.md)
在委派的提供者優惠之間移動訂閱。
這個程式只會執行 rebranding，不會變更訂閱的基礎方案、方案和配額。

### [新-AddonPlanDefinitionObject](New-AddonPlanDefinitionObject.md)
包含要連結或取消連結至優惠的所需方案名稱。

### [新-AzsOffer](New-AzsOffer.md)
建立新的優惠。

### [新-AzsOfferDelegation](New-AzsOfferDelegation.md)
建立新的 [優惠委派]。

### [新-AzsPlan](New-AzsPlan.md)
建立新方案

### [新-AzsSubscriptionPlan](New-AzsSubscriptionPlan.md)
建立訂閱者案。

### [新-AzsUserSubscription](New-AzsUserSubscription.md)
建立新的訂閱。

### [移除-AzsOffer](Remove-AzsOffer.md)
刪除指定的優惠。

### [移除-AzsOfferDelegation](Remove-AzsOfferDelegation.md)
移除 [提供委派]

### [移除-AzsPlan](Remove-AzsPlan.md)
移除指定的方案

### [移除-AzsPlanFromOffer](Remove-AzsPlanFromOffer.md)
從優惠中取消連結方案。

### [移除-AzsSubscriptionPlan](Remove-AzsSubscriptionPlan.md)
刪除訂閱者案。

### [移除-AzsUserSubscription](Remove-AzsUserSubscription.md)
移除指定的租使用者訂閱。

### [Set-AzsOffer](Set-AzsOffer.md)
更新優惠。

### [Set-AzsOfferDelegation](Set-AzsOfferDelegation.md)
更新 [提供委派]。

### [Set-AzsPlan](Set-AzsPlan.md)
更新指定的方案

### [Set-AzsUserSubscription](Set-AzsUserSubscription.md)
更新指定的使用者訂閱

### [Test-AzsMoveSubscription](Test-AzsMoveSubscription.md)
確認使用者訂閱可以在委派的提供者提供的服務之間移動。

### [Test-AzsNameAvailability](Test-AzsNameAvailability.md)
傳回指定訂閱資源類型和名稱的 avaialbility

