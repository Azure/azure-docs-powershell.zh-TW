---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: bbbdd28f0ea3916581c20cf8f078eca1cb2ddca6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441935"
---
# <span data-ttu-id="8b7dc-101">AzureRM MarketplaceOrdering Module</span><span class="sxs-lookup"><span data-stu-id="8b7dc-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="8b7dc-102">說明</span><span class="sxs-lookup"><span data-stu-id="8b7dc-102">Description</span></span>
<span data-ttu-id="8b7dc-103">本節中的主題會將 azure 資源管理器中的 azure PowerShell Cmdlet MarketplaceOrdering 到 Azure 資源管理員 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="8b7dc-104">MarketplaceOrdering 命名空間中存在 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="8b7dc-105">這些 Cmdlet 可讓 azure 使用者接受 marketplace 的法律條款，進一步允許以程式設計方式部署這些方案。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="8b7dc-106">使用者也可以拒絕已接受的一組法律詞彙。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="8b7dc-107">AzureRM MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8b7dc-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="8b7dc-108">AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8b7dc-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="8b7dc-109">取得指定發行商識別碼 (Publisher) 的合約條款，提供識別碼 (產品) 與方案 id (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8b7dc-110">此命令所傳回的 [詞彙] 物件應該傳遞給 Set-AzureRmMarketplaceTerms，以接受法律條款。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="8b7dc-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8b7dc-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="8b7dc-112">接受或拒絕指定發行者識別碼 (Publisher) 中的條款，提供識別碼 (產品) 與計畫識別碼 (名稱) 。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8b7dc-113">請使用 Get-AzureRmMarketplaceTerms 取得合約條款。</span><span class="sxs-lookup"><span data-stu-id="8b7dc-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

