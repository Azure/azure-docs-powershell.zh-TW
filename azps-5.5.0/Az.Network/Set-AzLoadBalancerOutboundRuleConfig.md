---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128679"
---
# <span data-ttu-id="6c259-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c259-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="6c259-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c259-102">SYNOPSIS</span></span>
<span data-ttu-id="6c259-103">設定負載平衡器的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="6c259-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6c259-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c259-104">SYNTAX</span></span>

### <span data-ttu-id="6c259-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6c259-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c259-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c259-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c259-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c259-107">DESCRIPTION</span></span>
<span data-ttu-id="6c259-108">**AzLoadBalancerOutboundRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="6c259-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6c259-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c259-109">EXAMPLES</span></span>

### <span data-ttu-id="6c259-110">範例1：修改負載平衡器上的輸出規則配置</span><span class="sxs-lookup"><span data-stu-id="6c259-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="6c259-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c259-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6c259-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerOutboundRuleConfig，這會在其中新增輸出規則設定。</span><span class="sxs-lookup"><span data-stu-id="6c259-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="6c259-113">第三個命令會將負載平衡器傳到 AzLoadBalancerOutboundRuleConfig，這會儲存並更新輸出規則 **設定**。</span><span class="sxs-lookup"><span data-stu-id="6c259-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="6c259-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c259-114">PARAMETERS</span></span>

### <span data-ttu-id="6c259-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="6c259-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="6c259-116">要用於 NAT 的輸出埠數目。</span><span class="sxs-lookup"><span data-stu-id="6c259-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="6c259-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6c259-117">-BackendAddressPool</span></span>
<span data-ttu-id="6c259-118">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="6c259-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="6c259-119">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="6c259-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="6c259-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6c259-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="6c259-121">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="6c259-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="6c259-122">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="6c259-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="6c259-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c259-123">-DefaultProfile</span></span>
<span data-ttu-id="6c259-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c259-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c259-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6c259-125">-EnableTcpReset</span></span>
<span data-ttu-id="6c259-126">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="6c259-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="6c259-127">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="6c259-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6c259-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c259-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6c259-129">負載平衡器的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6c259-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="6c259-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6c259-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6c259-131">TCP 空閒連線的超時時間</span><span class="sxs-lookup"><span data-stu-id="6c259-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="6c259-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c259-132">-LoadBalancer</span></span>
<span data-ttu-id="6c259-133">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="6c259-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="6c259-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c259-134">-Name</span></span>
<span data-ttu-id="6c259-135">輸出規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c259-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="6c259-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6c259-136">-Protocol</span></span>
<span data-ttu-id="6c259-137">通訊協定-TCP、UDP 或 All</span><span class="sxs-lookup"><span data-stu-id="6c259-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="6c259-138">-確認</span><span class="sxs-lookup"><span data-stu-id="6c259-138">-Confirm</span></span>
<span data-ttu-id="6c259-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c259-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c259-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c259-140">-WhatIf</span></span>
<span data-ttu-id="6c259-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c259-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c259-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c259-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c259-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c259-143">CommonParameters</span></span>
<span data-ttu-id="6c259-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c259-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c259-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c259-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c259-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6c259-146">INPUTS</span></span>

### <span data-ttu-id="6c259-147">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c259-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6c259-148">System.object</span><span class="sxs-lookup"><span data-stu-id="6c259-148">System.Int32</span></span>

### <span data-ttu-id="6c259-149">System.object</span><span class="sxs-lookup"><span data-stu-id="6c259-149">System.String</span></span>

### <span data-ttu-id="6c259-150">PSResourceId [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6c259-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="6c259-151">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c259-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="6c259-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6c259-152">OUTPUTS</span></span>

### <span data-ttu-id="6c259-153">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c259-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6c259-154">筆記</span><span class="sxs-lookup"><span data-stu-id="6c259-154">NOTES</span></span>

## <span data-ttu-id="6c259-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c259-155">RELATED LINKS</span></span>

[<span data-ttu-id="6c259-156">附加 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c259-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6c259-157">AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c259-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6c259-158">新-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c259-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6c259-159">移除-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c259-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
