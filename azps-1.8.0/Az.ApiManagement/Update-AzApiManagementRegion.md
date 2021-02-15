---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400700"
---
# <span data-ttu-id="25d61-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="25d61-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="25d61-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25d61-102">SYNOPSIS</span></span>
<span data-ttu-id="25d61-103">更新 PsApiManagement 實例中現有的部署區域。</span><span class="sxs-lookup"><span data-stu-id="25d61-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="25d61-104">語法</span><span class="sxs-lookup"><span data-stu-id="25d61-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25d61-105">描述</span><span class="sxs-lookup"><span data-stu-id="25d61-105">DESCRIPTION</span></span>
<span data-ttu-id="25d61-106">**Update-AzApiManagementRegion** Cmdlet 會更新 **Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementRegion** 中提供之類型 **Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement** 之額外 **Regions** 物件集合中的現有實例。</span><span class="sxs-lookup"><span data-stu-id="25d61-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="25d61-107">此 Cmdlet 不會部署任何專案，但會更新 **記憶體中的 PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="25d61-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="25d61-108">若要更新 API 管理部署，請使用修改過的 **PsApiManagementInstance** 至 Set-AzApiManagement Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25d61-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="25d61-109">例子</span><span class="sxs-lookup"><span data-stu-id="25d61-109">EXAMPLES</span></span>

### <span data-ttu-id="25d61-110">範例 1：增加 PsApiManagement 實例中額外區域的容量</span><span class="sxs-lookup"><span data-stu-id="25d61-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="25d61-111">此命令會獲得 API Management Premium SKU 服務，其區域位於美國中南部及美國中北部。</span><span class="sxs-lookup"><span data-stu-id="25d61-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="25d61-112">然後使用 **Update-AzApiManagementRegion** 將美國中北部地方的容量增加為 2。</span><span class="sxs-lookup"><span data-stu-id="25d61-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="25d61-113">下一個 Cmdlet Set-AzApiManagement將組配置變更適用于 Api 管理服務。</span><span class="sxs-lookup"><span data-stu-id="25d61-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="25d61-114">參數</span><span class="sxs-lookup"><span data-stu-id="25d61-114">PARAMETERS</span></span>

### <span data-ttu-id="25d61-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="25d61-115">-ApiManagement</span></span>
<span data-ttu-id="25d61-116">指定 **PsApiManagement 實例** ，以更新其中現有的部署區域。</span><span class="sxs-lookup"><span data-stu-id="25d61-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-117">-容量</span><span class="sxs-lookup"><span data-stu-id="25d61-117">-Capacity</span></span>
<span data-ttu-id="25d61-118">指定部署區域的新 SKU 容量值。</span><span class="sxs-lookup"><span data-stu-id="25d61-118">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d61-119">-DefaultProfile</span></span>
<span data-ttu-id="25d61-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25d61-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-121">-位置</span><span class="sxs-lookup"><span data-stu-id="25d61-121">-Location</span></span>
<span data-ttu-id="25d61-122">指定要更新的部署區域位置。</span><span class="sxs-lookup"><span data-stu-id="25d61-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="25d61-123">指定 Api 管理服務支援區域之間的新部署區域位置。</span><span class="sxs-lookup"><span data-stu-id="25d61-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="25d61-124">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" |其中 {$_.ResourceTypes[0]。ResourceTypeName -eq "service"} |Select-Object位置</span><span class="sxs-lookup"><span data-stu-id="25d61-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="25d61-125">-Sku</span></span>
<span data-ttu-id="25d61-126">指定部署區域的新層級值。</span><span class="sxs-lookup"><span data-stu-id="25d61-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="25d61-127">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="25d61-127">Valid values are:</span></span>
- <span data-ttu-id="25d61-128">開發 人員</span><span class="sxs-lookup"><span data-stu-id="25d61-128">Developer</span></span>
- <span data-ttu-id="25d61-129">標準</span><span class="sxs-lookup"><span data-stu-id="25d61-129">Standard</span></span>
- <span data-ttu-id="25d61-130">溢價</span><span class="sxs-lookup"><span data-stu-id="25d61-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25d61-131">-VirtualNetwork</span></span>
<span data-ttu-id="25d61-132">指定部署地區的虛擬網路群組原則。</span><span class="sxs-lookup"><span data-stu-id="25d61-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="25d61-133">傳遞$null將會移除地區的虛擬網路組配置。</span><span class="sxs-lookup"><span data-stu-id="25d61-133">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d61-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d61-134">CommonParameters</span></span>
<span data-ttu-id="25d61-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25d61-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d61-136">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="25d61-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d61-137">輸入</span><span class="sxs-lookup"><span data-stu-id="25d61-137">INPUTS</span></span>

### <span data-ttu-id="25d61-138">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="25d61-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="25d61-139">System.String</span><span class="sxs-lookup"><span data-stu-id="25d61-139">System.String</span></span>

### <span data-ttu-id="25d61-140">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="25d61-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="25d61-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="25d61-141">System.Int32</span></span>

### <span data-ttu-id="25d61-142">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25d61-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="25d61-143">輸出</span><span class="sxs-lookup"><span data-stu-id="25d61-143">OUTPUTS</span></span>

### <span data-ttu-id="25d61-144">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="25d61-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="25d61-145">筆記</span><span class="sxs-lookup"><span data-stu-id="25d61-145">NOTES</span></span>

## <span data-ttu-id="25d61-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="25d61-146">RELATED LINKS</span></span>

[<span data-ttu-id="25d61-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="25d61-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="25d61-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="25d61-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="25d61-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="25d61-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
