---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 76adf0c831b79b219598a254a859b8603f8c3f27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915313"
---
# <span data-ttu-id="c25e9-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c25e9-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c25e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c25e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c25e9-103">設定負載平衡器外發規則設定。</span><span class="sxs-lookup"><span data-stu-id="c25e9-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c25e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="c25e9-104">SYNTAX</span></span>

### <span data-ttu-id="c25e9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c25e9-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c25e9-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25e9-107">描述</span><span class="sxs-lookup"><span data-stu-id="c25e9-107">DESCRIPTION</span></span>
<span data-ttu-id="c25e9-108">**Set-AzLoadBalancerOutboundRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定輸出規則設定。</span><span class="sxs-lookup"><span data-stu-id="c25e9-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c25e9-109">例子</span><span class="sxs-lookup"><span data-stu-id="c25e9-109">EXAMPLES</span></span>

### <span data-ttu-id="c25e9-110">範例 1：修改負載平衡器上的外發規則組式</span><span class="sxs-lookup"><span data-stu-id="c25e9-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="c25e9-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在$slb變數中。</span><span class="sxs-lookup"><span data-stu-id="c25e9-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c25e9-112">第二個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerOutboundRuleConfig，為它新增輸出規則組式。</span><span class="sxs-lookup"><span data-stu-id="c25e9-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="c25e9-113">第三個命令會將負載平衡器傳遞至 **Set-AzLoadBalancerOutboundRuleConfig，** 這可節省和更新輸出規則設定。</span><span class="sxs-lookup"><span data-stu-id="c25e9-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="c25e9-114">參數</span><span class="sxs-lookup"><span data-stu-id="c25e9-114">PARAMETERS</span></span>

### <span data-ttu-id="c25e9-115">-已配置OutboundPort</span><span class="sxs-lookup"><span data-stu-id="c25e9-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c25e9-116">NAT 的外發端口數量。</span><span class="sxs-lookup"><span data-stu-id="c25e9-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c25e9-117">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="c25e9-117">-BackendAddressPool</span></span>
<span data-ttu-id="c25e9-118">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="c25e9-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c25e9-119">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="c25e9-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25e9-120">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c25e9-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="c25e9-121">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="c25e9-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c25e9-122">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="c25e9-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25e9-123">-DefaultProfile</span></span>
<span data-ttu-id="c25e9-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c25e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25e9-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c25e9-125">-EnableTcpReset</span></span>
<span data-ttu-id="c25e9-126">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="c25e9-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c25e9-127">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="c25e9-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c25e9-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c25e9-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c25e9-129">負載平衡器的前一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c25e9-129">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25e9-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c25e9-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c25e9-131">TCP 閒置連接的超時</span><span class="sxs-lookup"><span data-stu-id="c25e9-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c25e9-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c25e9-132">-LoadBalancer</span></span>
<span data-ttu-id="c25e9-133">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="c25e9-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c25e9-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="c25e9-134">-Name</span></span>
<span data-ttu-id="c25e9-135">外發規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c25e9-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c25e9-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c25e9-136">-Protocol</span></span>
<span data-ttu-id="c25e9-137">通訊協定 - TCP、UDP 或全部</span><span class="sxs-lookup"><span data-stu-id="c25e9-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25e9-138">-確認</span><span class="sxs-lookup"><span data-stu-id="c25e9-138">-Confirm</span></span>
<span data-ttu-id="c25e9-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c25e9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25e9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25e9-140">-WhatIf</span></span>
<span data-ttu-id="c25e9-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c25e9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25e9-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c25e9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25e9-143">CommonParameters</span></span>
<span data-ttu-id="c25e9-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c25e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25e9-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c25e9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25e9-146">輸入</span><span class="sxs-lookup"><span data-stu-id="c25e9-146">INPUTS</span></span>

### <span data-ttu-id="c25e9-147">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c25e9-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c25e9-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c25e9-148">System.Int32</span></span>

### <span data-ttu-id="c25e9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c25e9-149">System.String</span></span>

### <span data-ttu-id="c25e9-150">Microsoft.Azure.Commands.Network.models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="c25e9-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c25e9-151">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c25e9-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c25e9-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c25e9-152">OUTPUTS</span></span>

### <span data-ttu-id="c25e9-153">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c25e9-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c25e9-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c25e9-154">NOTES</span></span>

## <span data-ttu-id="c25e9-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c25e9-155">RELATED LINKS</span></span>

[<span data-ttu-id="c25e9-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c25e9-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c25e9-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c25e9-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c25e9-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c25e9-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c25e9-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c25e9-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
