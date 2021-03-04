---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: e03e14a3327f0e3eaf91131208653bbaaa2fc0c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905350"
---
# <span data-ttu-id="5d096-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d096-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="5d096-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d096-102">SYNOPSIS</span></span>
<span data-ttu-id="5d096-103">使用 ResourceGroupName 和 GatewayName 獲得 VpnGateway 資源，或按 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="5d096-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5d096-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d096-104">SYNTAX</span></span>

### <span data-ttu-id="5d096-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="5d096-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d096-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d096-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d096-107">描述</span><span class="sxs-lookup"><span data-stu-id="5d096-107">DESCRIPTION</span></span>
<span data-ttu-id="5d096-108">使用 ResourceGroupName 和 GatewayName 獲得 VpnGateway 資源，或按 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="5d096-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5d096-109">例子</span><span class="sxs-lookup"><span data-stu-id="5d096-109">EXAMPLES</span></span>

### <span data-ttu-id="5d096-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5d096-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5d096-111">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="5d096-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5d096-112">在此之後，將會以 2 個縮放單位在虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="5d096-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5d096-113">然後，它會使用其 resourceGroupName 和閘道名稱來獲得 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="5d096-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="5d096-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="5d096-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5d096-115">此 Cmdlet 會獲得以「測試」開始的所有閘道。</span><span class="sxs-lookup"><span data-stu-id="5d096-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="5d096-116">參數</span><span class="sxs-lookup"><span data-stu-id="5d096-116">PARAMETERS</span></span>

### <span data-ttu-id="5d096-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d096-117">-DefaultProfile</span></span>
<span data-ttu-id="5d096-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d096-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d096-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d096-119">-Name</span></span>
<span data-ttu-id="5d096-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5d096-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5d096-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d096-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d096-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5d096-122">The resource group name.</span></span>

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

### <span data-ttu-id="5d096-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d096-123">CommonParameters</span></span>
<span data-ttu-id="5d096-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d096-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d096-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d096-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d096-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5d096-126">INPUTS</span></span>

### <span data-ttu-id="5d096-127">沒有</span><span class="sxs-lookup"><span data-stu-id="5d096-127">None</span></span>

## <span data-ttu-id="5d096-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5d096-128">OUTPUTS</span></span>

### <span data-ttu-id="5d096-129">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d096-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="5d096-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5d096-130">NOTES</span></span>

## <span data-ttu-id="5d096-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d096-131">RELATED LINKS</span></span>

[<span data-ttu-id="5d096-132">New-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d096-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="5d096-133">Remove-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d096-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="5d096-134">Update-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5d096-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
