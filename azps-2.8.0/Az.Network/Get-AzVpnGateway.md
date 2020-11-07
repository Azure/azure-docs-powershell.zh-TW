---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789453"
---
# <span data-ttu-id="0adec-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0adec-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="0adec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0adec-102">SYNOPSIS</span></span>
<span data-ttu-id="0adec-103">使用 ResourceGroupName 和 GatewayName 取得 VpnGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="0adec-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="0adec-104">句法</span><span class="sxs-lookup"><span data-stu-id="0adec-104">SYNTAX</span></span>

### <span data-ttu-id="0adec-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="0adec-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0adec-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adec-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0adec-107">說明</span><span class="sxs-lookup"><span data-stu-id="0adec-107">DESCRIPTION</span></span>
<span data-ttu-id="0adec-108">使用 ResourceGroupName 和 GatewayName 取得 VpnGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="0adec-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="0adec-109">示例</span><span class="sxs-lookup"><span data-stu-id="0adec-109">EXAMPLES</span></span>

### <span data-ttu-id="0adec-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0adec-110">Example 1</span></span>

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
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="0adec-111">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="0adec-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="0adec-112">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="0adec-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="0adec-113">然後它會使用其 resourceGroupName 和閘道名稱取得 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="0adec-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="0adec-114">範例2</span><span class="sxs-lookup"><span data-stu-id="0adec-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="0adec-115">這個 Cmdlet 會取得以「test」開頭的所有閘道。</span><span class="sxs-lookup"><span data-stu-id="0adec-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="0adec-116">參數</span><span class="sxs-lookup"><span data-stu-id="0adec-116">PARAMETERS</span></span>

### <span data-ttu-id="0adec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adec-117">-DefaultProfile</span></span>
<span data-ttu-id="0adec-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0adec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0adec-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0adec-119">-Name</span></span>
<span data-ttu-id="0adec-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0adec-120">The resource name.</span></span>

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

### <span data-ttu-id="0adec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adec-121">-ResourceGroupName</span></span>
<span data-ttu-id="0adec-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0adec-122">The resource group name.</span></span>

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

### <span data-ttu-id="0adec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adec-123">CommonParameters</span></span>
<span data-ttu-id="0adec-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0adec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adec-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0adec-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adec-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0adec-126">INPUTS</span></span>

### <span data-ttu-id="0adec-127">所有</span><span class="sxs-lookup"><span data-stu-id="0adec-127">None</span></span>

## <span data-ttu-id="0adec-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0adec-128">OUTPUTS</span></span>

### <span data-ttu-id="0adec-129">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0adec-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="0adec-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0adec-130">NOTES</span></span>

## <span data-ttu-id="0adec-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0adec-131">RELATED LINKS</span></span>

[<span data-ttu-id="0adec-132">新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0adec-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="0adec-133">移除-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0adec-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="0adec-134">更新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0adec-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
