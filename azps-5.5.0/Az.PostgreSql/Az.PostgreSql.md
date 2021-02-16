---
Module Name: Az.PostgreSql
Module Guid: b09b1b72-75a0-43a4-a342-b69a27eb64b5
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.postgresql
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Az.PostgreSql.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Az.PostgreSql.md
ms.openlocfilehash: 21012a2cb8048c144935271c6bb8fde6673dd1ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132335"
---
# Az PostgreSql 模組
## 說明
Microsoft Azure PowerShell： PostgreSql Cmdlet

## Az PostgreSql Cmdlet
### [AzPostgreSqlConfiguration](Get-AzPostgreSqlConfiguration.md)
取得伺服器設定的相關資訊。

### [AzPostgreSqlConnectionString](Get-AzPostgreSqlConnectionString.md)
根據用戶端連線提供者取得連接字串。

### [AzPostgreSqlFirewallRule](Get-AzPostgreSqlFirewallRule.md)
取得伺服器防火牆規則的相關資訊。

### [AzPostgreSqlFlexibleServer](Get-AzPostgreSqlFlexibleServer.md)
取得伺服器的相關資訊。

### [AzPostgreSqlFlexibleServerConfiguration](Get-AzPostgreSqlFlexibleServerConfiguration.md)
取得伺服器設定的相關資訊。

### [AzPostgreSqlFlexibleServerConnectionString](Get-AzPostgreSqlFlexibleServerConnectionString.md)
根據用戶端連線提供者取得連接字串。

### [AzPostgreSqlFlexibleServerFirewallRule](Get-AzPostgreSqlFlexibleServerFirewallRule.md)
列出指定伺服器中的所有防火牆規則。

### [AzPostgreSqlFlexibleServerLocationBasedCapability](Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md)
取得該位置的可用 SKU 資訊

### [AzPostgreSqlReplica](Get-AzPostgreSqlReplica.md)
列出指定伺服器的所有複本。

### [AzPostgreSqlServer](Get-AzPostgreSqlServer.md)
取得伺服器的相關資訊。

### [AzPostgreSqlVirtualNetworkRule](Get-AzPostgreSqlVirtualNetworkRule.md)
取得虛擬網路規則。

### [新-AzPostgreSqlFirewallRule](New-AzPostgreSqlFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [新-AzPostgreSqlFlexibleServer](New-AzPostgreSqlFlexibleServer.md)
建立新的伺服器。

### [新-AzPostgreSqlFlexibleServerFirewallRule](New-AzPostgreSqlFlexibleServerFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [新-AzPostgreSqlReplica](New-AzPostgreSqlReplica.md)
從現有資料庫建立新的複本。

### [新-AzPostgreSqlServer](New-AzPostgreSqlServer.md)
建立新的伺服器。

### [新-AzPostgreSqlVirtualNetworkRule](New-AzPostgreSqlVirtualNetworkRule.md)
建立或更新現有的虛擬網路規則。

### [移除-AzPostgreSqlFirewallRule](Remove-AzPostgreSqlFirewallRule.md)
刪除伺服器防火牆規則。

### [移除-AzPostgreSqlFlexibleServer](Remove-AzPostgreSqlFlexibleServer.md)
刪除伺服器。

### [移除-AzPostgreSqlFlexibleServerFirewallRule](Remove-AzPostgreSqlFlexibleServerFirewallRule.md)
刪除 PostgreSQL 伺服器防火牆規則。

### [移除-AzPostgreSqlServer](Remove-AzPostgreSqlServer.md)
刪除伺服器。

### [移除-AzPostgreSqlVirtualNetworkRule](Remove-AzPostgreSqlVirtualNetworkRule.md)
刪除具有指定名稱的虛擬網路規則。

### [重新開機-AzPostgreSqlFlexibleServer](Restart-AzPostgreSqlFlexibleServer.md)
重新開機伺服器。

### [重新開機-AzPostgreSqlServer](Restart-AzPostgreSqlServer.md)
重新開機伺服器。

### [Restore-AzPostgreSqlFlexibleServer](Restore-AzPostgreSqlFlexibleServer.md)
從現有的備份還原伺服器

### [Restore-AzPostgreSqlServer](Restore-AzPostgreSqlServer.md)
從現有的備份還原伺服器

### [開始-AzPostgreSqlFlexibleServer](Start-AzPostgreSqlFlexibleServer.md)
啟動伺服器。

### [停止 AzPostgreSqlFlexibleServer](Stop-AzPostgreSqlFlexibleServer.md)
停止伺服器。

### [Test-AzPostgreSqlFlexibleServerConnect](Test-AzPostgreSqlFlexibleServerConnect.md)
測試資料庫伺服器的連線

### [更新-AzPostgreSqlConfiguration](Update-AzPostgreSqlConfiguration.md)
補救伺服器的設定。
如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlServer]。

### [更新-AzPostgreSqlFirewallRule](Update-AzPostgreSqlFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [更新-AzPostgreSqlFlexibleServer](Update-AzPostgreSqlFlexibleServer.md)
更新現有的伺服器。
要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。
如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostgreSqlFlexibleServerConfiguration。

### [更新-AzPostgreSqlFlexibleServerConfiguration](Update-AzPostgreSqlFlexibleServerConfiguration.md)
補救伺服器的設定。
如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlFlexibleServer]。

### [更新-AzPostgreSqlFlexibleServerFirewallRule](Update-AzPostgreSqlFlexibleServerFirewallRule.md)
建立新的防火牆規則或更新現有的防火牆規則。

### [更新-AzPostgreSqlServer](Update-AzPostgreSqlServer.md)
更新現有的伺服器。
要求主體可以包含一個到在一般伺服器定義中存在的許多屬性。
如果您想要補救伺服器參數（例如 wait_timeout 或 net_retry_count），請改用 Update-AzPostSqlConfiguration。

### [更新-AzPostgreSqlVirtualNetworkRule](Update-AzPostgreSqlVirtualNetworkRule.md)
建立或更新現有的虛擬網路規則。

