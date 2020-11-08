---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965648"
---
# <span data-ttu-id="cd2f6-101">Az ManagedServices 模組</span><span class="sxs-lookup"><span data-stu-id="cd2f6-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="cd2f6-102">說明</span><span class="sxs-lookup"><span data-stu-id="cd2f6-102">Description</span></span>
<span data-ttu-id="cd2f6-103">受管理服務提供者的客戶會使用這項功能 (MSPs) 。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="cd2f6-104">客戶可為 MSP 提供管理訂閱的功能。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="cd2f6-105">除了授予存取權之外，客戶也可以移除存取權或查看現有的存取委派。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="cd2f6-106">MSPs 可以查看已授與訂閱存取權的客戶清單。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="cd2f6-107">這個處理常式中有兩個物件：註冊定義，可識別 msp 以及授與的角色定義。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="cd2f6-108">MSP 可以選擇使用受管理的服務 marketplace 來定義此物件，以提供存取作業，將訂閱與定義產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="cd2f6-109">Az ManagedServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd2f6-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="cd2f6-110">AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="cd2f6-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="cd2f6-111">取得註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="cd2f6-112">AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2f6-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="cd2f6-113">取得註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="cd2f6-114">新-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="cd2f6-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="cd2f6-115">建立註冊作業。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="cd2f6-116">新-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2f6-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="cd2f6-117">建立註冊定義。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="cd2f6-118">移除-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="cd2f6-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="cd2f6-119">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="cd2f6-120">移除-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2f6-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="cd2f6-121">刪除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="cd2f6-121">Deletes the registration definition.</span></span>
