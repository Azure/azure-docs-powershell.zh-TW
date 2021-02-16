---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132762"
---
# <span data-ttu-id="843c7-101">Az ManagedServices 模組</span><span class="sxs-lookup"><span data-stu-id="843c7-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="843c7-102">說明</span><span class="sxs-lookup"><span data-stu-id="843c7-102">Description</span></span>
<span data-ttu-id="843c7-103">受管理服務提供者的客戶會使用這項功能 (MSPs) 。</span><span class="sxs-lookup"><span data-stu-id="843c7-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="843c7-104">客戶可為 MSP 提供管理訂閱或資源群組的功能。</span><span class="sxs-lookup"><span data-stu-id="843c7-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="843c7-105">除了授予存取權之外，客戶也可以移除存取權或查看現有的存取權。</span><span class="sxs-lookup"><span data-stu-id="843c7-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="843c7-106">MSPs 可以查看已授與訂閱存取權的客戶清單。</span><span class="sxs-lookup"><span data-stu-id="843c7-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="843c7-107">這個程式中有兩個物件：註冊定義，可識別 msp 以及授與 MSP 使用者的角色定義。</span><span class="sxs-lookup"><span data-stu-id="843c7-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="843c7-108">MSP 可以選擇使用受管理的服務 marketplace 來定義此物件，以提供存取作業，將訂閱與定義產生關聯。</span><span class="sxs-lookup"><span data-stu-id="843c7-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="843c7-109">Az ManagedServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="843c7-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="843c7-110">AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="843c7-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="843c7-111">取得特定的註冊指派或註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="843c7-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="843c7-112">AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="843c7-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="843c7-113">取得特定的註冊定義或註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="843c7-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="843c7-114">新-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="843c7-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="843c7-115">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="843c7-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="843c7-116">新-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="843c7-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="843c7-117">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="843c7-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="843c7-118">移除-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="843c7-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="843c7-119">移除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="843c7-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="843c7-120">移除-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="843c7-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="843c7-121">移除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="843c7-121">Removes a registration definition.</span></span>
