---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445776"
---
# <span data-ttu-id="fff65-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fff65-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="fff65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fff65-102">SYNOPSIS</span></span>
<span data-ttu-id="fff65-103">更新 PsApiManagement 實例中的現有部署區域。</span><span class="sxs-lookup"><span data-stu-id="fff65-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fff65-104">句法</span><span class="sxs-lookup"><span data-stu-id="fff65-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fff65-105">說明</span><span class="sxs-lookup"><span data-stu-id="fff65-105">DESCRIPTION</span></span>
<span data-ttu-id="fff65-106">**AzureRmApiManagementRegion** Cmdlet 會在所提供實例的 AdditionalRegions 物件集合中，更新 ApiManagement **類型的** **AdditionalRegions** 物件 **PsApiManagementRegion** 中的一個現有實例。 ApiManagement. PsApiManagement..。</span><span class="sxs-lookup"><span data-stu-id="fff65-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="fff65-107">這個 Cmdlet 不會部署任何內容，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="fff65-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="fff65-108">若要更新 API 管理的部署，請使用已修改的 **PsApiManagementInstance** 到 Update-AzureRmApiManagementDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fff65-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="fff65-109">示例</span><span class="sxs-lookup"><span data-stu-id="fff65-109">EXAMPLES</span></span>

## <span data-ttu-id="fff65-110">參數</span><span class="sxs-lookup"><span data-stu-id="fff65-110">PARAMETERS</span></span>

### <span data-ttu-id="fff65-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fff65-111">-ApiManagement</span></span>
<span data-ttu-id="fff65-112">指定要在其中更新現有部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="fff65-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="fff65-113">-容量</span><span class="sxs-lookup"><span data-stu-id="fff65-113">-Capacity</span></span>
<span data-ttu-id="fff65-114">指定部署區域的新 SKU 容量值。</span><span class="sxs-lookup"><span data-stu-id="fff65-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="fff65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff65-115">-DefaultProfile</span></span>
<span data-ttu-id="fff65-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fff65-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff65-117">-位置</span><span class="sxs-lookup"><span data-stu-id="fff65-117">-Location</span></span>
<span data-ttu-id="fff65-118">指定要更新之部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="fff65-118">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="fff65-119">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="fff65-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="fff65-120">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="fff65-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="fff65-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="fff65-121">-Sku</span></span>
<span data-ttu-id="fff65-122">指定部署區域的新層級值。</span><span class="sxs-lookup"><span data-stu-id="fff65-122">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="fff65-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="fff65-123">Valid values are:</span></span>
- <span data-ttu-id="fff65-124">人員</span><span class="sxs-lookup"><span data-stu-id="fff65-124">Developer</span></span>
- <span data-ttu-id="fff65-125">標準</span><span class="sxs-lookup"><span data-stu-id="fff65-125">Standard</span></span>
- <span data-ttu-id="fff65-126">佳</span><span class="sxs-lookup"><span data-stu-id="fff65-126">Premium</span></span>

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

### <span data-ttu-id="fff65-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fff65-127">-VirtualNetwork</span></span>
<span data-ttu-id="fff65-128">指定部署區域的虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="fff65-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="fff65-129">傳遞 $null 將會移除該區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="fff65-129">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="fff65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff65-130">CommonParameters</span></span>
<span data-ttu-id="fff65-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fff65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff65-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fff65-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff65-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fff65-133">INPUTS</span></span>

### <span data-ttu-id="fff65-134">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="fff65-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="fff65-135">參數： ApiManagement (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fff65-135">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="fff65-136">System.object</span><span class="sxs-lookup"><span data-stu-id="fff65-136">System.String</span></span>

### <span data-ttu-id="fff65-137">PsApiManagementSku 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="fff65-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="fff65-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fff65-138">System.Int32</span></span>

### <span data-ttu-id="fff65-139">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="fff65-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="fff65-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fff65-140">OUTPUTS</span></span>

### <span data-ttu-id="fff65-141">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="fff65-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fff65-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fff65-142">NOTES</span></span>

## <span data-ttu-id="fff65-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fff65-143">RELATED LINKS</span></span>

[<span data-ttu-id="fff65-144">附加 AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fff65-144">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="fff65-145">移除-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fff65-145">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="fff65-146">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fff65-146">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
