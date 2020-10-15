---
title: 使用 Invoke-AzRestMethod 管理 Azure 資源
description: 如何使用 Azure PowerShell 透過 Invoke-AzRestMethod Cmdlet 來管理資源。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001707"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="72781-103">使用 Invoke-AzRestMethod 管理 Azure 資源</span><span class="sxs-lookup"><span data-stu-id="72781-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="72781-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) 是 Azure PowerShell Cmdlet，在 Az PowerShell 模組 4.4.0 版引進。</span><span class="sxs-lookup"><span data-stu-id="72781-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="72781-105">其允許您使用 Az 內容對 Azure Resource Management (ARM) 端點提出自訂 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="72781-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="72781-106">當您想要針對 Az PowerShell 模組中尚未提供的功能來管理 Azure 服務時，此 Cmdlet 會很有用。</span><span class="sxs-lookup"><span data-stu-id="72781-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="72781-107">如何使用 Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="72781-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="72781-108">舉例來說，您可以只允許存取特定網路的 Azure Container Registry (ACR)，或拒絕公用存取。</span><span class="sxs-lookup"><span data-stu-id="72781-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="72781-109">截至 Az PowerShell 模組 4.5.0 版，這項功能尚無法在 [Az.ContainerRegistry PowerShell 模組](/powershell/module/Az.ContainerRegistry/)中使用。</span><span class="sxs-lookup"><span data-stu-id="72781-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="72781-110">不過，此功能可以在過渡期中使用 `Invoke-AzRestMethod` 進行管理。</span><span class="sxs-lookup"><span data-stu-id="72781-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="72781-111">搭配 GET 作業使用 Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="72781-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="72781-112">下列範例示範如何搭配 GET 作業使用 `Invoke-AzRestMethod`：</span><span class="sxs-lookup"><span data-stu-id="72781-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="72781-113">為了允許有最大彈性，`Invoke-AzRestMethod` 的大部分參數都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="72781-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="72781-114">不過，當您管理資源群組中的資源時，很可能需要提供資源的完整識別碼，或像是資源群組、資源提供者和資源類型的參數。</span><span class="sxs-lookup"><span data-stu-id="72781-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="72781-115">當目標資源需要一個以上的名稱時，`ResourceType` 和 `Name` 參數可以接受多個值。</span><span class="sxs-lookup"><span data-stu-id="72781-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="72781-116">例如，若要在 Log Analytics 工作區中操作已儲存的搜尋，參數看起來會如下列範例所示：`-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`。</span><span class="sxs-lookup"><span data-stu-id="72781-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="72781-117">根據陣列中的位置使用對應，此 Cmdlet 會建構下列資源：`Id:'/workspaces/my-la/savedsearches/my-search'`。</span><span class="sxs-lookup"><span data-stu-id="72781-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="72781-118">`APIVersion` 參數可讓您使用特定的 API 版本，包括預覽版。</span><span class="sxs-lookup"><span data-stu-id="72781-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="72781-119">您可以在 [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub 存放庫中找到適用於 Azure 資源提供者的支援 API 版本。</span><span class="sxs-lookup"><span data-stu-id="72781-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="72781-120">您可以在下列位置中找到 2019-12-01-preview 版本 ACR 的定義：[azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview)。</span><span class="sxs-lookup"><span data-stu-id="72781-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="72781-121">搭配 PATCH 作業使用 Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="72781-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="72781-122">您可以使用 `Invoke-AzRestMethod` Cmdlet 在 `myresourcegroup` 資源群組中停用名為 `myacr` 的現有 ACR 公用存取。</span><span class="sxs-lookup"><span data-stu-id="72781-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="72781-123">若要停用公用網路存取，您需要對 API 進行 **PATCH** 呼叫，變更 `publicNetwokAccess` 參數的值，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="72781-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="72781-124">`Payload` 屬性是 JSON 字串，可顯示要修改屬性的路徑。</span><span class="sxs-lookup"><span data-stu-id="72781-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="72781-125">此 API 的所有參數都會在與此 API 相關聯的 **rest-api-spec** 檔案中加以說明。</span><span class="sxs-lookup"><span data-stu-id="72781-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="72781-126">您可以在 2019-12-01 預覽版本 API 的[容器登錄 JSON 檔案](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json)中找到 publicNetworkAccess 參數的定義。</span><span class="sxs-lookup"><span data-stu-id="72781-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="72781-127">若只要允許從特定 IP 位址存取登錄，則必須修改承載，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="72781-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="72781-128">與 Get-AzResource、New-AzResource 和 Remove-AzResource 的比較</span><span class="sxs-lookup"><span data-stu-id="72781-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="72781-129">`*-AzResource` Cmdlet 可讓您藉由指定資源類型、API 版本和要更新的屬性，自訂對 Azure 的 REST API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="72781-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="72781-130">不過，您必須先將屬性建立為 `PSObject`。</span><span class="sxs-lookup"><span data-stu-id="72781-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="72781-131">此程序會使複雜度提高一層，而且很容易就會變得複雜。</span><span class="sxs-lookup"><span data-stu-id="72781-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="72781-132">`Invoke-AzRestMethod` 提供簡單的 Azure 資源管理方式。</span><span class="sxs-lookup"><span data-stu-id="72781-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="72781-133">如先前範例所示，您可以建立 JSON 字串，並使用該字串來自訂 REST API 呼叫，而不需要預先建立任何 `PSObjects`。</span><span class="sxs-lookup"><span data-stu-id="72781-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="72781-134">如果已經熟悉 `*-AzResource` Cmdlet，則可以繼續使用。</span><span class="sxs-lookup"><span data-stu-id="72781-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="72781-135">我們不打算停止支援。</span><span class="sxs-lookup"><span data-stu-id="72781-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="72781-136">在 `Invoke-AzRestMethod` 中，我們已將新的 Cmdlet 新增至您的工具組。</span><span class="sxs-lookup"><span data-stu-id="72781-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="72781-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72781-137">See Also</span></span>

* [<span data-ttu-id="72781-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="72781-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="72781-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="72781-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="72781-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="72781-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
