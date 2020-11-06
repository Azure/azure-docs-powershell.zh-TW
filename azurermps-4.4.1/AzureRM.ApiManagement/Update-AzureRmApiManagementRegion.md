---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445155"
---
# <span data-ttu-id="f8d24-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f8d24-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="f8d24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8d24-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d24-103">更新 PsApiManagement 實例中的現有部署區域。</span><span class="sxs-lookup"><span data-stu-id="f8d24-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d24-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8d24-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8d24-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8d24-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d24-106">**AzureRmApiManagementRegion** Cmdlet 會在所提供實例的 AdditionalRegions 物件集合中，更新 ApiManagement **類型的** **AdditionalRegions** 物件 **PsApiManagementRegion** 中的一個現有實例。 ApiManagement. PsApiManagement..。</span><span class="sxs-lookup"><span data-stu-id="f8d24-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f8d24-107">這個 Cmdlet 不會部署任何內容，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="f8d24-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f8d24-108">若要更新 API 管理的部署，請使用已修改的 **PsApiManagementInstance** 到 Update-AzureRmApiManagementDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8d24-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="f8d24-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8d24-109">EXAMPLES</span></span>

## <span data-ttu-id="f8d24-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8d24-110">PARAMETERS</span></span>

### <span data-ttu-id="f8d24-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8d24-111">-ApiManagement</span></span>
<span data-ttu-id="f8d24-112">指定要在其中更新現有部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="f8d24-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="f8d24-113">-容量</span><span class="sxs-lookup"><span data-stu-id="f8d24-113">-Capacity</span></span>
<span data-ttu-id="f8d24-114">指定部署區域的新 SKU 容量值。</span><span class="sxs-lookup"><span data-stu-id="f8d24-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="f8d24-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f8d24-115">-Location</span></span>
<span data-ttu-id="f8d24-116">指定要更新之部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="f8d24-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="f8d24-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f8d24-117">Valid values are:</span></span>

- <span data-ttu-id="f8d24-118">美國中北部</span><span class="sxs-lookup"><span data-stu-id="f8d24-118">North Central US</span></span>
- <span data-ttu-id="f8d24-119">美國中南部</span><span class="sxs-lookup"><span data-stu-id="f8d24-119">South Central US</span></span>
- <span data-ttu-id="f8d24-120">美國中部</span><span class="sxs-lookup"><span data-stu-id="f8d24-120">Central US</span></span>
- <span data-ttu-id="f8d24-121">西歐</span><span class="sxs-lookup"><span data-stu-id="f8d24-121">West Europe</span></span>
- <span data-ttu-id="f8d24-122">北歐</span><span class="sxs-lookup"><span data-stu-id="f8d24-122">North Europe</span></span>
- <span data-ttu-id="f8d24-123">美國西部</span><span class="sxs-lookup"><span data-stu-id="f8d24-123">West US</span></span>
- <span data-ttu-id="f8d24-124">東美國</span><span class="sxs-lookup"><span data-stu-id="f8d24-124">East US</span></span>
- <span data-ttu-id="f8d24-125">東美國2</span><span class="sxs-lookup"><span data-stu-id="f8d24-125">East US 2</span></span>
- <span data-ttu-id="f8d24-126">日本東</span><span class="sxs-lookup"><span data-stu-id="f8d24-126">Japan East</span></span>
- <span data-ttu-id="f8d24-127">日本西部</span><span class="sxs-lookup"><span data-stu-id="f8d24-127">Japan West</span></span>
- <span data-ttu-id="f8d24-128">巴西南部</span><span class="sxs-lookup"><span data-stu-id="f8d24-128">Brazil South</span></span>
- <span data-ttu-id="f8d24-129">東南亞</span><span class="sxs-lookup"><span data-stu-id="f8d24-129">Southeast Asia</span></span>
- <span data-ttu-id="f8d24-130">東亞</span><span class="sxs-lookup"><span data-stu-id="f8d24-130">East Asia</span></span>
- <span data-ttu-id="f8d24-131">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="f8d24-131">Australia East</span></span>
- <span data-ttu-id="f8d24-132">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="f8d24-132">Australia Southeast</span></span>

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

### <span data-ttu-id="f8d24-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="f8d24-133">-Sku</span></span>
<span data-ttu-id="f8d24-134">指定部署區域的新層級值。</span><span class="sxs-lookup"><span data-stu-id="f8d24-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="f8d24-135">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f8d24-135">Valid values are:</span></span>

- <span data-ttu-id="f8d24-136">人員</span><span class="sxs-lookup"><span data-stu-id="f8d24-136">Developer</span></span>
- <span data-ttu-id="f8d24-137">標準</span><span class="sxs-lookup"><span data-stu-id="f8d24-137">Standard</span></span>
- <span data-ttu-id="f8d24-138">佳</span><span class="sxs-lookup"><span data-stu-id="f8d24-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d24-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f8d24-139">-VirtualNetwork</span></span>
<span data-ttu-id="f8d24-140">指定部署區域的虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="f8d24-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="f8d24-141">傳遞 $null 將會移除該區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="f8d24-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="f8d24-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d24-142">-DefaultProfile</span></span>
<span data-ttu-id="f8d24-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8d24-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d24-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d24-144">CommonParameters</span></span>
<span data-ttu-id="f8d24-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8d24-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d24-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8d24-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d24-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f8d24-147">INPUTS</span></span>

### <span data-ttu-id="f8d24-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8d24-148">PsApiManagement</span></span>
<span data-ttu-id="f8d24-149">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f8d24-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="f8d24-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f8d24-150">OUTPUTS</span></span>

### <span data-ttu-id="f8d24-151">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="f8d24-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f8d24-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f8d24-152">NOTES</span></span>

## <span data-ttu-id="f8d24-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8d24-153">RELATED LINKS</span></span>

[<span data-ttu-id="f8d24-154">附加 AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f8d24-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f8d24-155">移除-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f8d24-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f8d24-156">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f8d24-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
