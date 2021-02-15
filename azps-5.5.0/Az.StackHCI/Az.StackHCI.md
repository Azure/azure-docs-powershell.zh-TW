---
Module Name: Az.StackHCI
Module Guid: 8ff047e4-15bb-4b53-a728-75641c49958b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.StackHCI
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
ms.openlocfilehash: 5666172da80ec27131931aecc353c9315266b185
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127350"
---
# <span data-ttu-id="66578-101">Az StackHCI 模組</span><span class="sxs-lookup"><span data-stu-id="66578-101">Az.StackHCI Module</span></span>
## <span data-ttu-id="66578-102">說明</span><span class="sxs-lookup"><span data-stu-id="66578-102">Description</span></span>
<span data-ttu-id="66578-103">Microsoft Azure PowerShell： Azure 堆疊 HCI 註冊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66578-103">Microsoft Azure PowerShell: Azure Stack HCI registration cmdlets</span></span>

## <span data-ttu-id="66578-104">Az StackHCI Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66578-104">Az.StackHCI Cmdlets</span></span>
### [<span data-ttu-id="66578-105">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="66578-105">Register-AzStackHCI</span></span>](Register-AzStackHCI.md)
<span data-ttu-id="66578-106">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="66578-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

### [<span data-ttu-id="66578-107">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="66578-107">Test-AzStackHCIConnection</span></span>](Test-AzStackHCIConnection.md)
<span data-ttu-id="66578-108">Test-AzStackHCIConnection 驗證來自內部部署叢集節點的連線至 Azure 堆疊 HCI 所需的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="66578-108">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

### [<span data-ttu-id="66578-109">取消註冊-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="66578-109">Unregister-AzStackHCI</span></span>](Unregister-AzStackHCI.md)
<span data-ttu-id="66578-110">Unregister-AzStackHCI 刪除代表內部部署群集的 AzureStackHCI 雲端資源，並以 Azure 登出內部部署群集。</span><span class="sxs-lookup"><span data-stu-id="66578-110">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="66578-111">如果未傳遞任何參數，則會使用在群集上註冊的資訊來登出群集。</span><span class="sxs-lookup"><span data-stu-id="66578-111">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

