---
Module Name: Az.CostManagement
Module Guid: 4cd9af10-559e-4fb9-8dcd-d3e8eb9e03b7
Download Help Link: https://docs.microsoft.com/powershell/module/az.costmanagement
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
ms.openlocfilehash: 540fe573ae08cc1ee740979df1e3a5f8eaa45d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913573"
---
# <span data-ttu-id="57815-101">Az.CostManagement 模組</span><span class="sxs-lookup"><span data-stu-id="57815-101">Az.CostManagement Module</span></span>
## <span data-ttu-id="57815-102">描述</span><span class="sxs-lookup"><span data-stu-id="57815-102">Description</span></span>
<span data-ttu-id="57815-103">Microsoft Azure PowerShell：成本 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57815-103">Microsoft Azure PowerShell: Cost cmdlets</span></span>

## <span data-ttu-id="57815-104">Az.CostManagement Cmdlets</span><span class="sxs-lookup"><span data-stu-id="57815-104">Az.CostManagement Cmdlets</span></span>
### [<span data-ttu-id="57815-105">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="57815-105">Get-AzCostManagementExport</span></span>](Get-AzCostManagementExport.md)
<span data-ttu-id="57815-106">以匯出名稱取得已定義範圍匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="57815-106">The operation to get the export for the defined scope by export name.</span></span>

### [<span data-ttu-id="57815-107">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="57815-107">Get-AzCostManagementExportExecutionHistory</span></span>](Get-AzCostManagementExportExecutionHistory.md)
<span data-ttu-id="57815-108">取得已定義範圍和匯出名稱之匯出執行歷程記錄的操作。</span><span class="sxs-lookup"><span data-stu-id="57815-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

### [<span data-ttu-id="57815-109">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="57815-109">Invoke-AzCostManagementExecuteExport</span></span>](Invoke-AzCostManagementExecuteExport.md)
<span data-ttu-id="57815-110">執行匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="57815-110">The operation to execute an export.</span></span>

### [<span data-ttu-id="57815-111">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="57815-111">Invoke-AzCostManagementQuery</span></span>](Invoke-AzCostManagementQuery.md)
<span data-ttu-id="57815-112">查詢已定義範圍的使用資料。</span><span class="sxs-lookup"><span data-stu-id="57815-112">Query the usage data for scope defined.</span></span>

### [<span data-ttu-id="57815-113">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="57815-113">New-AzCostManagementExport</span></span>](New-AzCostManagementExport.md)
<span data-ttu-id="57815-114">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="57815-114">The operation to create or update a export.</span></span>
<span data-ttu-id="57815-115">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-115">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="57815-116">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-116">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="57815-117">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-117">Create operation does not require eTag.</span></span>

### [<span data-ttu-id="57815-118">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="57815-118">New-AzCostManagementQueryComparisonExpressionObject</span></span>](New-AzCostManagementQueryComparisonExpressionObject.md)
<span data-ttu-id="57815-119">為 QueryComparisonExpression 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="57815-119">Create a in-memory object for QueryComparisonExpression</span></span>

### [<span data-ttu-id="57815-120">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="57815-120">New-AzCostManagementQueryFilterObject</span></span>](New-AzCostManagementQueryFilterObject.md)
<span data-ttu-id="57815-121">為 QueryFilter 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="57815-121">Create a in-memory object for QueryFilter</span></span>

### [<span data-ttu-id="57815-122">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="57815-122">Remove-AzCostManagementExport</span></span>](Remove-AzCostManagementExport.md)
<span data-ttu-id="57815-123">刪除匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="57815-123">The operation to delete a export.</span></span>

### [<span data-ttu-id="57815-124">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="57815-124">Update-AzCostManagementExport</span></span>](Update-AzCostManagementExport.md)
<span data-ttu-id="57815-125">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="57815-125">The operation to create or update a export.</span></span>
<span data-ttu-id="57815-126">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-126">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="57815-127">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-127">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="57815-128">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="57815-128">Create operation does not require eTag.</span></span>

