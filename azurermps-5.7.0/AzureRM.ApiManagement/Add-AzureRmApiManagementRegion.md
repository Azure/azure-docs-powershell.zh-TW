---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457208"
---
# <span data-ttu-id="b8b21-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8b21-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="b8b21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8b21-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b21-103">將新的部署區域新增至 PsApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="b8b21-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8b21-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8b21-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8b21-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8b21-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b21-106">**AzureRmApiManagementRegion** Cmdlet 會將類型 **PsApiManagementRegion** 的新實例新增到所提供之 AdditionalRegions 的 **中，** 的 **AdditionalRegions** 。</span><span class="sxs-lookup"><span data-stu-id="b8b21-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b8b21-107">這個 Cmdlet 不會自行部署任何內容，但會在記憶體中更新 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b8b21-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b8b21-108">若要更新 API 管理的部署，請將已修改的 **PsApiManagement** 實例傳到更新-AzureRmApiManagementDeployment。</span><span class="sxs-lookup"><span data-stu-id="b8b21-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="b8b21-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8b21-109">EXAMPLES</span></span>

### <span data-ttu-id="b8b21-110">範例1：將新的部署區域新增至 PsApiManagement 實例</span><span class="sxs-lookup"><span data-stu-id="b8b21-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="b8b21-111">這個命令會將兩個 premium SKU 單位及名為 [東美國] 的區域新增至 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="b8b21-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b8b21-112">範例2：將新的部署區域新增至 PsApiManagement 實例，然後更新部署</span><span class="sxs-lookup"><span data-stu-id="b8b21-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="b8b21-113">這個命令會取得 **PsApiManagement** 物件，為名為 [東部] 的地區新增兩個 premium SKU 單位，然後更新 [部署]。</span><span class="sxs-lookup"><span data-stu-id="b8b21-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="b8b21-114">參數</span><span class="sxs-lookup"><span data-stu-id="b8b21-114">PARAMETERS</span></span>

### <span data-ttu-id="b8b21-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8b21-115">-ApiManagement</span></span>
<span data-ttu-id="b8b21-116">指定此 Cmdlet 新增其他部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="b8b21-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-117">-容量</span><span class="sxs-lookup"><span data-stu-id="b8b21-117">-Capacity</span></span>
<span data-ttu-id="b8b21-118">指定部署區域的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="b8b21-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b21-119">-DefaultProfile</span></span>
<span data-ttu-id="b8b21-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8b21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b8b21-121">-Location</span></span>
<span data-ttu-id="b8b21-122">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="b8b21-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="b8b21-123">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="b8b21-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="b8b21-124">-Sku</span></span>
<span data-ttu-id="b8b21-125">指定部署區域的層級。</span><span class="sxs-lookup"><span data-stu-id="b8b21-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="b8b21-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b8b21-126">Valid values are:</span></span> 

- <span data-ttu-id="b8b21-127">人員</span><span class="sxs-lookup"><span data-stu-id="b8b21-127">Developer</span></span>
- <span data-ttu-id="b8b21-128">標準</span><span class="sxs-lookup"><span data-stu-id="b8b21-128">Standard</span></span>
- <span data-ttu-id="b8b21-129">佳</span><span class="sxs-lookup"><span data-stu-id="b8b21-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8b21-130">-VirtualNetwork</span></span>
<span data-ttu-id="b8b21-131">指定虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="b8b21-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b21-132">CommonParameters</span></span>
<span data-ttu-id="b8b21-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8b21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b21-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8b21-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b21-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b8b21-135">INPUTS</span></span>

### <span data-ttu-id="b8b21-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8b21-136">PsApiManagement</span></span>
<span data-ttu-id="b8b21-137">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b8b21-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="b8b21-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b8b21-138">OUTPUTS</span></span>

### <span data-ttu-id="b8b21-139">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b8b21-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b8b21-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b8b21-140">NOTES</span></span>
* <span data-ttu-id="b8b21-141">這個 Cmdlet 會將更新的 **PsApiManagement** 實例寫入管線。</span><span class="sxs-lookup"><span data-stu-id="b8b21-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="b8b21-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8b21-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8b21-143">移除-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8b21-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="b8b21-144">更新-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8b21-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="b8b21-145">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b8b21-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


