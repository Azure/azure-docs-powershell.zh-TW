---
Module Name: Az.CostManagement
Module Guid: 4cd9af10-559e-4fb9-8dcd-d3e8eb9e03b7
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
ms.openlocfilehash: 0bfac4d12c15bef8b16e9ba239423b1443a9f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98445956"
---
# <span data-ttu-id="d507d-101">Az CostManagement 模組</span><span class="sxs-lookup"><span data-stu-id="d507d-101">Az.CostManagement Module</span></span>
## <span data-ttu-id="d507d-102">說明</span><span class="sxs-lookup"><span data-stu-id="d507d-102">Description</span></span>
<span data-ttu-id="d507d-103">Microsoft Azure PowerShell：成本 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d507d-103">Microsoft Azure PowerShell: Cost cmdlets</span></span>

## <span data-ttu-id="d507d-104">Az CostManagement Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d507d-104">Az.CostManagement Cmdlets</span></span>
### [<span data-ttu-id="d507d-105">AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d507d-105">Get-AzCostManagementExport</span></span>](Get-AzCostManagementExport.md)
<span data-ttu-id="d507d-106">此作業可透過匯出名稱取得已定義範圍的匯出。</span><span class="sxs-lookup"><span data-stu-id="d507d-106">The operation to get the export for the defined scope by export name.</span></span>

### [<span data-ttu-id="d507d-107">AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="d507d-107">Get-AzCostManagementExportExecutionHistory</span></span>](Get-AzCostManagementExportExecutionHistory.md)
<span data-ttu-id="d507d-108">此作業可取得已定義範圍及匯出名稱之匯出的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d507d-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

### [<span data-ttu-id="d507d-109">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="d507d-109">Invoke-AzCostManagementExecuteExport</span></span>](Invoke-AzCostManagementExecuteExport.md)
<span data-ttu-id="d507d-110">執行匯出作業的操作。</span><span class="sxs-lookup"><span data-stu-id="d507d-110">The operation to execute an export.</span></span>

### [<span data-ttu-id="d507d-111">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="d507d-111">Invoke-AzCostManagementQuery</span></span>](Invoke-AzCostManagementQuery.md)
<span data-ttu-id="d507d-112">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="d507d-112">Query the usage data for scope defined.</span></span>

### [<span data-ttu-id="d507d-113">新-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d507d-113">New-AzCostManagementExport</span></span>](New-AzCostManagementExport.md)
<span data-ttu-id="d507d-114">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="d507d-114">The operation to create or update a export.</span></span>
<span data-ttu-id="d507d-115">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-115">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d507d-116">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-116">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d507d-117">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-117">Create operation does not require eTag.</span></span>

### [<span data-ttu-id="d507d-118">新-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="d507d-118">New-AzCostManagementQueryComparisonExpressionObject</span></span>](New-AzCostManagementQueryComparisonExpressionObject.md)
<span data-ttu-id="d507d-119">為 QueryComparisonExpression 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="d507d-119">Create a in-memory object for QueryComparisonExpression</span></span>

### [<span data-ttu-id="d507d-120">新-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="d507d-120">New-AzCostManagementQueryFilterObject</span></span>](New-AzCostManagementQueryFilterObject.md)
<span data-ttu-id="d507d-121">為 QueryFilter 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="d507d-121">Create a in-memory object for QueryFilter</span></span>

### [<span data-ttu-id="d507d-122">移除-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d507d-122">Remove-AzCostManagementExport</span></span>](Remove-AzCostManagementExport.md)
<span data-ttu-id="d507d-123">刪除匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="d507d-123">The operation to delete a export.</span></span>

### [<span data-ttu-id="d507d-124">更新-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d507d-124">Update-AzCostManagementExport</span></span>](Update-AzCostManagementExport.md)
<span data-ttu-id="d507d-125">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="d507d-125">The operation to create or update a export.</span></span>
<span data-ttu-id="d507d-126">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-126">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d507d-127">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-127">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d507d-128">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="d507d-128">Create operation does not require eTag.</span></span>

