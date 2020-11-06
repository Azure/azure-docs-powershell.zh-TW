---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: b180dabec976164eac70106b49378d832fb00db8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611650"
---
# <span data-ttu-id="b8c7d-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8c7d-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="b8c7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c7d-103">將新的部署區域新增至 PsApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="b8c7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c7d-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c7d-106">**AzApiManagementRegion** Cmdlet 會將類型 **PsApiManagementRegion** 的新實例新增到所提供之 AdditionalRegions 的 **中，** 的 **AdditionalRegions** 。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b8c7d-107">這個 Cmdlet 不會自行部署任何內容，但會在記憶體中更新 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b8c7d-108">若要更新 API 管理的部署，請將已修改的 **PsApiManagement** 實例傳到更新-AzApiManagementDeployment。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzApiManagementDeployment.</span></span>

## <span data-ttu-id="b8c7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8c7d-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c7d-110">範例1：將新的部署區域新增至 PsApiManagement 實例</span><span class="sxs-lookup"><span data-stu-id="b8c7d-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="b8c7d-111">這個命令會將兩個 premium SKU 單位及名為 [東美國] 的區域新增至 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b8c7d-112">範例2：將新的部署區域新增至 PsApiManagement 實例，然後更新部署</span><span class="sxs-lookup"><span data-stu-id="b8c7d-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzApiManagementDeployment
```

<span data-ttu-id="b8c7d-113">這個命令會取得 **PsApiManagement** 物件，為名為 [東部] 的地區新增兩個 premium SKU 單位，然後更新 [部署]。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="b8c7d-114">參數</span><span class="sxs-lookup"><span data-stu-id="b8c7d-114">PARAMETERS</span></span>

### <span data-ttu-id="b8c7d-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8c7d-115">-ApiManagement</span></span>
<span data-ttu-id="b8c7d-116">指定此 Cmdlet 新增其他部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="b8c7d-117">-容量</span><span class="sxs-lookup"><span data-stu-id="b8c7d-117">-Capacity</span></span>
<span data-ttu-id="b8c7d-118">指定部署區域的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c7d-119">-DefaultProfile</span></span>
<span data-ttu-id="b8c7d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c7d-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b8c7d-121">-Location</span></span>
<span data-ttu-id="b8c7d-122">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="b8c7d-123">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="b8c7d-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="b8c7d-124">-Sku</span></span>
<span data-ttu-id="b8c7d-125">指定部署區域的層級。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="b8c7d-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b8c7d-126">Valid values are:</span></span> 
- <span data-ttu-id="b8c7d-127">人員</span><span class="sxs-lookup"><span data-stu-id="b8c7d-127">Developer</span></span>
- <span data-ttu-id="b8c7d-128">標準</span><span class="sxs-lookup"><span data-stu-id="b8c7d-128">Standard</span></span>
- <span data-ttu-id="b8c7d-129">佳</span><span class="sxs-lookup"><span data-stu-id="b8c7d-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8c7d-130">-VirtualNetwork</span></span>
<span data-ttu-id="b8c7d-131">指定虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c7d-132">CommonParameters</span></span>
<span data-ttu-id="b8c7d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c7d-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c7d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c7d-135">INPUTS</span></span>

### <span data-ttu-id="b8c7d-136">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b8c7d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c7d-137">OUTPUTS</span></span>

### <span data-ttu-id="b8c7d-138">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b8c7d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c7d-139">NOTES</span></span>
* <span data-ttu-id="b8c7d-140">這個 Cmdlet 會將更新的 **PsApiManagement** 實例寫入管線。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="b8c7d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c7d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b8c7d-142">移除-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8c7d-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="b8c7d-143">更新-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b8c7d-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="b8c7d-144">更新-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b8c7d-144">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

