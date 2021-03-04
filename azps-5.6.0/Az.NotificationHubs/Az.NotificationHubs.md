---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901778"
---
# Az.NotificationHubs 模組
## 描述
本主題顯示 Azure 通知中樞 Cmdlet 的說明主題。 通知中樞可用來傳送推入通知給多個用戶端 (不論這些用戶端所使用的平臺 (iOS、Android、Windows Phone 8、Windows 市集等 ) 。 這些中樞大致相當於個別的應用程式：每一個 App 通常會有自己的通知中樞。 通知中樞是組織在稱為命名空間的邏輯容器內，而共用存取簽章 (SAS) 授權規則則用來管理中樞和命名空間的存取權。 所有這些元素都可以使用通知中樞 Cmdlet 來管理。

## Az.NotificationHubs Cmdlet
### [Get-AzNotificationHub](Get-AzNotificationHub.md)
獲得有關通知中樞的資訊。

### [Get-AzNotificationHubAuthorizationRule](Get-AzNotificationHubAuthorizationRule.md)
獲得與通知中樞相關聯的授權規則相關資訊。

### [Get-AzNotificationHubListKey](Get-AzNotificationHubListKey.md)
獲得與通知中樞授權規則相關聯的主要和次要連接字串。

### [Get-AzNotificationHubPNSCredential](Get-AzNotificationHubPNSCredential.md)
獲得通知中樞的 PNS 認證。

### [Get-AzNotificationHubsNamespace](Get-AzNotificationHubsNamespace.md)
獲得通知中樞命名空間相關資訊。

### [Get-AzNotificationHubsNamespaceAuthorizationRule](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
與通知中樞命名空間相關聯的授權規則相關資訊。

### [Get-AzNotificationHubsNamespaceListKey](Get-AzNotificationHubsNamespaceListKey.md)
獲得與通知中樞命名空間授權規則相關聯的主要和次要連接字串。

### [New-AzNotificationHub](New-AzNotificationHub.md)
建立通知中樞。

### [New-AzNotificationHubAuthorizationRule](New-AzNotificationHubAuthorizationRule.md)
建立授權規則，並將規則指派給通知中樞。

### [New-AzNotificationHubKey](New-AzNotificationHubKey.md)
重新產生 NotificationHub 的授權規則金鑰。

### [New-AzNotificationHubsNamespace](New-AzNotificationHubsNamespace.md)
建立通知中樞命名空間。

### [New-AzNotificationHubsNamespaceAuthorizationRule](New-AzNotificationHubsNamespaceAuthorizationRule.md)
建立授權規則，並將該規則指派給通知中樞命名空間。

### [New-AzNotificationHubsNamespaceKey](New-AzNotificationHubsNamespaceKey.md)
重新產生命名空間的授權規則金鑰。

### [Remove-AzNotificationHub](Remove-AzNotificationHub.md)
移除現有的通知中樞。

### [Remove-AzNotificationHubAuthorizationRule](Remove-AzNotificationHubAuthorizationRule.md)
從通知中樞移除授權規則。

### [Remove-AzNotificationHubsNamespace](Remove-AzNotificationHubsNamespace.md)
移除通知中樞命名空間。

### [Remove-AzNotificationHubsNamespaceAuthorizationRule](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
從通知中樞命名空間移除授權規則。

### [Set-AzNotificationHub](Set-AzNotificationHub.md)
設定通知中樞的屬性值。

### [Set-AzNotificationHubAuthorizationRule](Set-AzNotificationHubAuthorizationRule.md)
設定通知中樞的授權規則。

### [Set-AzNotificationHubsNamespace](Set-AzNotificationHubsNamespace.md)
設定通知中樞命名空間的屬性值。

### [Set-AzNotificationHubsNamespaceAuthorizationRule](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
設定通知中樞命名空間的授權規則。

