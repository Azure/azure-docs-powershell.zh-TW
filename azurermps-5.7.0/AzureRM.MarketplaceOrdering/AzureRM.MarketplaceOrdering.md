---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: 198de5436453caf633288e23f804085319a30f73
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442288"
---
# AzureRM MarketplaceOrdering Module
## 說明
本節中的主題會將 azure 資源管理器中的 azure PowerShell Cmdlet MarketplaceOrdering 到 Azure 資源管理員 (ARM) 架構中。 MarketplaceOrdering 命名空間中存在 Cmdlet。 這些 Cmdlet 可讓 azure 使用者接受 marketplace 的法律條款，進一步允許以程式設計方式部署這些方案。 使用者也可以拒絕已接受的一組法律詞彙。

## AzureRM MarketplaceOrdering Cmdlet
### [AzureRmMarketplaceTerms](Get-AzureRmMarketplaceTerms.md)
取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。 此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzureRmMarketplaceTerms，以接受法律條款。

### [Set-AzureRmMarketplaceTerms](Set-AzureRmMarketplaceTerms.md)
接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。 請使用 Get-AzureRmMarketplaceTerms 取得合約條款。

