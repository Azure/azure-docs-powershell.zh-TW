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
# <span data-ttu-id="c4b2a-101">Az.MarketplaceOrdering 模組</span><span class="sxs-lookup"><span data-stu-id="c4b2a-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="c4b2a-102">描述</span><span class="sxs-lookup"><span data-stu-id="c4b2a-102">Description</span></span>
<span data-ttu-id="c4b2a-103">本節主題將說明 Azure Resource Manager 中 Azure MarketplaceOrdering 的 Azure PowerShell Cmdlet (ARM) 架構。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c4b2a-104">Cmdlet 存在於 Microsoft.Azure.Commands.MarketplaceOrdering 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="c4b2a-105">這些 Cmdlet 允許 Azure 使用者接受提供進一步允許這些解決方案之程式設計部署之服務商場的法律條款。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="c4b2a-106">使用者也可以拒絕一組已接受的法律條款。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="c4b2a-107">Az.MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4b2a-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="c4b2a-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="c4b2a-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="c4b2a-109">取得 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="c4b2a-110">此命令所傳回的字詞物件應傳遞至Set-AzMarketplaceTerms接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="c4b2a-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="c4b2a-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="c4b2a-112">接受或拒絕 Publisher (發行者識別碼) 、提供識別碼 (產品) 以及方案 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="c4b2a-113">請使用Get-AzMarketplaceTerms以取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="c4b2a-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

