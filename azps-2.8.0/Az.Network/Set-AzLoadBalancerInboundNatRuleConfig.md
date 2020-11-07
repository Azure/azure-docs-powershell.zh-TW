---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ea27d5b58586aeb9e627c926fc67d89cfe8ec354
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788978"
---
# <span data-ttu-id="3c658-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c658-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="3c658-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c658-102">SYNOPSIS</span></span>
<span data-ttu-id="3c658-103">為負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="3c658-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3c658-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c658-104">SYNTAX</span></span>

### <span data-ttu-id="3c658-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="3c658-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c658-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c658-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c658-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c658-107">DESCRIPTION</span></span>
<span data-ttu-id="3c658-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="3c658-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3c658-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c658-109">EXAMPLES</span></span>

### <span data-ttu-id="3c658-110">範例1：修改負載平衡器上的輸入 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="3c658-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="3c658-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c658-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="3c658-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzLoadBalancerInboundNatRuleConfig，這會將輸入的 NAT 規則設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="3c658-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="3c658-113">第三個命令會將負載平衡器傳到 **AzLoadBalancerInboundNatRuleConfig** ，這會儲存並更新入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="3c658-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="3c658-114">請注意，規則設定沒有啟用浮動 IP，而是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="3c658-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="3c658-115">參數</span><span class="sxs-lookup"><span data-stu-id="3c658-115">PARAMETERS</span></span>

### <span data-ttu-id="3c658-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3c658-116">-BackendPort</span></span>
<span data-ttu-id="3c658-117">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="3c658-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="3c658-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c658-118">-DefaultProfile</span></span>
<span data-ttu-id="3c658-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c658-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c658-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="3c658-120">-EnableFloatingIP</span></span>
<span data-ttu-id="3c658-121">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3c658-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="3c658-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="3c658-122">-EnableTcpReset</span></span>
<span data-ttu-id="3c658-123">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="3c658-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="3c658-124">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="3c658-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="3c658-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c658-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3c658-126">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="3c658-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="3c658-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3c658-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3c658-128">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="3c658-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="3c658-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3c658-129">-FrontendPort</span></span>
<span data-ttu-id="3c658-130">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="3c658-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3c658-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3c658-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3c658-132">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c658-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="3c658-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3c658-133">-LoadBalancer</span></span>
<span data-ttu-id="3c658-134">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="3c658-134">Specifies a load balancer.</span></span>
<span data-ttu-id="3c658-135">這個 Cmdlet 為此參數指定的負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="3c658-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c658-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c658-136">-Name</span></span>
<span data-ttu-id="3c658-137">指定入站 NAT 規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c658-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="3c658-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3c658-138">-Protocol</span></span>
<span data-ttu-id="3c658-139">指定與入站 NAT 規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3c658-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="3c658-140">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="3c658-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="3c658-141">-確認</span><span class="sxs-lookup"><span data-stu-id="3c658-141">-Confirm</span></span>
<span data-ttu-id="3c658-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c658-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c658-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c658-143">-WhatIf</span></span>
<span data-ttu-id="3c658-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c658-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c658-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c658-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c658-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c658-146">CommonParameters</span></span>
<span data-ttu-id="3c658-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c658-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c658-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c658-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c658-149">輸入</span><span class="sxs-lookup"><span data-stu-id="3c658-149">INPUTS</span></span>

### <span data-ttu-id="3c658-150">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c658-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3c658-151">System.object</span><span class="sxs-lookup"><span data-stu-id="3c658-151">System.String</span></span>

### <span data-ttu-id="3c658-152">System.object</span><span class="sxs-lookup"><span data-stu-id="3c658-152">System.Int32</span></span>

### <span data-ttu-id="3c658-153">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c658-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="3c658-154">輸出</span><span class="sxs-lookup"><span data-stu-id="3c658-154">OUTPUTS</span></span>

### <span data-ttu-id="3c658-155">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c658-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3c658-156">筆記</span><span class="sxs-lookup"><span data-stu-id="3c658-156">NOTES</span></span>

## <span data-ttu-id="3c658-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c658-157">RELATED LINKS</span></span>

[<span data-ttu-id="3c658-158">附加 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c658-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3c658-159">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3c658-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3c658-160">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c658-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3c658-161">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c658-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3c658-162">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c658-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


