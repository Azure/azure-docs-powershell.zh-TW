---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450225"
---
# <span data-ttu-id="f3c43-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f3c43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3c43-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c43-103">設定負載平衡器規則配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c43-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c43-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3c43-104">SYNTAX</span></span>

### <span data-ttu-id="f3c43-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f3c43-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c43-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c43-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c43-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3c43-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c43-108">**AzureRmLoadBalancerRuleConfig** Cmdlet 會設定負載平衡器規則配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f3c43-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="f3c43-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3c43-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c43-110">範例1：修改負載平衡規則配置</span><span class="sxs-lookup"><span data-stu-id="f3c43-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="f3c43-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="f3c43-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f3c43-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerRuleConfig，這會將名為 NewRule 的規則新增至它。</span><span class="sxs-lookup"><span data-stu-id="f3c43-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="f3c43-113">第三個命令會將負載平衡器傳遞至 AzureRmLoadBalancerRuleConfig，這會設定新的規則 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="f3c43-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="f3c43-114">請注意，此設定不會啟用 [浮動 IP 位址]，這是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="f3c43-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="f3c43-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3c43-115">PARAMETERS</span></span>

### <span data-ttu-id="f3c43-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f3c43-116">-BackendAddressPool</span></span>
<span data-ttu-id="f3c43-117">指定要與負載平衡器規則相關聯的 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="f3c43-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="f3c43-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f3c43-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f3c43-119">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c43-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f3c43-120">-BackendPort</span></span>
<span data-ttu-id="f3c43-121">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="f3c43-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c43-122">-DefaultProfile</span></span>
<span data-ttu-id="f3c43-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3c43-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c43-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="f3c43-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="f3c43-125">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="f3c43-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="f3c43-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f3c43-126">-EnableFloatingIP</span></span>
<span data-ttu-id="f3c43-127">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f3c43-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f3c43-128">-EnableTcpReset</span></span>
<span data-ttu-id="f3c43-129">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="f3c43-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f3c43-130">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="f3c43-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f3c43-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c43-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f3c43-132">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="f3c43-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f3c43-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f3c43-134">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="f3c43-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f3c43-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f3c43-135">-FrontendPort</span></span>
<span data-ttu-id="f3c43-136">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="f3c43-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f3c43-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f3c43-138">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3c43-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f3c43-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3c43-139">-LoadBalancer</span></span>
<span data-ttu-id="f3c43-140">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f3c43-140">Specifies a load balancer.</span></span>
<span data-ttu-id="f3c43-141">這個 Cmdlet 會針對此參數指定的負載平衡器設定目標狀態規則配置。</span><span class="sxs-lookup"><span data-stu-id="f3c43-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f3c43-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="f3c43-142">-LoadDistribution</span></span>
<span data-ttu-id="f3c43-143">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="f3c43-143">Specifies a load distribution.</span></span>
<span data-ttu-id="f3c43-144">此參數可接受的值為： SourceIP 和 SourceIPProtocol。</span><span class="sxs-lookup"><span data-stu-id="f3c43-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="f3c43-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3c43-145">-Name</span></span>
<span data-ttu-id="f3c43-146">指定負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c43-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="f3c43-147">探測器</span><span class="sxs-lookup"><span data-stu-id="f3c43-147">-Probe</span></span>
<span data-ttu-id="f3c43-148">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="f3c43-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f3c43-149">-ProbeId</span></span>
<span data-ttu-id="f3c43-150">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c43-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f3c43-151">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f3c43-151">-Protocol</span></span>
<span data-ttu-id="f3c43-152">指定由負載等化器規則所相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f3c43-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="f3c43-153">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="f3c43-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f3c43-154">-確認</span><span class="sxs-lookup"><span data-stu-id="f3c43-154">-Confirm</span></span>
<span data-ttu-id="f3c43-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3c43-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c43-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c43-156">-WhatIf</span></span>
<span data-ttu-id="f3c43-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3c43-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3c43-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c43-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c43-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c43-159">CommonParameters</span></span>
<span data-ttu-id="f3c43-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3c43-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c43-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3c43-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c43-162">輸入</span><span class="sxs-lookup"><span data-stu-id="f3c43-162">INPUTS</span></span>

### <span data-ttu-id="f3c43-163">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3c43-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="f3c43-164">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f3c43-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="f3c43-165">輸出</span><span class="sxs-lookup"><span data-stu-id="f3c43-165">OUTPUTS</span></span>

### <span data-ttu-id="f3c43-166">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3c43-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f3c43-167">筆記</span><span class="sxs-lookup"><span data-stu-id="f3c43-167">NOTES</span></span>

## <span data-ttu-id="f3c43-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3c43-168">RELATED LINKS</span></span>

[<span data-ttu-id="f3c43-169">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f3c43-170">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f3c43-171">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f3c43-172">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f3c43-173">移除-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3c43-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


