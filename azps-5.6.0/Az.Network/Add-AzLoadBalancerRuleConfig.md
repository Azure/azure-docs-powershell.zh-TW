---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 8aa8850caa2194bd29c44b03c42fe7c7dcec725d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907341"
---
# <span data-ttu-id="1b303-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b303-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="1b303-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b303-102">SYNOPSIS</span></span>
<span data-ttu-id="1b303-103">新增規則組配置至負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="1b303-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="1b303-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b303-104">SYNTAX</span></span>

### <span data-ttu-id="1b303-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1b303-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b303-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b303-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b303-107">描述</span><span class="sxs-lookup"><span data-stu-id="1b303-107">DESCRIPTION</span></span>
<span data-ttu-id="1b303-108">**Add-AzLoadBalancerRuleConfig** Cmdlet 會新增規則組配置至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="1b303-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="1b303-109">例子</span><span class="sxs-lookup"><span data-stu-id="1b303-109">EXAMPLES</span></span>

### <span data-ttu-id="1b303-110">範例 1：在負載平衡器中新增規則組</span><span class="sxs-lookup"><span data-stu-id="1b303-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="1b303-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="1b303-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="1b303-112">第二個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 **Add-AzLoadBalancerRuleConfig，** 此命令會新增名為 NewRule 的規則組式。</span><span class="sxs-lookup"><span data-stu-id="1b303-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="1b303-113">第三個命令會以新的負載平衡器規則 Config 更新 azure 中的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="1b303-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="1b303-114">參數</span><span class="sxs-lookup"><span data-stu-id="1b303-114">PARAMETERS</span></span>

### <span data-ttu-id="1b303-115">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="1b303-115">-BackendAddressPool</span></span>
<span data-ttu-id="1b303-116">指定要與負載平衡器規則群組原則關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="1b303-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-117">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1b303-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="1b303-118">指定要與負載 **平衡器規則群組原則關聯的後端AddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b303-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-119">-後端埠</span><span class="sxs-lookup"><span data-stu-id="1b303-119">-BackendPort</span></span>
<span data-ttu-id="1b303-120">指定與負載平衡器規則組配置相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="1b303-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b303-121">-DefaultProfile</span></span>
<span data-ttu-id="1b303-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b303-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b303-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="1b303-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="1b303-124">為後端集區中的虛擬機器設定 SNAT，以使用負載平衡規則前端指定的公用IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b303-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="1b303-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="1b303-125">-EnableFloatingIP</span></span>
<span data-ttu-id="1b303-126">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b303-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1b303-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1b303-127">-EnableTcpReset</span></span>
<span data-ttu-id="1b303-128">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="1b303-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="1b303-129">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="1b303-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1b303-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b303-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1b303-131">指定要與負載平衡器規則群組原則關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="1b303-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1b303-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1b303-133">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b303-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="1b303-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1b303-134">-FrontendPort</span></span>
<span data-ttu-id="1b303-135">指定與負載平衡器規則組配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="1b303-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1b303-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1b303-137">指定在負載平衡器中維持交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="1b303-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="1b303-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b303-138">-LoadBalancer</span></span>
<span data-ttu-id="1b303-139">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="1b303-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="1b303-140">此 Cmdlet 會新增規則設定至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="1b303-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b303-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="1b303-141">-LoadDistribution</span></span>
<span data-ttu-id="1b303-142">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="1b303-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="1b303-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b303-143">-Name</span></span>
<span data-ttu-id="1b303-144">指定負載平衡器規則組名。</span><span class="sxs-lookup"><span data-stu-id="1b303-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-145">-進位</span><span class="sxs-lookup"><span data-stu-id="1b303-145">-Probe</span></span>
<span data-ttu-id="1b303-146">指定與負載平衡器規則組配置的關聯。</span><span class="sxs-lookup"><span data-stu-id="1b303-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-147">-一維Id</span><span class="sxs-lookup"><span data-stu-id="1b303-147">-ProbeId</span></span>
<span data-ttu-id="1b303-148">指定要與負載平衡器規則組式關聯的探索識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b303-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b303-149">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1b303-149">-Protocol</span></span>
<span data-ttu-id="1b303-150">指定負載平衡器規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1b303-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="1b303-151">此參數可接受的值為：Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="1b303-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="1b303-152">-確認</span><span class="sxs-lookup"><span data-stu-id="1b303-152">-Confirm</span></span>
<span data-ttu-id="1b303-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1b303-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b303-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b303-154">-WhatIf</span></span>
<span data-ttu-id="1b303-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b303-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b303-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b303-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b303-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b303-157">CommonParameters</span></span>
<span data-ttu-id="1b303-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b303-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b303-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1b303-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b303-160">輸入</span><span class="sxs-lookup"><span data-stu-id="1b303-160">INPUTS</span></span>

### <span data-ttu-id="1b303-161">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b303-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1b303-162">System.String</span><span class="sxs-lookup"><span data-stu-id="1b303-162">System.String</span></span>

### <span data-ttu-id="1b303-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1b303-163">System.Int32</span></span>

### <span data-ttu-id="1b303-164">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b303-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="1b303-165">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b303-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="1b303-166">Microsoft.Azure.Commands.Network.models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="1b303-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="1b303-167">輸出</span><span class="sxs-lookup"><span data-stu-id="1b303-167">OUTPUTS</span></span>

### <span data-ttu-id="1b303-168">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b303-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b303-169">筆記</span><span class="sxs-lookup"><span data-stu-id="1b303-169">NOTES</span></span>

## <span data-ttu-id="1b303-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b303-170">RELATED LINKS</span></span>

[<span data-ttu-id="1b303-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b303-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1b303-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b303-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b303-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b303-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b303-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b303-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b303-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b303-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


