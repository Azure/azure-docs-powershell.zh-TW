---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: dc51caee3a0cb8d5571a5a316c2018c30abbe239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457516"
---
# <span data-ttu-id="22dfd-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="22dfd-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="22dfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="22dfd-103">建立 PsApiManagementRegion 的實例。</span><span class="sxs-lookup"><span data-stu-id="22dfd-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22dfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="22dfd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22dfd-105">說明</span><span class="sxs-lookup"><span data-stu-id="22dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="22dfd-106">[Helper] 命令來建立 PsApiManagementRegion 的實例。</span><span class="sxs-lookup"><span data-stu-id="22dfd-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="22dfd-107">此命令將與 New-AzureRmApiManagement 命令搭配使用。</span><span class="sxs-lookup"><span data-stu-id="22dfd-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="22dfd-108">示例</span><span class="sxs-lookup"><span data-stu-id="22dfd-108">EXAMPLES</span></span>

### <span data-ttu-id="22dfd-109">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="22dfd-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="22dfd-110">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="22dfd-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="22dfd-111">在 West 美國地區建立外部 VpnType 的 ApiManagement 服務，並在美國中部新增一個區域。</span><span class="sxs-lookup"><span data-stu-id="22dfd-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="22dfd-112">參數</span><span class="sxs-lookup"><span data-stu-id="22dfd-112">PARAMETERS</span></span>

### <span data-ttu-id="22dfd-113">-容量</span><span class="sxs-lookup"><span data-stu-id="22dfd-113">-Capacity</span></span>
<span data-ttu-id="22dfd-114">Azure API Management 服務其他區域的 Sku 容量。</span><span class="sxs-lookup"><span data-stu-id="22dfd-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="22dfd-115">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="22dfd-115">Default value is 1.</span></span>

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

### <span data-ttu-id="22dfd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dfd-116">-DefaultProfile</span></span>
<span data-ttu-id="22dfd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22dfd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="22dfd-118">-位置</span><span class="sxs-lookup"><span data-stu-id="22dfd-118">-Location</span></span>
<span data-ttu-id="22dfd-119">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="22dfd-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="22dfd-120">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="22dfd-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="22dfd-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="22dfd-121">-VirtualNetwork</span></span>
<span data-ttu-id="22dfd-122">Azure API Management 部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="22dfd-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="22dfd-123">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="22dfd-123">Default value is $null.</span></span>

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

### <span data-ttu-id="22dfd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dfd-124">CommonParameters</span></span>
<span data-ttu-id="22dfd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22dfd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dfd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22dfd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dfd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="22dfd-127">INPUTS</span></span>

### <span data-ttu-id="22dfd-128">所有</span><span class="sxs-lookup"><span data-stu-id="22dfd-128">None</span></span>
<span data-ttu-id="22dfd-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="22dfd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22dfd-130">輸出</span><span class="sxs-lookup"><span data-stu-id="22dfd-130">OUTPUTS</span></span>

### <span data-ttu-id="22dfd-131">PsApiManagementRegion 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="22dfd-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="22dfd-132">筆記</span><span class="sxs-lookup"><span data-stu-id="22dfd-132">NOTES</span></span>

## <span data-ttu-id="22dfd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="22dfd-133">RELATED LINKS</span></span>

