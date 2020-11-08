---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139416"
---
# <span data-ttu-id="8ddf6-101">Az. 支援模組</span><span class="sxs-lookup"><span data-stu-id="8ddf6-101">Az.Support Module</span></span>
## <span data-ttu-id="8ddf6-102">說明</span><span class="sxs-lookup"><span data-stu-id="8ddf6-102">Description</span></span>
<span data-ttu-id="8ddf6-103">本節主題所述的 Azure PowerShell Cmdlet 可在 Azure 資源管理器 (ARM) 架構中建立和管理 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="8ddf6-104">Cmdlet 存在於 Microsoft. 命令中。支援命名空間</span><span class="sxs-lookup"><span data-stu-id="8ddf6-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="8ddf6-105">Az. 支援 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ddf6-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="8ddf6-106">AzSupportService</span><span class="sxs-lookup"><span data-stu-id="8ddf6-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="8ddf6-107">取得目前提供支援的 Azure 服務清單。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="8ddf6-108">每個 Azure 服務都有自己的一組類別，稱為「問題分類」。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="8ddf6-109">使用 AzSupportProblemClassification，以取得服務的目前問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="8ddf6-110">您可以使用 [服務] 和 [問題分類 GUID]，使用新的 AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="8ddf6-111">AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="8ddf6-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="8ddf6-112">取得 Azure 服務的目前問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="8ddf6-113">您可以使用 [服務] 和 [問題分類 GUID]，使用新的 AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="8ddf6-114">新-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="8ddf6-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="8ddf6-115">協助程式 Cmdlet 建立支援連絡人設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="8ddf6-116">您可以將此物件用於 New-AzSupportTicket Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="8ddf6-117">新-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ddf6-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="8ddf6-118">建立新的 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="8ddf6-119">這個作業會根據 Azure [新支援要求頁面](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)的行為進行模型。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="8ddf6-120">AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ddf6-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="8ddf6-121">取得支援票證的清單。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-121">Gets the list of support tickets.</span></span> <span data-ttu-id="8ddf6-122">您可以依票證名稱取得完整的支援票證詳細資料，或依 *狀態* 或 *CreatedDate* 篩選支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="8ddf6-123">更新-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ddf6-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="8ddf6-124">更新支援票證的嚴重性、狀態或客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="8ddf6-125">AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8ddf6-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="8ddf6-126">取得支援票證的通訊。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="8ddf6-127">您也可以使用 *CreatedDate* 或 *CommunicationType* 來篩選支援票證通訊。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="8ddf6-128">新-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8ddf6-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="8ddf6-129">將新的客戶通訊新增至 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="8ddf6-129">Adds a new customer communication to an Azure support ticket.</span></span> 



