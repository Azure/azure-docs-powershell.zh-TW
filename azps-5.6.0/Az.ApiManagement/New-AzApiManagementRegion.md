---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 5a0348c4aa55fd6ef381806be9b0ecc924ed8d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906354"
---
# <span data-ttu-id="eb22e-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb22e-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="eb22e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb22e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb22e-103">建立 PsApiManagementRegion 的實例。</span><span class="sxs-lookup"><span data-stu-id="eb22e-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="eb22e-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb22e-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb22e-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb22e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb22e-106">建立 PsApiManagementRegion 實例的協助程式命令。</span><span class="sxs-lookup"><span data-stu-id="eb22e-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="eb22e-107">此命令會與命令一New-AzApiManagement使用。</span><span class="sxs-lookup"><span data-stu-id="eb22e-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="eb22e-108">例子</span><span class="sxs-lookup"><span data-stu-id="eb22e-108">EXAMPLES</span></span>

### <span data-ttu-id="eb22e-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="eb22e-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="eb22e-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="eb22e-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="eb22e-111">在西部美國地區建立 External VpnType 的 ApiManagement 服務，美國中還有一個額外的地區。</span><span class="sxs-lookup"><span data-stu-id="eb22e-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="eb22e-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb22e-112">PARAMETERS</span></span>

### <span data-ttu-id="eb22e-113">-容量</span><span class="sxs-lookup"><span data-stu-id="eb22e-113">-Capacity</span></span>
<span data-ttu-id="eb22e-114">Azure API 管理服務額外地區的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="eb22e-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="eb22e-115">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="eb22e-115">Default value is 1.</span></span>

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

### <span data-ttu-id="eb22e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb22e-116">-DefaultProfile</span></span>
<span data-ttu-id="eb22e-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb22e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb22e-118">-位置</span><span class="sxs-lookup"><span data-stu-id="eb22e-118">-Location</span></span>
<span data-ttu-id="eb22e-119">指定 Api 管理服務支援區域之間的新部署區域位置。</span><span class="sxs-lookup"><span data-stu-id="eb22e-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="eb22e-120">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" |其中 {$_.ResourceTypes[0]。ResourceTypeName -eq "service"} |Select-Object位置</span><span class="sxs-lookup"><span data-stu-id="eb22e-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="eb22e-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb22e-121">-VirtualNetwork</span></span>
<span data-ttu-id="eb22e-122">Azure API 管理部署地區的虛擬網路組配置。</span><span class="sxs-lookup"><span data-stu-id="eb22e-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="eb22e-123">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="eb22e-123">Default value is $null.</span></span>

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

### <span data-ttu-id="eb22e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb22e-124">CommonParameters</span></span>
<span data-ttu-id="eb22e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb22e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb22e-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb22e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb22e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="eb22e-127">INPUTS</span></span>

### <span data-ttu-id="eb22e-128">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb22e-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="eb22e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="eb22e-129">OUTPUTS</span></span>

### <span data-ttu-id="eb22e-130">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb22e-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="eb22e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="eb22e-131">NOTES</span></span>

## <span data-ttu-id="eb22e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb22e-132">RELATED LINKS</span></span>
