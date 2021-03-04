---
Module Name: Az.StackHCI
Module Guid: 8ff047e4-15bb-4b53-a728-75641c49958b
Download Help Link: https://docs.microsoft.com/powershell/module/az.StackHCI
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Az.StackHCI.md
ms.openlocfilehash: a047ba7417390d6cd90bd9c9363eb76616f9d2aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913013"
---
# <span data-ttu-id="4ad81-101">Az.StackHCI 模組</span><span class="sxs-lookup"><span data-stu-id="4ad81-101">Az.StackHCI Module</span></span>
## <span data-ttu-id="4ad81-102">描述</span><span class="sxs-lookup"><span data-stu-id="4ad81-102">Description</span></span>
<span data-ttu-id="4ad81-103">Microsoft Azure PowerShell：Azure Stack HCI 註冊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4ad81-103">Microsoft Azure PowerShell: Azure Stack HCI registration cmdlets</span></span>

## <span data-ttu-id="4ad81-104">Az.StackHCI Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4ad81-104">Az.StackHCI Cmdlets</span></span>
### [<span data-ttu-id="4ad81-105">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="4ad81-105">Register-AzStackHCI</span></span>](Register-AzStackHCI.md)
<span data-ttu-id="4ad81-106">Register-AzStackHCI建立代表內部部署組群的 Microsoft.AzureStackHCI 雲端資源，然後向 Azure 登錄內部部署組。</span><span class="sxs-lookup"><span data-stu-id="4ad81-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

### [<span data-ttu-id="4ad81-107">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="4ad81-107">Test-AzStackHCIConnection</span></span>](Test-AzStackHCIConnection.md)
<span data-ttu-id="4ad81-108">Test-AzStackHCIConnection驗證從內部部署組群節點到 Azure Stack HCI 所需 Azure 服務的連接。</span><span class="sxs-lookup"><span data-stu-id="4ad81-108">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

### [<span data-ttu-id="4ad81-109">取消註冊-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="4ad81-109">Unregister-AzStackHCI</span></span>](Unregister-AzStackHCI.md)
<span data-ttu-id="4ad81-110">Unregister-AzStackHCI Microsoft.AzureStackHCI 雲端資源代表內部部署組，並取消註冊 Azure 內部部署組。</span><span class="sxs-lookup"><span data-stu-id="4ad81-110">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="4ad81-111">如果未傳遞任何參數，該組組上可用的登錄資訊會用來取消註冊該組。</span><span class="sxs-lookup"><span data-stu-id="4ad81-111">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

