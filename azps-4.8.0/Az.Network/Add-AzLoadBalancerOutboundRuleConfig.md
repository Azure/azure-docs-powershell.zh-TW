---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127545"
---
# <span data-ttu-id="d4f6a-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4f6a-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="d4f6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f6a-103">將輸出規則設定新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="d4f6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4f6a-104">SYNTAX</span></span>

### <span data-ttu-id="d4f6a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d4f6a-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f6a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4f6a-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4f6a-107">說明</span><span class="sxs-lookup"><span data-stu-id="d4f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="d4f6a-108">**AzLoadBalancerOutboundRuleConfig** Cmdlet 會將輸出規則配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d4f6a-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="d4f6a-110">範例1：在負載平衡器中新增輸出規則配置</span><span class="sxs-lookup"><span data-stu-id="d4f6a-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="d4f6a-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d4f6a-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzLoadBalancerOutboundRuleConfig** ，這會將輸出規則設定新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d4f6a-113">參數</span><span class="sxs-lookup"><span data-stu-id="d4f6a-113">PARAMETERS</span></span>

### <span data-ttu-id="d4f6a-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="d4f6a-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="d4f6a-115">要用於 NAT 的輸出埠數目。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="d4f6a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d4f6a-116">-BackendAddressPool</span></span>
<span data-ttu-id="d4f6a-117">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="d4f6a-118">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="d4f6a-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d4f6a-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="d4f6a-120">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="d4f6a-121">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="d4f6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f6a-122">-DefaultProfile</span></span>
<span data-ttu-id="d4f6a-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f6a-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d4f6a-124">-EnableTcpReset</span></span>
<span data-ttu-id="d4f6a-125">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="d4f6a-126">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d4f6a-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4f6a-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d4f6a-128">負載平衡器的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="d4f6a-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4f6a-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d4f6a-130">TCP 空閒連線的超時時間</span><span class="sxs-lookup"><span data-stu-id="d4f6a-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="d4f6a-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4f6a-131">-LoadBalancer</span></span>
<span data-ttu-id="d4f6a-132">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="d4f6a-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4f6a-133">-Name</span></span>
<span data-ttu-id="d4f6a-134">輸出規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="d4f6a-135">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d4f6a-135">-Protocol</span></span>
<span data-ttu-id="d4f6a-136">通訊協定-TCP、UDP 或 All</span><span class="sxs-lookup"><span data-stu-id="d4f6a-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="d4f6a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="d4f6a-137">-Confirm</span></span>
<span data-ttu-id="d4f6a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f6a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f6a-139">-WhatIf</span></span>
<span data-ttu-id="d4f6a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f6a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f6a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f6a-142">CommonParameters</span></span>
<span data-ttu-id="d4f6a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f6a-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4f6a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f6a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d4f6a-145">INPUTS</span></span>

### <span data-ttu-id="d4f6a-146">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4f6a-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d4f6a-147">System.object</span><span class="sxs-lookup"><span data-stu-id="d4f6a-147">System.Int32</span></span>

### <span data-ttu-id="d4f6a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="d4f6a-148">System.String</span></span>

### <span data-ttu-id="d4f6a-149">PSResourceId [] （[]）</span><span class="sxs-lookup"><span data-stu-id="d4f6a-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="d4f6a-150">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4f6a-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d4f6a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="d4f6a-151">OUTPUTS</span></span>

### <span data-ttu-id="d4f6a-152">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4f6a-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d4f6a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="d4f6a-153">NOTES</span></span>

## <span data-ttu-id="d4f6a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4f6a-154">RELATED LINKS</span></span>

[<span data-ttu-id="d4f6a-155">AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4f6a-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d4f6a-156">新-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4f6a-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d4f6a-157">移除-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4f6a-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d4f6a-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4f6a-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)