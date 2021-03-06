---
Module Name: Az.MySql
Module Guid: 0b8ac9f4-b926-4ac8-b73f-937a0d218521
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.mysql
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Az.MySql.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Az.MySql.md
ms.openlocfilehash: 77da7c2edb3ff01360b2446b96973a01970666a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132679"
---
# Az （MySql）模組
## 說明
Microsoft Azure PowerShell： MySql Cmdlet

## Az. MySql Cmdlet
### [AzMySqlConfiguration](Get-AzMySqlConfiguration.md)
取得伺服器設定的相關資訊。

### [AzMySqlConnectionString](Get-AzMySqlConnectionString.md)
根據用戶端連線提供者取得連接字串。

### [AzMySqlFirewallRule](Get-AzMySqlFirewallRule.md)
取得伺服器防火牆規則的相關資訊。

### [AzMySqlFlexibleServer](Get-AzMySqlFlexibleServer.md)
取得伺服器的相關資訊。

### [AzMySqlFlexibleServerConfiguration](Get-AzMySqlFlexibleServerConfiguration.md)
取得伺服器設定的相關資訊。

### [AzMySqlFlexibleServerConnectionString](Get-AzMySqlFlexibleServerConnectionString.md)
根據用戶端連線提供者取得連接字串。

### [AzMySqlFlexibleServerDatabase](Get-AzMySqlFlexibleServerDatabase.md)
取得資料庫的相關資訊。

### [AzMySqlFlexibleServerFirewallRule](Get-AzMySqlFlexibleServerFirewallRule.md)
取得伺服器防火牆規則的相關資訊。

### [AzMySqlFlexibleServerLocationBasedCapability](Get-AzMySqlFlexibleServerLocationBasedCapability.md)
取得該位置的可用 SKU 資訊

### [AzMySqlFlexibleServerReplica](Get-AzMySqlFlexibleServerReplica.md)
列出指定伺服器的所有複本。

### [AzMySqlReplica](Get-AzMySqlReplica.md)
列出指定伺服器的所有複本。

### [AzMySqlServer](Get-AzMySqlServer.md)
取得伺服器的相關資訊。

### [AzMySqlVirtualNetworkRule](Get-AzMySqlVirtualNetworkRule.md)
取得虛擬網路規則。

### [新-AzMySqlFirewallRule](New-AzMySqlFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [新-AzMySqlFlexibleServer](New-AzMySqlFlexibleServer.md)
建立新的 MySQL 靈活伺服器。

### [新-AzMySqlFlexibleServerDatabase](New-AzMySqlFlexibleServerDatabase.md)
建立新資料庫或更新現有的資料庫。

### [新-AzMySqlFlexibleServerFirewallRule](New-AzMySqlFlexibleServerFirewallRule.md)
建立適用于 MySQL 靈活伺服器的新防火牆規則

### [新-AzMySqlFlexibleServerReplica](New-AzMySqlFlexibleServerReplica.md)
從現有資料庫建立新的複本。

### [新-AzMySqlReplica](New-AzMySqlReplica.md)
從現有資料庫建立新的複本。

### [新-AzMySqlServer](New-AzMySqlServer.md)
建立新的伺服器。

### [新-AzMySqlVirtualNetworkRule](New-AzMySqlVirtualNetworkRule.md)
建立或更新現有的虛擬網路規則。

### [移除-AzMySqlFirewallRule](Remove-AzMySqlFirewallRule.md)
刪除伺服器防火牆規則。

### [移除-AzMySqlFlexibleServer](Remove-AzMySqlFlexibleServer.md)
刪除伺服器。

### [移除-AzMySqlFlexibleServerDatabase](Remove-AzMySqlFlexibleServerDatabase.md)
刪除資料庫。

### [移除-AzMySqlFlexibleServerFirewallRule](Remove-AzMySqlFlexibleServerFirewallRule.md)
刪除防火牆規則。

### [移除-AzMySqlServer](Remove-AzMySqlServer.md)
刪除伺服器。

### [移除-AzMySqlVirtualNetworkRule](Remove-AzMySqlVirtualNetworkRule.md)
刪除具有指定名稱的虛擬網路規則。

### [重新開機-AzMySqlFlexibleServer](Restart-AzMySqlFlexibleServer.md)
重新開機伺服器。

### [重新開機-AzMySqlServer](Restart-AzMySqlServer.md)
重新開機伺服器。

### [Restore-AzMySqlFlexibleServer](Restore-AzMySqlFlexibleServer.md)
從現有的備份還原伺服器

### [Restore-AzMySqlServer](Restore-AzMySqlServer.md)
從現有的備份還原伺服器

### [開始-AzMySqlFlexibleServer](Start-AzMySqlFlexibleServer.md)
啟動伺服器。

### [停止 AzMySqlFlexibleServer](Stop-AzMySqlFlexibleServer.md)
停止伺服器。

### [Test-AzMySqlFlexibleServerConnect](Test-AzMySqlFlexibleServerConnect.md)
測試資料庫伺服器的連線

### [更新-AzMySqlConfiguration](Update-AzMySqlConfiguration.md)
補救伺服器的設定。
如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzMySqlServer]。

### [更新-AzMySqlFirewallRule](Update-AzMySqlFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [更新-AzMySqlFlexibleServer](Update-AzMySqlFlexibleServer.md)
更新現有的 MySQL 靈活伺服器。
要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。
如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlFlexibleServerConfiguration。

### [更新-AzMySqlFlexibleServerConfiguration](Update-AzMySqlFlexibleServerConfiguration.md)
更新有關 MySQL 靈活伺服器設定的資訊。

### [更新-AzMySqlFlexibleServerDatabase](Update-AzMySqlFlexibleServerDatabase.md)
建立新資料庫或更新現有的資料庫。

### [更新-AzMySqlFlexibleServerFirewallRule](Update-AzMySqlFlexibleServerFirewallRule.md)
更新現有的防火牆規則。

### [更新-AzMySqlServer](Update-AzMySqlServer.md)
更新現有的伺服器。
要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。
如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzMySqlConfiguration。

### [更新-AzMySqlVirtualNetworkRule](Update-AzMySqlVirtualNetworkRule.md)
建立或更新現有的虛擬網路規則。

