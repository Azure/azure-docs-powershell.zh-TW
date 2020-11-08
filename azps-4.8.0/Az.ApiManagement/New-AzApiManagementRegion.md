---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969438"
---
# <span data-ttu-id="8a61d-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8a61d-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="8a61d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a61d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a61d-103">建立 PsApiManagementRegion 的實例。</span><span class="sxs-lookup"><span data-stu-id="8a61d-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="8a61d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a61d-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a61d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a61d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a61d-106">[Helper] 命令來建立 PsApiManagementRegion 的實例。</span><span class="sxs-lookup"><span data-stu-id="8a61d-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="8a61d-107">此命令將與 New-AzApiManagement 命令搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8a61d-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="8a61d-108">示例</span><span class="sxs-lookup"><span data-stu-id="8a61d-108">EXAMPLES</span></span>

### <span data-ttu-id="8a61d-109">範例1</span><span class="sxs-lookup"><span data-stu-id="8a61d-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="8a61d-110">範例2</span><span class="sxs-lookup"><span data-stu-id="8a61d-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="8a61d-111">在 West 美國地區建立外部 VpnType 的 ApiManagement 服務，並在美國中部新增一個區域。</span><span class="sxs-lookup"><span data-stu-id="8a61d-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="8a61d-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a61d-112">PARAMETERS</span></span>

### <span data-ttu-id="8a61d-113">-容量</span><span class="sxs-lookup"><span data-stu-id="8a61d-113">-Capacity</span></span>
<span data-ttu-id="8a61d-114">Azure API Management 服務其他區域的 Sku 容量。</span><span class="sxs-lookup"><span data-stu-id="8a61d-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="8a61d-115">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="8a61d-115">Default value is 1.</span></span>

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

### <span data-ttu-id="8a61d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a61d-116">-DefaultProfile</span></span>
<span data-ttu-id="8a61d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a61d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a61d-118">-位置</span><span class="sxs-lookup"><span data-stu-id="8a61d-118">-Location</span></span>
<span data-ttu-id="8a61d-119">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="8a61d-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="8a61d-120">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="8a61d-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8a61d-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8a61d-121">-VirtualNetwork</span></span>
<span data-ttu-id="8a61d-122">Azure API Management 部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="8a61d-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="8a61d-123">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="8a61d-123">Default value is $null.</span></span>

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

### <span data-ttu-id="8a61d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a61d-124">CommonParameters</span></span>
<span data-ttu-id="8a61d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a61d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a61d-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a61d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a61d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8a61d-127">INPUTS</span></span>

### <span data-ttu-id="8a61d-128">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="8a61d-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="8a61d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8a61d-129">OUTPUTS</span></span>

### <span data-ttu-id="8a61d-130">PsApiManagementRegion 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="8a61d-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="8a61d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8a61d-131">NOTES</span></span>

## <span data-ttu-id="8a61d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a61d-132">RELATED LINKS</span></span>