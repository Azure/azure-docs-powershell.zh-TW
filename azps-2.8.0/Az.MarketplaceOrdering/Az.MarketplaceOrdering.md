---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "93611526"
---
# Az MarketplaceOrdering 模組
## 說明
本節中的主題會將 azure 資源管理器中的 azure PowerShell Cmdlet MarketplaceOrdering 到 Azure 資源管理員 (ARM) 架構中。 MarketplaceOrdering 命名空間中存在 Cmdlet。 這些 Cmdlet 可讓 azure 使用者接受 marketplace 的法律條款，進一步允許以程式設計方式部署這些方案。 使用者也可以拒絕已接受的一組法律詞彙。

## Az MarketplaceOrdering Cmdlet
### [AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。 此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzMarketplaceTerms，以接受法律條款。

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。 請使用 Get-AzMarketplaceTerms 取得合約條款。

