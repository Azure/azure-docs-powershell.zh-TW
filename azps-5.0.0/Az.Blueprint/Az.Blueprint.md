---
Module Name: Az.Blueprint
Module Guid: ef36c942-4a71-4e19-9450-05a35843deb6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.blueprint
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
ms.openlocfilehash: 1722032406a81253ebf580f79172be85aa23c55f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138363"
---
# <span data-ttu-id="a4245-101">Az. 藍圖模組</span><span class="sxs-lookup"><span data-stu-id="a4245-101">Az.Blueprint Module</span></span>
## <span data-ttu-id="a4245-102">說明</span><span class="sxs-lookup"><span data-stu-id="a4245-102">Description</span></span>
<span data-ttu-id="a4245-103">本節中的主題會在 Azure 資源管理器架構中記錄 Azure 藍圖的 Azure PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4245-103">The topics in this section document the Azure PowerShell cmdlets for Azure Blueprints in the Azure Resource Manager framework.</span></span> <span data-ttu-id="a4245-104">Cmdlet 存在於 Microsoft. PowerShell 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a4245-104">The cmdlets exist in the Microsoft.Azure.PowerShell.Cmdlets.Blueprint namespace.</span></span>

## <span data-ttu-id="a4245-105">Az. 藍圖 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4245-105">Az.Blueprint Cmdlets</span></span>
### [<span data-ttu-id="a4245-106">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a4245-106">Export-AzBlueprintWithArtifact</span></span>](Export-AzBlueprintWithArtifact.md)
<span data-ttu-id="a4245-107">將指定的藍圖定義匯出到指定的輸出位置做為 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="a4245-107">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

### [<span data-ttu-id="a4245-108">AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4245-108">Get-AzBlueprint</span></span>](Get-AzBlueprint.md)
<span data-ttu-id="a4245-109">取得一或多個藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="a4245-109">Get one or more blueprint definitions.</span></span>

### [<span data-ttu-id="a4245-110">AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a4245-110">Get-AzBlueprintArtifact</span></span>](Get-AzBlueprintArtifact.md)
<span data-ttu-id="a4245-111">從藍圖定義中取得專案。</span><span class="sxs-lookup"><span data-stu-id="a4245-111">Retrieve artifacts from a blueprint definition.</span></span>

### [<span data-ttu-id="a4245-112">AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a4245-112">Get-AzBlueprintAssignment</span></span>](Get-AzBlueprintAssignment.md)
<span data-ttu-id="a4245-113">取得一或多個藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="a4245-113">Get one or more blueprint assignments.</span></span>

### [<span data-ttu-id="a4245-114">匯入-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a4245-114">Import-AzBlueprintWithArtifact</span></span>](Import-AzBlueprintWithArtifact.md)
<span data-ttu-id="a4245-115">將 JSON 格式的藍圖檔案匯入至藍圖物件，然後將它儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="a4245-115">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="a4245-116">新-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4245-116">New-AzBlueprint</span></span>](New-AzBlueprint.md)
<span data-ttu-id="a4245-117">建立新的藍圖定義，並將它儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="a4245-117">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="a4245-118">新-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a4245-118">New-AzBlueprintArtifact</span></span>](New-AzBlueprintArtifact.md)
<span data-ttu-id="a4245-119">建立新的專案，並將它儲存在藍圖定義中。</span><span class="sxs-lookup"><span data-stu-id="a4245-119">Create a new artifact and save it within a blueprint definition.</span></span>

### [<span data-ttu-id="a4245-120">新-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a4245-120">New-AzBlueprintAssignment</span></span>](New-AzBlueprintAssignment.md)
<span data-ttu-id="a4245-121">將藍圖定義指派給訂閱或管理群組。</span><span class="sxs-lookup"><span data-stu-id="a4245-121">Assign a blueprint definition to a subscription or a management group.</span></span>

### [<span data-ttu-id="a4245-122">發佈-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4245-122">Publish-AzBlueprint</span></span>](Publish-AzBlueprint.md)
<span data-ttu-id="a4245-123">發佈新版本的藍圖。</span><span class="sxs-lookup"><span data-stu-id="a4245-123">Publish a new version of a blueprint.</span></span>

### [<span data-ttu-id="a4245-124">移除-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a4245-124">Remove-AzBlueprintAssignment</span></span>](Remove-AzBlueprintAssignment.md)
<span data-ttu-id="a4245-125">從訂閱或管理群組中移除藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="a4245-125">Remove a blueprint assignment from a subscription or a management group.</span></span>

### [<span data-ttu-id="a4245-126">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4245-126">Set-AzBlueprint</span></span>](Set-AzBlueprint.md)
<span data-ttu-id="a4245-127">更新藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="a4245-127">Update a blueprint definition.</span></span>

### [<span data-ttu-id="a4245-128">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a4245-128">Set-AzBlueprintArtifact</span></span>](Set-AzBlueprintArtifact.md)
<span data-ttu-id="a4245-129">更新藍圖定義中的專案。</span><span class="sxs-lookup"><span data-stu-id="a4245-129">Update an artifact in a blueprint definition.</span></span>

### [<span data-ttu-id="a4245-130">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a4245-130">Set-AzBlueprintAssignment</span></span>](Set-AzBlueprintAssignment.md)
<span data-ttu-id="a4245-131">更新現有的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="a4245-131">Update an existing blueprint assignment.</span></span>
