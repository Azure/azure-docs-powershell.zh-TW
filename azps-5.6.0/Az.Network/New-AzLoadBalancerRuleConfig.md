---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 544d43ab3a82ff7eb00712ea121d3f799d632f79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912357"
---
# <span data-ttu-id="9300b-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9300b-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="9300b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9300b-102">SYNOPSIS</span></span>
<span data-ttu-id="9300b-103">建立負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="9300b-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9300b-104">語法</span><span class="sxs-lookup"><span data-stu-id="9300b-104">SYNTAX</span></span>

### <span data-ttu-id="9300b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9300b-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9300b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9300b-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9300b-107">描述</span><span class="sxs-lookup"><span data-stu-id="9300b-107">DESCRIPTION</span></span>
<span data-ttu-id="9300b-108">**New-AzLoadBalancerRuleConfig** Cmdlet 會建立 Azure 負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="9300b-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9300b-109">例子</span><span class="sxs-lookup"><span data-stu-id="9300b-109">EXAMPLES</span></span>

### <span data-ttu-id="9300b-110">範例 1：建立 Azure 負載平衡器的規則組</span><span class="sxs-lookup"><span data-stu-id="9300b-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="9300b-111">前三個命令會針對第四個命令中的規則設定設定公用 IP、前端和設定。</span><span class="sxs-lookup"><span data-stu-id="9300b-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="9300b-112">第四個命令會建立一個稱為 MyLBrule 的新規則，具有特定規格。</span><span class="sxs-lookup"><span data-stu-id="9300b-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="9300b-113">參數</span><span class="sxs-lookup"><span data-stu-id="9300b-113">PARAMETERS</span></span>

### <span data-ttu-id="9300b-114">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="9300b-114">-BackendAddressPool</span></span>
<span data-ttu-id="9300b-115">指定 **要與負載平衡器規則群組原則關聯的後端AddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="9300b-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-116">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9300b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="9300b-117">指定要與負載 **平衡器規則群組原則關聯的後端AddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9300b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-118">-後端埠</span><span class="sxs-lookup"><span data-stu-id="9300b-118">-BackendPort</span></span>
<span data-ttu-id="9300b-119">指定此負載平衡器規則組配置相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="9300b-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9300b-120">-DefaultProfile</span></span>
<span data-ttu-id="9300b-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9300b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9300b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="9300b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="9300b-123">為後端集區中的虛擬機器設定 SNAT，以使用負載平衡規則前端指定的公用IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9300b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="9300b-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9300b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="9300b-125">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9300b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9300b-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9300b-126">-EnableTcpReset</span></span>
<span data-ttu-id="9300b-127">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="9300b-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9300b-128">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="9300b-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9300b-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9300b-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9300b-130">指定要與負載平衡器規則群組原則關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="9300b-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9300b-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9300b-132">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9300b-132">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9300b-133">-FrontendPort</span></span>
<span data-ttu-id="9300b-134">指定與負載平衡器規則組配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="9300b-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9300b-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9300b-136">指定在負載平衡器中維持交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="9300b-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="9300b-137">-LoadDistribution</span></span>
<span data-ttu-id="9300b-138">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="9300b-138">Specifies a load distribution.</span></span>
<span data-ttu-id="9300b-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9300b-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9300b-140">預設</span><span class="sxs-lookup"><span data-stu-id="9300b-140">Default</span></span>
- <span data-ttu-id="9300b-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="9300b-141">SourceIP</span></span>
- <span data-ttu-id="9300b-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="9300b-142">SourceIPProtocol</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="9300b-143">-Name</span></span>
<span data-ttu-id="9300b-144">指定此 Cmdlet 所建立之負載平衡規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9300b-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9300b-145">-進位</span><span class="sxs-lookup"><span data-stu-id="9300b-145">-Probe</span></span>
<span data-ttu-id="9300b-146">指定與負載平衡器規則組配置的關聯。</span><span class="sxs-lookup"><span data-stu-id="9300b-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-147">-一維Id</span><span class="sxs-lookup"><span data-stu-id="9300b-147">-ProbeId</span></span>
<span data-ttu-id="9300b-148">指定要與負載平衡器規則組式關聯的探索識別碼。</span><span class="sxs-lookup"><span data-stu-id="9300b-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-149">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9300b-149">-Protocol</span></span>
<span data-ttu-id="9300b-150">指定與負載平衡器規則組配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9300b-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="9300b-151">此參數可接受的值為：Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="9300b-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9300b-152">-確認</span><span class="sxs-lookup"><span data-stu-id="9300b-152">-Confirm</span></span>
<span data-ttu-id="9300b-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9300b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9300b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9300b-154">-WhatIf</span></span>
<span data-ttu-id="9300b-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9300b-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9300b-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9300b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9300b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9300b-157">CommonParameters</span></span>
<span data-ttu-id="9300b-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9300b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9300b-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9300b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9300b-160">輸入</span><span class="sxs-lookup"><span data-stu-id="9300b-160">INPUTS</span></span>

### <span data-ttu-id="9300b-161">System.String</span><span class="sxs-lookup"><span data-stu-id="9300b-161">System.String</span></span>

### <span data-ttu-id="9300b-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9300b-162">System.Int32</span></span>

### <span data-ttu-id="9300b-163">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9300b-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="9300b-164">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9300b-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="9300b-165">Microsoft.Azure.Commands.Network.models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="9300b-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="9300b-166">輸出</span><span class="sxs-lookup"><span data-stu-id="9300b-166">OUTPUTS</span></span>

### <span data-ttu-id="9300b-167">Microsoft.Azure.Commands.Network.models.PSLoadBalrule</span><span class="sxs-lookup"><span data-stu-id="9300b-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="9300b-168">筆記</span><span class="sxs-lookup"><span data-stu-id="9300b-168">NOTES</span></span>

## <span data-ttu-id="9300b-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="9300b-169">RELATED LINKS</span></span>

[<span data-ttu-id="9300b-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9300b-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9300b-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9300b-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9300b-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9300b-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9300b-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9300b-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


