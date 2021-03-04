---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904649"
---
# <span data-ttu-id="40a22-101">Az.ManagedServices 模組</span><span class="sxs-lookup"><span data-stu-id="40a22-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="40a22-102">描述</span><span class="sxs-lookup"><span data-stu-id="40a22-102">Description</span></span>
<span data-ttu-id="40a22-103">受管理服務提供者的客戶 (MSP) 。</span><span class="sxs-lookup"><span data-stu-id="40a22-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="40a22-104">客戶提供 MSP 管理其訂閱或資源群組的能力。</span><span class="sxs-lookup"><span data-stu-id="40a22-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="40a22-105">除了授予存取權，客戶也可以移除存取權或查看現有的存取權。</span><span class="sxs-lookup"><span data-stu-id="40a22-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="40a22-106">MSP 可以查看已授予訂閱存取權的客戶清單。</span><span class="sxs-lookup"><span data-stu-id="40a22-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="40a22-107">此套裝程式含兩個物件：可識別 MSP 的註冊定義，以及授予 MSP 使用者的角色定義。</span><span class="sxs-lookup"><span data-stu-id="40a22-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="40a22-108">MSP 可以選擇性地使用提供 Access 指派的 Managed Services Marketplace 來定義此物件，這會將訂閱與定義關聯。</span><span class="sxs-lookup"><span data-stu-id="40a22-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="40a22-109">Az.ManagedServices Cmdlets</span><span class="sxs-lookup"><span data-stu-id="40a22-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="40a22-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="40a22-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="40a22-111">獲得特定的註冊作業或註冊作業清單。</span><span class="sxs-lookup"><span data-stu-id="40a22-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="40a22-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="40a22-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="40a22-113">獲得特定的註冊定義或註冊定義清單。</span><span class="sxs-lookup"><span data-stu-id="40a22-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="40a22-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="40a22-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="40a22-115">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="40a22-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="40a22-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="40a22-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="40a22-117">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="40a22-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="40a22-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="40a22-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="40a22-119">移除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="40a22-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="40a22-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="40a22-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="40a22-121">移除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="40a22-121">Removes a registration definition.</span></span>
