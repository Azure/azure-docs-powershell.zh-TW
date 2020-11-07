---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625487"
---
# <span data-ttu-id="ed7d7-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ed7d7-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="ed7d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7d7-103">更新 PsApiManagement 實例中的現有部署區域。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed7d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed7d7-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed7d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7d7-106">**AzureRmApiManagementRegion** Cmdlet 會在所提供實例的 AdditionalRegions 物件集合中，更新 ApiManagement **類型的** **AdditionalRegions** 物件 **PsApiManagementRegion** 中的一個現有實例。 ApiManagement. PsApiManagement..。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ed7d7-107">這個 Cmdlet 不會部署任何內容，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ed7d7-108">若要更新 API 管理的部署，請使用已修改的 **PsApiManagementInstance** 到 Update-AzureRmApiManagementDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="ed7d7-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed7d7-109">EXAMPLES</span></span>

## <span data-ttu-id="ed7d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="ed7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="ed7d7-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed7d7-111">-ApiManagement</span></span>
<span data-ttu-id="ed7d7-112">指定要在其中更新現有部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="ed7d7-113">-容量</span><span class="sxs-lookup"><span data-stu-id="ed7d7-113">-Capacity</span></span>
<span data-ttu-id="ed7d7-114">指定部署區域的新 SKU 容量值。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7d7-115">-DefaultProfile</span></span>
<span data-ttu-id="ed7d7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ed7d7-117">-位置</span><span class="sxs-lookup"><span data-stu-id="ed7d7-117">-Location</span></span>
<span data-ttu-id="ed7d7-118">指定要更新之部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="ed7d7-119">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="ed7d7-120">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="ed7d7-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7d7-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="ed7d7-121">-Sku</span></span>
<span data-ttu-id="ed7d7-122">指定部署區域的新層級值。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="ed7d7-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ed7d7-123">Valid values are:</span></span>

- <span data-ttu-id="ed7d7-124">人員</span><span class="sxs-lookup"><span data-stu-id="ed7d7-124">Developer</span></span>
- <span data-ttu-id="ed7d7-125">標準</span><span class="sxs-lookup"><span data-stu-id="ed7d7-125">Standard</span></span>
- <span data-ttu-id="ed7d7-126">佳</span><span class="sxs-lookup"><span data-stu-id="ed7d7-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7d7-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed7d7-127">-VirtualNetwork</span></span>
<span data-ttu-id="ed7d7-128">指定部署區域的虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="ed7d7-129">傳遞 $null 將會移除該區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7d7-130">CommonParameters</span></span>
<span data-ttu-id="ed7d7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7d7-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7d7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ed7d7-133">INPUTS</span></span>

### <span data-ttu-id="ed7d7-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed7d7-134">PsApiManagement</span></span>
<span data-ttu-id="ed7d7-135">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ed7d7-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="ed7d7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ed7d7-136">OUTPUTS</span></span>

### <span data-ttu-id="ed7d7-137">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="ed7d7-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ed7d7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ed7d7-138">NOTES</span></span>

## <span data-ttu-id="ed7d7-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed7d7-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed7d7-140">附加 AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ed7d7-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="ed7d7-141">移除-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ed7d7-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="ed7d7-142">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ed7d7-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
