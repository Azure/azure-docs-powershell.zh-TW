---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: aebcb8be906811607aefee7dbdc2c7630b9e391e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401176"
---
# <span data-ttu-id="164b9-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="164b9-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="164b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="164b9-102">SYNOPSIS</span></span>
<span data-ttu-id="164b9-103">新增部署區域至 PsApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="164b9-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="164b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="164b9-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="164b9-105">描述</span><span class="sxs-lookup"><span data-stu-id="164b9-105">DESCRIPTION</span></span>
<span data-ttu-id="164b9-106">**Add-AzApiManagementRegion** Cmdlet 會將 **類型 PsApiManagementRegion** 的新實例新增到 **Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement** 類型提供實例的 **AdditionalRegions** 集合。</span><span class="sxs-lookup"><span data-stu-id="164b9-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="164b9-107">此 Cmdlet 不會自行部署任何專案，但會更新 **記憶體中的 PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="164b9-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="164b9-108">若要更新 API 管理部署，請將修改後的 **PsApiManagement** 實例傳遞至 Set-AzApiManagement。</span><span class="sxs-lookup"><span data-stu-id="164b9-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="164b9-109">例子</span><span class="sxs-lookup"><span data-stu-id="164b9-109">EXAMPLES</span></span>

### <span data-ttu-id="164b9-110">範例 1：新增部署區域至 PsApiManagement 實例</span><span class="sxs-lookup"><span data-stu-id="164b9-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="164b9-111">此命令會將兩個進位 SKU 單位和名為 East US 的區域新增到 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="164b9-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="164b9-112">範例 2：新增部署區域至 PsApiManagement 實例，然後更新部署</span><span class="sxs-lookup"><span data-stu-id="164b9-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Set-AzApiManagement
```

<span data-ttu-id="164b9-113">此命令會獲得 **PsApiManagement 物件** 、為名為 East US 的區域新增兩個進位 SKU 單位，然後更新部署。</span><span class="sxs-lookup"><span data-stu-id="164b9-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="164b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="164b9-114">PARAMETERS</span></span>

### <span data-ttu-id="164b9-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="164b9-115">-ApiManagement</span></span>
<span data-ttu-id="164b9-116">指定此 **Cmdlet 新增其他部署區域的 PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="164b9-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="164b9-117">-容量</span><span class="sxs-lookup"><span data-stu-id="164b9-117">-Capacity</span></span>
<span data-ttu-id="164b9-118">指定部署地區的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="164b9-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="164b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164b9-119">-DefaultProfile</span></span>
<span data-ttu-id="164b9-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="164b9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="164b9-121">-位置</span><span class="sxs-lookup"><span data-stu-id="164b9-121">-Location</span></span>
<span data-ttu-id="164b9-122">指定 Api 管理服務支援區域之間的新部署區域位置。</span><span class="sxs-lookup"><span data-stu-id="164b9-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="164b9-123">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" |其中 {$_.ResourceTypes[0]。ResourceTypeName -eq "service"} |Select-Object位置</span><span class="sxs-lookup"><span data-stu-id="164b9-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="164b9-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="164b9-124">-Sku</span></span>
<span data-ttu-id="164b9-125">指定部署區域層級。</span><span class="sxs-lookup"><span data-stu-id="164b9-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="164b9-126">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="164b9-126">Valid values are:</span></span>
- <span data-ttu-id="164b9-127">開發 人員</span><span class="sxs-lookup"><span data-stu-id="164b9-127">Developer</span></span>
- <span data-ttu-id="164b9-128">標準</span><span class="sxs-lookup"><span data-stu-id="164b9-128">Standard</span></span>
- <span data-ttu-id="164b9-129">溢價</span><span class="sxs-lookup"><span data-stu-id="164b9-129">Premium</span></span>

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

### <span data-ttu-id="164b9-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="164b9-130">-VirtualNetwork</span></span>
<span data-ttu-id="164b9-131">指定虛擬網路組配置。</span><span class="sxs-lookup"><span data-stu-id="164b9-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="164b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164b9-132">CommonParameters</span></span>
<span data-ttu-id="164b9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="164b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164b9-134">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="164b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164b9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="164b9-135">INPUTS</span></span>

### <span data-ttu-id="164b9-136">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="164b9-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="164b9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="164b9-137">OUTPUTS</span></span>

### <span data-ttu-id="164b9-138">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="164b9-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="164b9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="164b9-139">NOTES</span></span>
* <span data-ttu-id="164b9-140">Cmdlet 會將更新 **的 PsApiManagement 實例** 寫入管線。</span><span class="sxs-lookup"><span data-stu-id="164b9-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="164b9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="164b9-141">RELATED LINKS</span></span>

[<span data-ttu-id="164b9-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="164b9-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="164b9-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="164b9-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="164b9-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="164b9-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


