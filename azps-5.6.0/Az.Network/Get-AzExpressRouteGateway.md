---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 0d7bec7a40ced6ddcd5ffc61f48f233cea115459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916609"
---
# <span data-ttu-id="80092-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="80092-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="80092-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80092-102">SYNOPSIS</span></span>
<span data-ttu-id="80092-103">使用 ResourceGroupName 和 GatewayName 獲得 ExpressRouteGateway 資源，或按 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="80092-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="80092-104">語法</span><span class="sxs-lookup"><span data-stu-id="80092-104">SYNTAX</span></span>

### <span data-ttu-id="80092-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="80092-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80092-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80092-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80092-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="80092-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80092-108">描述</span><span class="sxs-lookup"><span data-stu-id="80092-108">DESCRIPTION</span></span>
<span data-ttu-id="80092-109">使用 ResourceGroupName 和 GatewayName 獲得 ExpressRouteGateway 資源，或按 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="80092-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="80092-110">例子</span><span class="sxs-lookup"><span data-stu-id="80092-110">EXAMPLES</span></span>

### <span data-ttu-id="80092-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="80092-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="80092-112">上述將在 Azure 的 「testRG」 資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="80092-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="80092-113">在此之後，將會以 2 個縮放單位在虛擬中心中建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="80092-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="80092-114">然後，它會使用其 resourceGroupName 和閘道名稱來獲得 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="80092-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="80092-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="80092-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="80092-116">此命令會取得以「測試」開始的所有 ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="80092-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="80092-117">參數</span><span class="sxs-lookup"><span data-stu-id="80092-117">PARAMETERS</span></span>

### <span data-ttu-id="80092-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80092-118">-DefaultProfile</span></span>
<span data-ttu-id="80092-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80092-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80092-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="80092-120">-Name</span></span>
<span data-ttu-id="80092-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="80092-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="80092-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80092-122">-ResourceGroupName</span></span>
<span data-ttu-id="80092-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="80092-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="80092-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80092-124">-ResourceId</span></span>
<span data-ttu-id="80092-125">要刪除 expressRouteGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="80092-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80092-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80092-126">CommonParameters</span></span>
<span data-ttu-id="80092-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80092-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80092-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80092-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80092-129">輸入</span><span class="sxs-lookup"><span data-stu-id="80092-129">INPUTS</span></span>

### <span data-ttu-id="80092-130">System.String</span><span class="sxs-lookup"><span data-stu-id="80092-130">System.String</span></span>

## <span data-ttu-id="80092-131">輸出</span><span class="sxs-lookup"><span data-stu-id="80092-131">OUTPUTS</span></span>

### <span data-ttu-id="80092-132">Microsoft.Azure.Commands.Network.models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="80092-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="80092-133">筆記</span><span class="sxs-lookup"><span data-stu-id="80092-133">NOTES</span></span>

## <span data-ttu-id="80092-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="80092-134">RELATED LINKS</span></span>
