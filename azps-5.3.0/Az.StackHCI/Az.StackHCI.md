---
Module Name: Az.StackHCI
Module Guid: 8ff047e4-15bb-4b53-a728-75641c49958b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.StackHCI
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
ms.openlocfilehash: e11c0afba08bb7127551826427b5298e83245d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285516"
---
# <span data-ttu-id="bb59d-101">Az StackHCI 模組</span><span class="sxs-lookup"><span data-stu-id="bb59d-101">Az.StackHCI Module</span></span>
## <span data-ttu-id="bb59d-102">說明</span><span class="sxs-lookup"><span data-stu-id="bb59d-102">Description</span></span>
<span data-ttu-id="bb59d-103">Microsoft Azure PowerShell： StackHCI Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bb59d-103">Microsoft Azure PowerShell: StackHCI cmdlets</span></span>

## <span data-ttu-id="bb59d-104">Az StackHCI Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bb59d-104">Az.StackHCI Cmdlets</span></span>
### [<span data-ttu-id="bb59d-105">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="bb59d-105">Register-AzStackHCI</span></span>](Register-AzStackHCI.md)
<span data-ttu-id="bb59d-106">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="bb59d-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

### [<span data-ttu-id="bb59d-107">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="bb59d-107">Test-AzStackHCIConnection</span></span>](Test-AzStackHCIConnection.md)
<span data-ttu-id="bb59d-108">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="bb59d-108">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

### [<span data-ttu-id="bb59d-109">取消註冊-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="bb59d-109">Unregister-AzStackHCI</span></span>](Unregister-AzStackHCI.md)
<span data-ttu-id="bb59d-110">Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。</span><span class="sxs-lookup"><span data-stu-id="bb59d-110">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="bb59d-111">如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。</span><span class="sxs-lookup"><span data-stu-id="bb59d-111">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

