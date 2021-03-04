---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908701"
---
# <span data-ttu-id="70e75-101">Az.Support 模組</span><span class="sxs-lookup"><span data-stu-id="70e75-101">Az.Support Module</span></span>
## <span data-ttu-id="70e75-102">描述</span><span class="sxs-lookup"><span data-stu-id="70e75-102">Description</span></span>
<span data-ttu-id="70e75-103">本節主題將說明在 Azure Resource Manager (ARM) 中建立及管理 Azure 支援票證的 Azure PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70e75-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="70e75-104">Cmdlet 存在於 Microsoft.Azure.Commands.support 命名空間中</span><span class="sxs-lookup"><span data-stu-id="70e75-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="70e75-105">Az.Support Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70e75-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="70e75-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="70e75-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="70e75-107">獲得目前支援可用的 Azure 服務清單。</span><span class="sxs-lookup"><span data-stu-id="70e75-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="70e75-108">每個 Azure 服務都有自己的一組類別，稱為問題分類。</span><span class="sxs-lookup"><span data-stu-id="70e75-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="70e75-109">使用 Get-AzSupportProblemClassification 取得服務目前的問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="70e75-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="70e75-110">您可以使用服務和問題分類 GUID，使用 New-AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="70e75-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="70e75-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="70e75-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="70e75-112">獲得 Azure 服務目前的問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="70e75-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="70e75-113">您可以使用服務和問題分類 GUID，使用 New-AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="70e75-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="70e75-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="70e75-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="70e75-115">建立支援連絡人設定檔物件的協助程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70e75-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="70e75-116">您可以在 Cmdlet 中使用此New-AzSupportTicket物件。</span><span class="sxs-lookup"><span data-stu-id="70e75-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="70e75-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="70e75-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="70e75-118">建立新的 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="70e75-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="70e75-119">此作業以 Azure 新增支援要求頁面 [的行為為模型](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)。</span><span class="sxs-lookup"><span data-stu-id="70e75-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="70e75-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="70e75-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="70e75-121">獲得支援票證清單。</span><span class="sxs-lookup"><span data-stu-id="70e75-121">Gets the list of support tickets.</span></span> <span data-ttu-id="70e75-122">您可以根據票證名稱取得完整支援票證詳細資料，或根據狀態或 *CreatedDate 篩選支援票證*。</span><span class="sxs-lookup"><span data-stu-id="70e75-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="70e75-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="70e75-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="70e75-124">更新支援票證的嚴重性、狀態或客戶連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="70e75-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="70e75-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="70e75-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="70e75-126">獲得支援票證的通訊。</span><span class="sxs-lookup"><span data-stu-id="70e75-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="70e75-127">您也可以使用 *CreatedDate* 或 *CommunicationType 篩選支援票證通訊*。</span><span class="sxs-lookup"><span data-stu-id="70e75-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="70e75-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="70e75-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="70e75-129">新增客戶通訊至 Azure 支援票證。</span><span class="sxs-lookup"><span data-stu-id="70e75-129">Adds a new customer communication to an Azure support ticket.</span></span> 



