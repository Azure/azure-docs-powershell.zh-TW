---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 11baabe406180e92a4a6af0f62b5e3b285e016b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790486"
---
# <span data-ttu-id="0f6f7-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0f6f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6f7-103">更新負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0f6f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f6f7-104">SYNTAX</span></span>

### <span data-ttu-id="0f6f7-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0f6f7-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6f7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6f7-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="0f6f7-107">DESCRIPTION</span></span>
<span data-ttu-id="0f6f7-108">**AzLoadBalancerRuleConfig** Cmdlet 會更新負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0f6f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="0f6f7-109">EXAMPLES</span></span>

### <span data-ttu-id="0f6f7-110">範例1：修改負載平衡規則配置</span><span class="sxs-lookup"><span data-stu-id="0f6f7-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="0f6f7-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="0f6f7-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerRuleConfig，這會將名為 NewRule 的規則新增至它。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="0f6f7-113">第三個命令會將負載平衡器傳遞至 AzLoadBalancerRuleConfig，這會設定新的規則 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="0f6f7-114">請注意，此設定不會啟用 [浮動 IP 位址]，這是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="0f6f7-115">參數</span><span class="sxs-lookup"><span data-stu-id="0f6f7-115">PARAMETERS</span></span>

### <span data-ttu-id="0f6f7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f6f7-116">-BackendAddressPool</span></span>
<span data-ttu-id="0f6f7-117">指定要與負載平衡器規則相關聯的 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="0f6f7-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0f6f7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0f6f7-119">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0f6f7-120">-BackendPort</span></span>
<span data-ttu-id="0f6f7-121">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6f7-122">-DefaultProfile</span></span>
<span data-ttu-id="0f6f7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f6f7-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="0f6f7-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="0f6f7-125">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="0f6f7-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0f6f7-126">-EnableFloatingIP</span></span>
<span data-ttu-id="0f6f7-127">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0f6f7-128">-EnableTcpReset</span></span>
<span data-ttu-id="0f6f7-129">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0f6f7-130">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0f6f7-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f6f7-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0f6f7-132">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0f6f7-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0f6f7-134">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0f6f7-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0f6f7-135">-FrontendPort</span></span>
<span data-ttu-id="0f6f7-136">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0f6f7-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0f6f7-138">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0f6f7-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f6f7-139">-LoadBalancer</span></span>
<span data-ttu-id="0f6f7-140">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-140">Specifies a load balancer.</span></span>
<span data-ttu-id="0f6f7-141">這個 Cmdlet 會針對此參數指定的負載平衡器更新規則設定。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f6f7-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="0f6f7-142">-LoadDistribution</span></span>
<span data-ttu-id="0f6f7-143">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-143">Specifies a load distribution.</span></span>
<span data-ttu-id="0f6f7-144">此參數可接受的值為： SourceIP 和 SourceIPProtocol。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="0f6f7-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f6f7-145">-Name</span></span>
<span data-ttu-id="0f6f7-146">指定負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="0f6f7-147">探測器</span><span class="sxs-lookup"><span data-stu-id="0f6f7-147">-Probe</span></span>
<span data-ttu-id="0f6f7-148">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="0f6f7-149">-ProbeId</span></span>
<span data-ttu-id="0f6f7-150">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f6f7-151">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0f6f7-151">-Protocol</span></span>
<span data-ttu-id="0f6f7-152">指定由負載等化器規則所相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="0f6f7-153">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0f6f7-154">-確認</span><span class="sxs-lookup"><span data-stu-id="0f6f7-154">-Confirm</span></span>
<span data-ttu-id="0f6f7-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6f7-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6f7-156">-WhatIf</span></span>
<span data-ttu-id="0f6f7-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f6f7-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6f7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6f7-159">CommonParameters</span></span>
<span data-ttu-id="0f6f7-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6f7-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f6f7-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6f7-162">輸入</span><span class="sxs-lookup"><span data-stu-id="0f6f7-162">INPUTS</span></span>

### <span data-ttu-id="0f6f7-163">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f6f7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0f6f7-164">System.object</span><span class="sxs-lookup"><span data-stu-id="0f6f7-164">System.String</span></span>

### <span data-ttu-id="0f6f7-165">System.object</span><span class="sxs-lookup"><span data-stu-id="0f6f7-165">System.Int32</span></span>

### <span data-ttu-id="0f6f7-166">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f6f7-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="0f6f7-167">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f6f7-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="0f6f7-168">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f6f7-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="0f6f7-169">輸出</span><span class="sxs-lookup"><span data-stu-id="0f6f7-169">OUTPUTS</span></span>

### <span data-ttu-id="0f6f7-170">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0f6f7-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f6f7-171">筆記</span><span class="sxs-lookup"><span data-stu-id="0f6f7-171">NOTES</span></span>

## <span data-ttu-id="0f6f7-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f6f7-172">RELATED LINKS</span></span>

[<span data-ttu-id="0f6f7-173">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0f6f7-174">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0f6f7-175">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0f6f7-176">新-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0f6f7-177">移除-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f6f7-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

