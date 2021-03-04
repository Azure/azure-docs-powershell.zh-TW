---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916077"
---
# <span data-ttu-id="74971-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74971-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="74971-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74971-102">SYNOPSIS</span></span>
<span data-ttu-id="74971-103">新增外發規則組式至負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="74971-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="74971-104">語法</span><span class="sxs-lookup"><span data-stu-id="74971-104">SYNTAX</span></span>

### <span data-ttu-id="74971-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="74971-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74971-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74971-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74971-107">描述</span><span class="sxs-lookup"><span data-stu-id="74971-107">DESCRIPTION</span></span>
<span data-ttu-id="74971-108">**Add-AzLoadBalancerOutboundRuleConfig** Cmdlet 會將輸出規則組配置新增到 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="74971-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="74971-109">例子</span><span class="sxs-lookup"><span data-stu-id="74971-109">EXAMPLES</span></span>

### <span data-ttu-id="74971-110">範例 1：新增外發規則組式至負載平衡器</span><span class="sxs-lookup"><span data-stu-id="74971-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="74971-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="74971-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="74971-112">第二個命令會使用管線運算子，將 $slb 中的負載平衡器傳遞到 **Add-AzLoadBalancerOutboundRuleConfig，** 此為負載平衡器新增輸出規則組式。</span><span class="sxs-lookup"><span data-stu-id="74971-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="74971-113">參數</span><span class="sxs-lookup"><span data-stu-id="74971-113">PARAMETERS</span></span>

### <span data-ttu-id="74971-114">-已配置OutboundPort</span><span class="sxs-lookup"><span data-stu-id="74971-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="74971-115">NAT 的外發端口數量。</span><span class="sxs-lookup"><span data-stu-id="74971-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="74971-116">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="74971-116">-BackendAddressPool</span></span>
<span data-ttu-id="74971-117">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="74971-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="74971-118">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="74971-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="74971-119">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="74971-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="74971-120">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="74971-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="74971-121">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="74971-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="74971-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74971-122">-DefaultProfile</span></span>
<span data-ttu-id="74971-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74971-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74971-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="74971-124">-EnableTcpReset</span></span>
<span data-ttu-id="74971-125">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="74971-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="74971-126">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="74971-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="74971-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="74971-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="74971-128">負載平衡器的前一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="74971-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="74971-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="74971-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="74971-130">TCP 閒置連接的超時</span><span class="sxs-lookup"><span data-stu-id="74971-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="74971-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74971-131">-LoadBalancer</span></span>
<span data-ttu-id="74971-132">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="74971-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="74971-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="74971-133">-Name</span></span>
<span data-ttu-id="74971-134">外發規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="74971-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="74971-135">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="74971-135">-Protocol</span></span>
<span data-ttu-id="74971-136">通訊協定 - TCP、UDP 或全部</span><span class="sxs-lookup"><span data-stu-id="74971-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="74971-137">-確認</span><span class="sxs-lookup"><span data-stu-id="74971-137">-Confirm</span></span>
<span data-ttu-id="74971-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="74971-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74971-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74971-139">-WhatIf</span></span>
<span data-ttu-id="74971-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74971-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74971-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74971-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74971-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74971-142">CommonParameters</span></span>
<span data-ttu-id="74971-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74971-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74971-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="74971-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74971-145">輸入</span><span class="sxs-lookup"><span data-stu-id="74971-145">INPUTS</span></span>

### <span data-ttu-id="74971-146">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74971-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="74971-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="74971-147">System.Int32</span></span>

### <span data-ttu-id="74971-148">System.String</span><span class="sxs-lookup"><span data-stu-id="74971-148">System.String</span></span>

### <span data-ttu-id="74971-149">Microsoft.Azure.Commands.Network.models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="74971-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="74971-150">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="74971-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="74971-151">輸出</span><span class="sxs-lookup"><span data-stu-id="74971-151">OUTPUTS</span></span>

### <span data-ttu-id="74971-152">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74971-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="74971-153">筆記</span><span class="sxs-lookup"><span data-stu-id="74971-153">NOTES</span></span>

## <span data-ttu-id="74971-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="74971-154">RELATED LINKS</span></span>

[<span data-ttu-id="74971-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74971-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="74971-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74971-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="74971-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74971-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="74971-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74971-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
