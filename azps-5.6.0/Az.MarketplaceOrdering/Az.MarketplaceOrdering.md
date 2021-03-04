---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911926"
---
# Az.MarketplaceOrdering 模組
## 描述
本節主題將說明 Azure Resource Manager 中 Azure MarketplaceOrdering 的 Azure PowerShell Cmdlet (ARM) 架構。 Cmdlet 存在於 Microsoft.Azure.Commands.MarketplaceOrdering 命名空間中。 這些 Cmdlet 允許 Azure 使用者接受提供進一步允許這些解決方案之程式設計部署之服務商場的法律條款。 使用者也可以拒絕一組已接受的法律條款。

## Az.MarketplaceOrdering Cmdlet
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
取得 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。 此命令所傳回的字詞物件應傳遞至Set-AzMarketplaceTerms接受法律條款。

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
接受或拒絕 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。 請使用Get-AzMarketplaceTerms以取得合約條款。

