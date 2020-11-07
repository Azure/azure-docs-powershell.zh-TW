---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fff6145adaa909bcadde90f36802072b812ba0ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965604"
---
# <span data-ttu-id="b3879-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b3879-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="b3879-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3879-102">SYNOPSIS</span></span>
<span data-ttu-id="b3879-103">更新 PsApiManagement 實例中的現有部署區域。</span><span class="sxs-lookup"><span data-stu-id="b3879-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="b3879-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3879-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3879-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3879-105">DESCRIPTION</span></span>
<span data-ttu-id="b3879-106">**AzApiManagementRegion** Cmdlet 會在所提供實例的 AdditionalRegions 物件集合中，更新 ApiManagement **類型的** **AdditionalRegions** 物件 **PsApiManagementRegion** 中的一個現有實例。 ApiManagement. PsApiManagement..。</span><span class="sxs-lookup"><span data-stu-id="b3879-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b3879-107">這個 Cmdlet 不會部署任何內容，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b3879-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b3879-108">若要更新 API 管理的部署，請使用已修改的 **PsApiManagementInstance** 到 Set-AzApiManagement Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3879-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="b3879-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3879-109">EXAMPLES</span></span>

### <span data-ttu-id="b3879-110">範例1：增加 PsApiManagement 實例中額外區域的容量</span><span class="sxs-lookup"><span data-stu-id="b3879-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="b3879-111">這個命令會取得 API 管理 Premium SKU 服務，在美國中南部和北中央都有地區。</span><span class="sxs-lookup"><span data-stu-id="b3879-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="b3879-112">然後使用 **AzApiManagement** ，將北部的中美區域容量增加到2。</span><span class="sxs-lookup"><span data-stu-id="b3879-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="b3879-113">下一個 Cmdlet **AzApiManagement** 會將設定變更套用至 Api 管理服務。</span><span class="sxs-lookup"><span data-stu-id="b3879-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="b3879-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3879-114">PARAMETERS</span></span>

### <span data-ttu-id="b3879-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3879-115">-ApiManagement</span></span>
<span data-ttu-id="b3879-116">指定要在其中更新現有部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="b3879-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="b3879-117">-容量</span><span class="sxs-lookup"><span data-stu-id="b3879-117">-Capacity</span></span>
<span data-ttu-id="b3879-118">指定部署區域的新 SKU 容量值。</span><span class="sxs-lookup"><span data-stu-id="b3879-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="b3879-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3879-119">-DefaultProfile</span></span>
<span data-ttu-id="b3879-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3879-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3879-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b3879-121">-Location</span></span>
<span data-ttu-id="b3879-122">指定要更新之部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="b3879-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="b3879-123">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="b3879-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="b3879-124">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="b3879-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="b3879-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="b3879-125">-Sku</span></span>
<span data-ttu-id="b3879-126">指定部署區域的新層級值。</span><span class="sxs-lookup"><span data-stu-id="b3879-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="b3879-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b3879-127">Valid values are:</span></span>
- <span data-ttu-id="b3879-128">人員</span><span class="sxs-lookup"><span data-stu-id="b3879-128">Developer</span></span>
- <span data-ttu-id="b3879-129">標準</span><span class="sxs-lookup"><span data-stu-id="b3879-129">Standard</span></span>
- <span data-ttu-id="b3879-130">佳</span><span class="sxs-lookup"><span data-stu-id="b3879-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3879-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3879-131">-VirtualNetwork</span></span>
<span data-ttu-id="b3879-132">指定部署區域的虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="b3879-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="b3879-133">傳遞 $null 將會移除該區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="b3879-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="b3879-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3879-134">CommonParameters</span></span>
<span data-ttu-id="b3879-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3879-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3879-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3879-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3879-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b3879-137">INPUTS</span></span>

### <span data-ttu-id="b3879-138">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b3879-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="b3879-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b3879-139">System.String</span></span>

### <span data-ttu-id="b3879-140">PsApiManagementSku 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b3879-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="b3879-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b3879-141">System.Int32</span></span>

### <span data-ttu-id="b3879-142">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b3879-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="b3879-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b3879-143">OUTPUTS</span></span>

### <span data-ttu-id="b3879-144">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b3879-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b3879-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b3879-145">NOTES</span></span>

## <span data-ttu-id="b3879-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3879-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3879-147">附加 AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b3879-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="b3879-148">移除-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b3879-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="b3879-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3879-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
