---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127506"
---
# <span data-ttu-id="627a9-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627a9-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="627a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="627a9-102">SYNOPSIS</span></span>
<span data-ttu-id="627a9-103">為負載平衡器建立規則配置。</span><span class="sxs-lookup"><span data-stu-id="627a9-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="627a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="627a9-104">SYNTAX</span></span>

### <span data-ttu-id="627a9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="627a9-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627a9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="627a9-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="627a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="627a9-107">DESCRIPTION</span></span>
<span data-ttu-id="627a9-108">**新的-AzLoadBalancerRuleConfig** Cmdlet 會建立 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="627a9-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="627a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="627a9-109">EXAMPLES</span></span>

### <span data-ttu-id="627a9-110">範例1：建立 Azure 負載平衡器的規則配置</span><span class="sxs-lookup"><span data-stu-id="627a9-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="627a9-111">前三個命令會在下一個命令中設定公用 IP、前端及規則配置的探測。</span><span class="sxs-lookup"><span data-stu-id="627a9-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="627a9-112">向下的命令會建立一個名為 MyLBrule 的新規則，並提供特定的規格。</span><span class="sxs-lookup"><span data-stu-id="627a9-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="627a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="627a9-113">PARAMETERS</span></span>

### <span data-ttu-id="627a9-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="627a9-114">-BackendAddressPool</span></span>
<span data-ttu-id="627a9-115">指定要與負載平衡器規則配置相關聯的 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="627a9-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="627a9-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="627a9-117">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="627a9-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="627a9-118">-BackendPort</span></span>
<span data-ttu-id="627a9-119">指定此負載平衡器規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="627a9-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627a9-120">-DefaultProfile</span></span>
<span data-ttu-id="627a9-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="627a9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627a9-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="627a9-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="627a9-123">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="627a9-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="627a9-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="627a9-124">-EnableFloatingIP</span></span>
<span data-ttu-id="627a9-125">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="627a9-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="627a9-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="627a9-126">-EnableTcpReset</span></span>
<span data-ttu-id="627a9-127">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="627a9-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="627a9-128">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="627a9-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="627a9-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="627a9-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="627a9-130">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="627a9-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="627a9-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="627a9-132">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="627a9-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="627a9-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="627a9-133">-FrontendPort</span></span>
<span data-ttu-id="627a9-134">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="627a9-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="627a9-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="627a9-136">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="627a9-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="627a9-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="627a9-137">-LoadDistribution</span></span>
<span data-ttu-id="627a9-138">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="627a9-138">Specifies a load distribution.</span></span>
<span data-ttu-id="627a9-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="627a9-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="627a9-140">設置</span><span class="sxs-lookup"><span data-stu-id="627a9-140">Default</span></span>
- <span data-ttu-id="627a9-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="627a9-141">SourceIP</span></span>
- <span data-ttu-id="627a9-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="627a9-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="627a9-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="627a9-143">-Name</span></span>
<span data-ttu-id="627a9-144">指定此 Cmdlet 所建立之負載平衡規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="627a9-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="627a9-145">探測器</span><span class="sxs-lookup"><span data-stu-id="627a9-145">-Probe</span></span>
<span data-ttu-id="627a9-146">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="627a9-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="627a9-147">-ProbeId</span></span>
<span data-ttu-id="627a9-148">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="627a9-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="627a9-149">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="627a9-149">-Protocol</span></span>
<span data-ttu-id="627a9-150">指定與負載平衡器規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="627a9-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="627a9-151">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="627a9-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="627a9-152">-確認</span><span class="sxs-lookup"><span data-stu-id="627a9-152">-Confirm</span></span>
<span data-ttu-id="627a9-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="627a9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="627a9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="627a9-154">-WhatIf</span></span>
<span data-ttu-id="627a9-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="627a9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="627a9-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="627a9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="627a9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627a9-157">CommonParameters</span></span>
<span data-ttu-id="627a9-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="627a9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627a9-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="627a9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627a9-160">輸入</span><span class="sxs-lookup"><span data-stu-id="627a9-160">INPUTS</span></span>

### <span data-ttu-id="627a9-161">System.object</span><span class="sxs-lookup"><span data-stu-id="627a9-161">System.String</span></span>

### <span data-ttu-id="627a9-162">System.object</span><span class="sxs-lookup"><span data-stu-id="627a9-162">System.Int32</span></span>

### <span data-ttu-id="627a9-163">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="627a9-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="627a9-164">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="627a9-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="627a9-165">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="627a9-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="627a9-166">輸出</span><span class="sxs-lookup"><span data-stu-id="627a9-166">OUTPUTS</span></span>

### <span data-ttu-id="627a9-167">PSLoadBalancingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="627a9-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="627a9-168">筆記</span><span class="sxs-lookup"><span data-stu-id="627a9-168">NOTES</span></span>

## <span data-ttu-id="627a9-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="627a9-169">RELATED LINKS</span></span>

[<span data-ttu-id="627a9-170">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627a9-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="627a9-171">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627a9-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="627a9-172">移除-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627a9-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="627a9-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="627a9-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


