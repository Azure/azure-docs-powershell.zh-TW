---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132414"
---
# <span data-ttu-id="c0e3f-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c0e3f-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="c0e3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e3f-103">更新與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="c0e3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0e3f-104">SYNTAX</span></span>

### <span data-ttu-id="c0e3f-105">ByVpnGatewayNatRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="c0e3f-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0e3f-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3f-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e3f-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="c0e3f-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e3f-108">說明</span><span class="sxs-lookup"><span data-stu-id="c0e3f-108">DESCRIPTION</span></span>
<span data-ttu-id="c0e3f-109">**AzVpnGatewayNatRule** Cmdlet 會更新與 VpnGateway 相關聯的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="c0e3f-110">示例</span><span class="sxs-lookup"><span data-stu-id="c0e3f-110">EXAMPLES</span></span>

### <span data-ttu-id="c0e3f-111">範例</span><span class="sxs-lookup"><span data-stu-id="c0e3f-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
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

<span data-ttu-id="c0e3f-112">上述將會建立資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="c0e3f-113">接著，我們會在該虛擬中樞下建立 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="c0e3f-114">接著，建立與建立的 VpnGateway 相關聯的新 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="c0e3f-115">使用此命令：更新-AzVpnGatewayNatRule、更新 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="c0e3f-116">參數</span><span class="sxs-lookup"><span data-stu-id="c0e3f-116">PARAMETERS</span></span>

### <span data-ttu-id="c0e3f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0e3f-117">-AsJob</span></span>
<span data-ttu-id="c0e3f-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0e3f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0e3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e3f-119">-DefaultProfile</span></span>
<span data-ttu-id="c0e3f-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e3f-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="c0e3f-121">-ExternalMapping</span></span>
<span data-ttu-id="c0e3f-122">NAT 的私人 IP 位址子網外部對應清單</span><span class="sxs-lookup"><span data-stu-id="c0e3f-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e3f-123">-InputObject</span></span>
<span data-ttu-id="c0e3f-124">要更新的 VpnGatewayNatRule 物件。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-124">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="c0e3f-125">-InternalMapping</span></span>
<span data-ttu-id="c0e3f-126">NAT 的私人 IP 位址子網內部鏡像清單</span><span class="sxs-lookup"><span data-stu-id="c0e3f-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c0e3f-127">-IpConfigurationId</span></span>
<span data-ttu-id="c0e3f-128">此 NAT 規則適用的 IP 配置識別碼</span><span class="sxs-lookup"><span data-stu-id="c0e3f-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="c0e3f-129">模式</span><span class="sxs-lookup"><span data-stu-id="c0e3f-129">-Mode</span></span>
<span data-ttu-id="c0e3f-130">VPN NAT 的來源 NAT 方向</span><span class="sxs-lookup"><span data-stu-id="c0e3f-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="c0e3f-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0e3f-131">-Name</span></span>
<span data-ttu-id="c0e3f-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c0e3f-133">-ParentResourceName</span></span>
<span data-ttu-id="c0e3f-134">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-134">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e3f-135">-ResourceGroupName</span></span>
<span data-ttu-id="c0e3f-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3f-137">-ResourceId</span></span>
<span data-ttu-id="c0e3f-138">要刪除之 VpnGatewayNatRule 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-139">-類型</span><span class="sxs-lookup"><span data-stu-id="c0e3f-139">-Type</span></span>
<span data-ttu-id="c0e3f-140">VPN NAT 的 NAT 規則類型</span><span class="sxs-lookup"><span data-stu-id="c0e3f-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="c0e3f-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c0e3f-141">-Confirm</span></span>
<span data-ttu-id="c0e3f-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e3f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e3f-143">-WhatIf</span></span>
<span data-ttu-id="c0e3f-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e3f-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e3f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e3f-146">CommonParameters</span></span>
<span data-ttu-id="c0e3f-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e3f-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e3f-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c0e3f-149">INPUTS</span></span>

### <span data-ttu-id="c0e3f-150">System.object</span><span class="sxs-lookup"><span data-stu-id="c0e3f-150">System.String</span></span>

### <span data-ttu-id="c0e3f-151">PSVpnGatewayNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0e3f-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="c0e3f-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c0e3f-152">OUTPUTS</span></span>

### <span data-ttu-id="c0e3f-153">PSVpnGatewayNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0e3f-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="c0e3f-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c0e3f-154">NOTES</span></span>

## <span data-ttu-id="c0e3f-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0e3f-155">RELATED LINKS</span></span>
