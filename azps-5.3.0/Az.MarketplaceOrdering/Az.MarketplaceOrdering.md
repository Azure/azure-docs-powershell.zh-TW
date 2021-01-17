---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438016"
---
# <span data-ttu-id="6b283-101">Az MarketplaceOrdering 模組</span><span class="sxs-lookup"><span data-stu-id="6b283-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="6b283-102">說明</span><span class="sxs-lookup"><span data-stu-id="6b283-102">Description</span></span>
<span data-ttu-id="6b283-103">本節中的主題會將 azure 資源管理器中的 azure PowerShell Cmdlet MarketplaceOrdering 到 Azure 資源管理員 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="6b283-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="6b283-104">MarketplaceOrdering 命名空間中存在 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b283-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="6b283-105">這些 Cmdlet 可讓 azure 使用者接受 marketplace 的法律條款，進一步允許以程式設計方式部署這些方案。</span><span class="sxs-lookup"><span data-stu-id="6b283-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="6b283-106">使用者也可以拒絕已接受的一組法律詞彙。</span><span class="sxs-lookup"><span data-stu-id="6b283-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="6b283-107">Az MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b283-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="6b283-108">AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="6b283-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="6b283-109">取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="6b283-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="6b283-110">此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzMarketplaceTerms，以接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="6b283-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="6b283-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="6b283-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="6b283-112">接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="6b283-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="6b283-113">請使用 Get-AzMarketplaceTerms 取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="6b283-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

