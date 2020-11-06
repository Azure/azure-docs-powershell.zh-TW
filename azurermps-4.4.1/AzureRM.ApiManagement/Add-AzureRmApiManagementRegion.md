---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454972"
---
# <span data-ttu-id="53bd5-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="53bd5-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="53bd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="53bd5-103">將新的部署區域新增至 PsApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="53bd5-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="53bd5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bd5-105">說明</span><span class="sxs-lookup"><span data-stu-id="53bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="53bd5-106">**AzureRmApiManagementRegion** Cmdlet 會將類型 **PsApiManagementRegion** 的新實例新增到所提供之 AdditionalRegions 的 **中，** 的 **AdditionalRegions** 。</span><span class="sxs-lookup"><span data-stu-id="53bd5-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="53bd5-107">這個 Cmdlet 不會自行部署任何內容，但會在記憶體中更新 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="53bd5-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="53bd5-108">若要更新 API 管理的部署，請將已修改的 **PsApiManagement** 實例傳到更新-AzureRmApiManagementDeployment。</span><span class="sxs-lookup"><span data-stu-id="53bd5-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="53bd5-109">示例</span><span class="sxs-lookup"><span data-stu-id="53bd5-109">EXAMPLES</span></span>

### <span data-ttu-id="53bd5-110">範例1：將新的部署區域新增至 PsApiManagement 實例</span><span class="sxs-lookup"><span data-stu-id="53bd5-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="53bd5-111">這個命令會將兩個 premium SKU 單位及名為 [東美國] 的區域新增至 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="53bd5-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="53bd5-112">範例2：將新的部署區域新增至 PsApiManagement 實例，然後更新部署</span><span class="sxs-lookup"><span data-stu-id="53bd5-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="53bd5-113">這個命令會取得 **PsApiManagement** 物件，為名為 [東部] 的地區新增兩個 premium SKU 單位，然後更新 [部署]。</span><span class="sxs-lookup"><span data-stu-id="53bd5-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="53bd5-114">參數</span><span class="sxs-lookup"><span data-stu-id="53bd5-114">PARAMETERS</span></span>

### <span data-ttu-id="53bd5-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53bd5-115">-ApiManagement</span></span>
<span data-ttu-id="53bd5-116">指定此 Cmdlet 新增其他部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="53bd5-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="53bd5-117">-容量</span><span class="sxs-lookup"><span data-stu-id="53bd5-117">-Capacity</span></span>
<span data-ttu-id="53bd5-118">指定部署區域的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="53bd5-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="53bd5-119">-位置</span><span class="sxs-lookup"><span data-stu-id="53bd5-119">-Location</span></span>
<span data-ttu-id="53bd5-120">指定新部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="53bd5-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="53bd5-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="53bd5-121">Valid values are:</span></span> 

- <span data-ttu-id="53bd5-122">美國中北部</span><span class="sxs-lookup"><span data-stu-id="53bd5-122">North Central US</span></span>
- <span data-ttu-id="53bd5-123">美國中南部</span><span class="sxs-lookup"><span data-stu-id="53bd5-123">South Central US</span></span>
- <span data-ttu-id="53bd5-124">美國中部</span><span class="sxs-lookup"><span data-stu-id="53bd5-124">Central US</span></span>
- <span data-ttu-id="53bd5-125">西歐</span><span class="sxs-lookup"><span data-stu-id="53bd5-125">West Europe</span></span>
- <span data-ttu-id="53bd5-126">北歐</span><span class="sxs-lookup"><span data-stu-id="53bd5-126">North Europe</span></span>
- <span data-ttu-id="53bd5-127">美國西部</span><span class="sxs-lookup"><span data-stu-id="53bd5-127">West US</span></span>
- <span data-ttu-id="53bd5-128">東美國</span><span class="sxs-lookup"><span data-stu-id="53bd5-128">East US</span></span>
- <span data-ttu-id="53bd5-129">東美國2</span><span class="sxs-lookup"><span data-stu-id="53bd5-129">East US 2</span></span>
- <span data-ttu-id="53bd5-130">日本東</span><span class="sxs-lookup"><span data-stu-id="53bd5-130">Japan East</span></span>
- <span data-ttu-id="53bd5-131">日本西部</span><span class="sxs-lookup"><span data-stu-id="53bd5-131">Japan West</span></span>
- <span data-ttu-id="53bd5-132">巴西南部</span><span class="sxs-lookup"><span data-stu-id="53bd5-132">Brazil South</span></span>
- <span data-ttu-id="53bd5-133">東南亞</span><span class="sxs-lookup"><span data-stu-id="53bd5-133">Southeast Asia</span></span>
- <span data-ttu-id="53bd5-134">東亞</span><span class="sxs-lookup"><span data-stu-id="53bd5-134">East Asia</span></span>
- <span data-ttu-id="53bd5-135">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="53bd5-135">Australia East</span></span>
- <span data-ttu-id="53bd5-136">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="53bd5-136">Australia Southeast</span></span>

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

### <span data-ttu-id="53bd5-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="53bd5-137">-Sku</span></span>
<span data-ttu-id="53bd5-138">指定部署區域的層級。</span><span class="sxs-lookup"><span data-stu-id="53bd5-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="53bd5-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="53bd5-139">Valid values are:</span></span> 

- <span data-ttu-id="53bd5-140">人員</span><span class="sxs-lookup"><span data-stu-id="53bd5-140">Developer</span></span>
- <span data-ttu-id="53bd5-141">標準</span><span class="sxs-lookup"><span data-stu-id="53bd5-141">Standard</span></span>
- <span data-ttu-id="53bd5-142">佳</span><span class="sxs-lookup"><span data-stu-id="53bd5-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bd5-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="53bd5-143">-VirtualNetwork</span></span>
<span data-ttu-id="53bd5-144">指定虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="53bd5-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="53bd5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bd5-145">-DefaultProfile</span></span>
<span data-ttu-id="53bd5-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53bd5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bd5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bd5-147">CommonParameters</span></span>
<span data-ttu-id="53bd5-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53bd5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bd5-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53bd5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bd5-150">輸入</span><span class="sxs-lookup"><span data-stu-id="53bd5-150">INPUTS</span></span>

### <span data-ttu-id="53bd5-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="53bd5-151">PsApiManagement</span></span>
<span data-ttu-id="53bd5-152">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53bd5-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="53bd5-153">輸出</span><span class="sxs-lookup"><span data-stu-id="53bd5-153">OUTPUTS</span></span>

### <span data-ttu-id="53bd5-154">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="53bd5-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="53bd5-155">筆記</span><span class="sxs-lookup"><span data-stu-id="53bd5-155">NOTES</span></span>
* <span data-ttu-id="53bd5-156">這個 Cmdlet 會將更新的 **PsApiManagement** 實例寫入管線。</span><span class="sxs-lookup"><span data-stu-id="53bd5-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="53bd5-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="53bd5-157">RELATED LINKS</span></span>

[<span data-ttu-id="53bd5-158">移除-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="53bd5-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="53bd5-159">更新-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="53bd5-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="53bd5-160">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="53bd5-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


