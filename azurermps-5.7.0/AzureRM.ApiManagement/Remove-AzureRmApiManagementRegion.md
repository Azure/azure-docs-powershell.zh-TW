---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457511"
---
# <span data-ttu-id="33ef3-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="33ef3-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="33ef3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="33ef3-103">從 PsApiManagement 實例移除現有的部署區域。</span><span class="sxs-lookup"><span data-stu-id="33ef3-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ef3-104">句法</span><span class="sxs-lookup"><span data-stu-id="33ef3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ef3-105">說明</span><span class="sxs-lookup"><span data-stu-id="33ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="33ef3-106">AzureRmApiManagementRegion Cmdlet 會從已提供 type **PsApiManagementRegion ApiManagement** 的實例的 AdditionalRegions 集合中移除類型的實例， **並** 從 **的** 中移除的 **。**</span><span class="sxs-lookup"><span data-stu-id="33ef3-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="33ef3-107">這個 Cmdlet 不會自行修改部署，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="33ef3-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="33ef3-108">若要更新 API 管理的部署，請將修改過的 **PsApiManagementInstance** 傳遞到 **update-AzureRmApiManagement** 。</span><span class="sxs-lookup"><span data-stu-id="33ef3-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="33ef3-109">示例</span><span class="sxs-lookup"><span data-stu-id="33ef3-109">EXAMPLES</span></span>

### <span data-ttu-id="33ef3-110">範例1：從 PsApiManagement 實例中移除區域</span><span class="sxs-lookup"><span data-stu-id="33ef3-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="33ef3-111">這個命令會從 **PsApiManagement** 實例中移除名為「美國東部」的地區。</span><span class="sxs-lookup"><span data-stu-id="33ef3-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="33ef3-112">範例2：使用一系列命令從 PsApiManagement 實例中移除區域</span><span class="sxs-lookup"><span data-stu-id="33ef3-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="33ef3-113">這個第一個命令會從名為 Contoso 的資源群組（名為 ContosoApi）中取得 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="33ef3-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="33ef3-114">然後，最後一個命令會從該實例移除名為 East 的地區，然後更新部署。</span><span class="sxs-lookup"><span data-stu-id="33ef3-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="33ef3-115">參數</span><span class="sxs-lookup"><span data-stu-id="33ef3-115">PARAMETERS</span></span>

### <span data-ttu-id="33ef3-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33ef3-116">-ApiManagement</span></span>
<span data-ttu-id="33ef3-117">指定此 Cmdlet 移除其他部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="33ef3-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="33ef3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ef3-118">-DefaultProfile</span></span>
<span data-ttu-id="33ef3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33ef3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="33ef3-120">-位置</span><span class="sxs-lookup"><span data-stu-id="33ef3-120">-Location</span></span>
<span data-ttu-id="33ef3-121">指定此 Cmdlet 移除之區域的位置。</span><span class="sxs-lookup"><span data-stu-id="33ef3-121">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="33ef3-122">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="33ef3-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="33ef3-123">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="33ef3-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="33ef3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ef3-124">CommonParameters</span></span>
<span data-ttu-id="33ef3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33ef3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ef3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33ef3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ef3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="33ef3-127">INPUTS</span></span>

### <span data-ttu-id="33ef3-128">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="33ef3-128">PsApiManagement</span></span>
<span data-ttu-id="33ef3-129">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="33ef3-129">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="33ef3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="33ef3-130">OUTPUTS</span></span>

### <span data-ttu-id="33ef3-131">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="33ef3-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="33ef3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="33ef3-132">NOTES</span></span>

## <span data-ttu-id="33ef3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="33ef3-133">RELATED LINKS</span></span>

[<span data-ttu-id="33ef3-134">附加 AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="33ef3-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="33ef3-135">更新-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="33ef3-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


