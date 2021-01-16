---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281296"
---
# <span data-ttu-id="544bf-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="544bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="544bf-102">SYNOPSIS</span></span>
<span data-ttu-id="544bf-103">為負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="544bf-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="544bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="544bf-104">SYNTAX</span></span>

### <span data-ttu-id="544bf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="544bf-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="544bf-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="544bf-107">DESCRIPTION</span></span>
<span data-ttu-id="544bf-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="544bf-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="544bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="544bf-109">EXAMPLES</span></span>

### <span data-ttu-id="544bf-110">範例1：修改負載平衡器上的輸入 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="544bf-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="544bf-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="544bf-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="544bf-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerInboundNatRuleConfig，這會將輸入的 NAT 規則設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="544bf-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="544bf-113">第三個命令會將負載平衡器傳到 **AzLoadBalancerInboundNatRuleConfig**，這會儲存並更新入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="544bf-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="544bf-114">請注意，規則設定沒有啟用浮動 IP，而是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="544bf-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="544bf-115">參數</span><span class="sxs-lookup"><span data-stu-id="544bf-115">PARAMETERS</span></span>

### <span data-ttu-id="544bf-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="544bf-116">-BackendPort</span></span>
<span data-ttu-id="544bf-117">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="544bf-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="544bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544bf-118">-DefaultProfile</span></span>
<span data-ttu-id="544bf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="544bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="544bf-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="544bf-120">-EnableFloatingIP</span></span>
<span data-ttu-id="544bf-121">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="544bf-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="544bf-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="544bf-122">-EnableTcpReset</span></span>
<span data-ttu-id="544bf-123">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="544bf-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="544bf-124">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="544bf-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="544bf-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="544bf-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="544bf-126">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="544bf-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="544bf-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="544bf-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="544bf-128">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="544bf-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="544bf-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="544bf-129">-FrontendPort</span></span>
<span data-ttu-id="544bf-130">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="544bf-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="544bf-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="544bf-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="544bf-132">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="544bf-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="544bf-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="544bf-133">-LoadBalancer</span></span>
<span data-ttu-id="544bf-134">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="544bf-134">Specifies a load balancer.</span></span>
<span data-ttu-id="544bf-135">這個 Cmdlet 為此參數指定的負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="544bf-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="544bf-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="544bf-136">-Name</span></span>
<span data-ttu-id="544bf-137">指定入站 NAT 規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="544bf-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="544bf-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="544bf-138">-Protocol</span></span>
<span data-ttu-id="544bf-139">指定與入站 NAT 規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="544bf-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="544bf-140">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="544bf-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="544bf-141">-確認</span><span class="sxs-lookup"><span data-stu-id="544bf-141">-Confirm</span></span>
<span data-ttu-id="544bf-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="544bf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544bf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544bf-143">-WhatIf</span></span>
<span data-ttu-id="544bf-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="544bf-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="544bf-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="544bf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="544bf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544bf-146">CommonParameters</span></span>
<span data-ttu-id="544bf-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="544bf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544bf-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="544bf-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544bf-149">輸入</span><span class="sxs-lookup"><span data-stu-id="544bf-149">INPUTS</span></span>

### <span data-ttu-id="544bf-150">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="544bf-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="544bf-151">System.object</span><span class="sxs-lookup"><span data-stu-id="544bf-151">System.String</span></span>

### <span data-ttu-id="544bf-152">System.object</span><span class="sxs-lookup"><span data-stu-id="544bf-152">System.Int32</span></span>

### <span data-ttu-id="544bf-153">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="544bf-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="544bf-154">輸出</span><span class="sxs-lookup"><span data-stu-id="544bf-154">OUTPUTS</span></span>

### <span data-ttu-id="544bf-155">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="544bf-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="544bf-156">筆記</span><span class="sxs-lookup"><span data-stu-id="544bf-156">NOTES</span></span>

## <span data-ttu-id="544bf-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="544bf-157">RELATED LINKS</span></span>

[<span data-ttu-id="544bf-158">附加 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="544bf-159">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="544bf-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="544bf-160">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="544bf-161">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="544bf-162">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


