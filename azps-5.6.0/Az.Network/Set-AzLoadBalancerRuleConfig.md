---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 28f71cfe18b344c1e0fbccb632e87a19cf6e8075
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915306"
---
# <span data-ttu-id="9b64e-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="9b64e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b64e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b64e-103">更新負載平衡器的規則組。</span><span class="sxs-lookup"><span data-stu-id="9b64e-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9b64e-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b64e-104">SYNTAX</span></span>

### <span data-ttu-id="9b64e-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9b64e-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b64e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b64e-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b64e-107">描述</span><span class="sxs-lookup"><span data-stu-id="9b64e-107">DESCRIPTION</span></span>
<span data-ttu-id="9b64e-108">**Set-AzLoadBalancerRuleConfig** Cmdlet 會更新負載平衡器的規則設定。</span><span class="sxs-lookup"><span data-stu-id="9b64e-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9b64e-109">例子</span><span class="sxs-lookup"><span data-stu-id="9b64e-109">EXAMPLES</span></span>

### <span data-ttu-id="9b64e-110">範例 1：修改負載平衡規則組</span><span class="sxs-lookup"><span data-stu-id="9b64e-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="9b64e-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在$slb變數中。</span><span class="sxs-lookup"><span data-stu-id="9b64e-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9b64e-112">第二個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerRuleConfig，這會將名為 NewRule 的規則新增到其中。</span><span class="sxs-lookup"><span data-stu-id="9b64e-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="9b64e-113">第三個命令會將負載平衡器傳遞至 **Set-AzLoadBalancerRuleConfig，** 以設定新的規則設定。</span><span class="sxs-lookup"><span data-stu-id="9b64e-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="9b64e-114">請注意，此組配置不會啟用由上一個命令啟用的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9b64e-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="9b64e-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b64e-115">PARAMETERS</span></span>

### <span data-ttu-id="9b64e-116">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="9b64e-116">-BackendAddressPool</span></span>
<span data-ttu-id="9b64e-117">指定 **要與負載平衡器規則關聯的後端AddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b64e-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="9b64e-118">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9b64e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="9b64e-119">指定要與負載 **平衡器規則群組原則關聯的後端AddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b64e-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-120">-後端埠</span><span class="sxs-lookup"><span data-stu-id="9b64e-120">-BackendPort</span></span>
<span data-ttu-id="9b64e-121">指定符合此規則組配置的流量後端埠。</span><span class="sxs-lookup"><span data-stu-id="9b64e-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b64e-122">-DefaultProfile</span></span>
<span data-ttu-id="9b64e-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b64e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b64e-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="9b64e-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="9b64e-125">為後端集區中的虛擬機器設定 SNAT，以使用負載平衡規則前端指定的公用IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9b64e-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="9b64e-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9b64e-126">-EnableFloatingIP</span></span>
<span data-ttu-id="9b64e-127">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9b64e-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9b64e-128">-EnableTcpReset</span></span>
<span data-ttu-id="9b64e-129">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="9b64e-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9b64e-130">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="9b64e-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9b64e-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b64e-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9b64e-132">指定要與負載平衡器規則群組原則關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="9b64e-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9b64e-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9b64e-134">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b64e-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9b64e-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9b64e-135">-FrontendPort</span></span>
<span data-ttu-id="9b64e-136">指定與負載平衡器規則組配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="9b64e-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9b64e-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9b64e-138">指定在負載平衡器中維護交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="9b64e-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9b64e-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b64e-139">-LoadBalancer</span></span>
<span data-ttu-id="9b64e-140">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="9b64e-140">Specifies a load balancer.</span></span>
<span data-ttu-id="9b64e-141">此 Cmdlet 會更新此參數指定的負載平衡器規則設定。</span><span class="sxs-lookup"><span data-stu-id="9b64e-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b64e-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="9b64e-142">-LoadDistribution</span></span>
<span data-ttu-id="9b64e-143">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="9b64e-143">Specifies a load distribution.</span></span>
<span data-ttu-id="9b64e-144">此參數可接受的值為：SourceIP 和 SourceIPProtocol。</span><span class="sxs-lookup"><span data-stu-id="9b64e-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="9b64e-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b64e-145">-Name</span></span>
<span data-ttu-id="9b64e-146">指定負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b64e-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="9b64e-147">-進位</span><span class="sxs-lookup"><span data-stu-id="9b64e-147">-Probe</span></span>
<span data-ttu-id="9b64e-148">指定與負載平衡器規則組配置的關聯。</span><span class="sxs-lookup"><span data-stu-id="9b64e-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-149">-一維Id</span><span class="sxs-lookup"><span data-stu-id="9b64e-149">-ProbeId</span></span>
<span data-ttu-id="9b64e-150">指定要與負載平衡器規則組式關聯的探索識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b64e-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9b64e-151">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9b64e-151">-Protocol</span></span>
<span data-ttu-id="9b64e-152">指定負載平衡器規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9b64e-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="9b64e-153">此參數可接受的值為：Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="9b64e-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="9b64e-154">-確認</span><span class="sxs-lookup"><span data-stu-id="9b64e-154">-Confirm</span></span>
<span data-ttu-id="9b64e-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9b64e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b64e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b64e-156">-WhatIf</span></span>
<span data-ttu-id="9b64e-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b64e-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b64e-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b64e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b64e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b64e-159">CommonParameters</span></span>
<span data-ttu-id="9b64e-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b64e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b64e-161">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9b64e-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b64e-162">輸入</span><span class="sxs-lookup"><span data-stu-id="9b64e-162">INPUTS</span></span>

### <span data-ttu-id="9b64e-163">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b64e-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9b64e-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9b64e-164">System.String</span></span>

### <span data-ttu-id="9b64e-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9b64e-165">System.Int32</span></span>

### <span data-ttu-id="9b64e-166">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b64e-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="9b64e-167">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9b64e-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="9b64e-168">Microsoft.Azure.Commands.Network.models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="9b64e-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="9b64e-169">輸出</span><span class="sxs-lookup"><span data-stu-id="9b64e-169">OUTPUTS</span></span>

### <span data-ttu-id="9b64e-170">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b64e-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9b64e-171">筆記</span><span class="sxs-lookup"><span data-stu-id="9b64e-171">NOTES</span></span>

## <span data-ttu-id="9b64e-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b64e-172">RELATED LINKS</span></span>

[<span data-ttu-id="9b64e-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9b64e-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9b64e-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9b64e-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="9b64e-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b64e-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


