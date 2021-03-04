---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: d4f0b908a229ee47472d40eefe60c5771c0147d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910014"
---
# <span data-ttu-id="2f67a-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="2f67a-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="2f67a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f67a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f67a-103">在 VpnGateway 上建立可以與 VpnSiteLinkConnection 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="2f67a-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="2f67a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f67a-104">SYNTAX</span></span>

### <span data-ttu-id="2f67a-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="2f67a-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f67a-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2f67a-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f67a-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2f67a-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f67a-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f67a-108">DESCRIPTION</span></span>
<span data-ttu-id="2f67a-109">在 VpnGateway 上建立可以與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="2f67a-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="2f67a-110">例子</span><span class="sxs-lookup"><span data-stu-id="2f67a-110">EXAMPLES</span></span>

### <span data-ttu-id="2f67a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f67a-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="2f67a-112">上述將建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="2f67a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="2f67a-113">接著，我們將建立虛擬中樞下的 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="2f67a-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="2f67a-114">然後，使用此命令：New-Az VpnGatewayNatRule，NAT 規則可以建立，並與已建立 VpnGateway 相關聯。</span><span class="sxs-lookup"><span data-stu-id="2f67a-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="2f67a-115">參數</span><span class="sxs-lookup"><span data-stu-id="2f67a-115">PARAMETERS</span></span>

### <span data-ttu-id="2f67a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f67a-116">-AsJob</span></span>
<span data-ttu-id="2f67a-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f67a-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f67a-118">-DefaultProfile</span></span>
<span data-ttu-id="2f67a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f67a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f67a-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="2f67a-120">-ExternalMapping</span></span>
<span data-ttu-id="2f67a-121">NAT 的私人 IP 位址子網外部地圖清單</span><span class="sxs-lookup"><span data-stu-id="2f67a-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-122">-內部Mapping</span><span class="sxs-lookup"><span data-stu-id="2f67a-122">-InternalMapping</span></span>
<span data-ttu-id="2f67a-123">NAT 的私人 IP 位址子網內部地圖清單</span><span class="sxs-lookup"><span data-stu-id="2f67a-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2f67a-124">-IpConfigurationId</span></span>
<span data-ttu-id="2f67a-125">此 NAT 規則所適用的 IP 組組識別碼</span><span class="sxs-lookup"><span data-stu-id="2f67a-125">The IP Configuration ID this NAT rule applies to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-126">-模式</span><span class="sxs-lookup"><span data-stu-id="2f67a-126">-Mode</span></span>
<span data-ttu-id="2f67a-127">VPN NAT 的來源 NAT 方向</span><span class="sxs-lookup"><span data-stu-id="2f67a-127">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f67a-128">-Name</span></span>
<span data-ttu-id="2f67a-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2f67a-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2f67a-130">-ParentObject</span></span>
<span data-ttu-id="2f67a-131">此 NAT 規則的父 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="2f67a-131">The parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f67a-132">-ParentResourceId</span></span>
<span data-ttu-id="2f67a-133">此 NAT 規則之父 VpnGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f67a-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="2f67a-134">-ParentResourceName</span></span>
<span data-ttu-id="2f67a-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f67a-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f67a-136">-ResourceGroupName</span></span>
<span data-ttu-id="2f67a-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f67a-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-138">-類型</span><span class="sxs-lookup"><span data-stu-id="2f67a-138">-Type</span></span>
<span data-ttu-id="2f67a-139">VPN NAT 的 NAT 規則類型</span><span class="sxs-lookup"><span data-stu-id="2f67a-139">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-140">-確認</span><span class="sxs-lookup"><span data-stu-id="2f67a-140">-Confirm</span></span>
<span data-ttu-id="2f67a-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f67a-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f67a-142">-WhatIf</span></span>
<span data-ttu-id="2f67a-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f67a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f67a-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f67a-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f67a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f67a-145">CommonParameters</span></span>
<span data-ttu-id="2f67a-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f67a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f67a-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f67a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f67a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="2f67a-148">INPUTS</span></span>

### <span data-ttu-id="2f67a-149">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="2f67a-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2f67a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2f67a-150">System.String</span></span>

## <span data-ttu-id="2f67a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="2f67a-151">OUTPUTS</span></span>

### <span data-ttu-id="2f67a-152">Microsoft.Azure.Commands.Network.models.PS VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="2f67a-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="2f67a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="2f67a-153">NOTES</span></span>

## <span data-ttu-id="2f67a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f67a-154">RELATED LINKS</span></span>
