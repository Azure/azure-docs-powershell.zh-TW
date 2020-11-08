---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138490"
---
# <span data-ttu-id="6faec-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6faec-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6faec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6faec-102">SYNOPSIS</span></span>
<span data-ttu-id="6faec-103">在負載平衡器中新增規則配置。</span><span class="sxs-lookup"><span data-stu-id="6faec-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="6faec-104">句法</span><span class="sxs-lookup"><span data-stu-id="6faec-104">SYNTAX</span></span>

### <span data-ttu-id="6faec-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6faec-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6faec-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6faec-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6faec-107">說明</span><span class="sxs-lookup"><span data-stu-id="6faec-107">DESCRIPTION</span></span>
<span data-ttu-id="6faec-108">**AzLoadBalancerRuleConfig** Cmdlet 會將規則配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6faec-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="6faec-109">示例</span><span class="sxs-lookup"><span data-stu-id="6faec-109">EXAMPLES</span></span>

### <span data-ttu-id="6faec-110">範例1：在負載平衡器中新增規則配置</span><span class="sxs-lookup"><span data-stu-id="6faec-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="6faec-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6faec-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6faec-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzLoadBalancerRuleConfig** ，這會新增名為 NewRule 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="6faec-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="6faec-113">第三個命令會使用新的負載平衡器規則 Config 來更新 azure 中的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6faec-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="6faec-114">參數</span><span class="sxs-lookup"><span data-stu-id="6faec-114">PARAMETERS</span></span>

### <span data-ttu-id="6faec-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6faec-115">-BackendAddressPool</span></span>
<span data-ttu-id="6faec-116">指定要與負載平衡器規則配置相關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="6faec-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6faec-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="6faec-118">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6faec-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6faec-119">-BackendPort</span></span>
<span data-ttu-id="6faec-120">指定與負載平衡器規則設定相符的流量後端埠。</span><span class="sxs-lookup"><span data-stu-id="6faec-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6faec-121">-DefaultProfile</span></span>
<span data-ttu-id="6faec-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6faec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6faec-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6faec-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6faec-124">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="6faec-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6faec-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6faec-125">-EnableFloatingIP</span></span>
<span data-ttu-id="6faec-126">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6faec-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6faec-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6faec-127">-EnableTcpReset</span></span>
<span data-ttu-id="6faec-128">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="6faec-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6faec-129">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="6faec-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6faec-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6faec-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6faec-131">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="6faec-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6faec-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6faec-133">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="6faec-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6faec-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6faec-134">-FrontendPort</span></span>
<span data-ttu-id="6faec-135">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="6faec-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6faec-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6faec-137">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="6faec-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="6faec-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6faec-138">-LoadBalancer</span></span>
<span data-ttu-id="6faec-139">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="6faec-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="6faec-140">這個 Cmdlet 會將規則配置新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6faec-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6faec-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6faec-141">-LoadDistribution</span></span>
<span data-ttu-id="6faec-142">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="6faec-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="6faec-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="6faec-143">-Name</span></span>
<span data-ttu-id="6faec-144">指定負載平衡器規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6faec-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-145">探測器</span><span class="sxs-lookup"><span data-stu-id="6faec-145">-Probe</span></span>
<span data-ttu-id="6faec-146">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="6faec-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6faec-147">-ProbeId</span></span>
<span data-ttu-id="6faec-148">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="6faec-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6faec-149">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6faec-149">-Protocol</span></span>
<span data-ttu-id="6faec-150">指定由負載等化器規則所相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6faec-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6faec-151">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="6faec-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6faec-152">-確認</span><span class="sxs-lookup"><span data-stu-id="6faec-152">-Confirm</span></span>
<span data-ttu-id="6faec-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6faec-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6faec-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6faec-154">-WhatIf</span></span>
<span data-ttu-id="6faec-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6faec-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6faec-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6faec-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6faec-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6faec-157">CommonParameters</span></span>
<span data-ttu-id="6faec-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6faec-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6faec-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6faec-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6faec-160">輸入</span><span class="sxs-lookup"><span data-stu-id="6faec-160">INPUTS</span></span>

### <span data-ttu-id="6faec-161">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6faec-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6faec-162">System.object</span><span class="sxs-lookup"><span data-stu-id="6faec-162">System.String</span></span>

### <span data-ttu-id="6faec-163">System.object</span><span class="sxs-lookup"><span data-stu-id="6faec-163">System.Int32</span></span>

### <span data-ttu-id="6faec-164">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6faec-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="6faec-165">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6faec-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="6faec-166">PSProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6faec-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="6faec-167">輸出</span><span class="sxs-lookup"><span data-stu-id="6faec-167">OUTPUTS</span></span>

### <span data-ttu-id="6faec-168">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6faec-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6faec-169">筆記</span><span class="sxs-lookup"><span data-stu-id="6faec-169">NOTES</span></span>

## <span data-ttu-id="6faec-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="6faec-170">RELATED LINKS</span></span>

[<span data-ttu-id="6faec-171">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6faec-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6faec-172">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6faec-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6faec-173">新-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6faec-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6faec-174">移除-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6faec-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6faec-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6faec-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


