---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 1cfee59f1432cee5355ae562f8cc732a640d8c2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790278"
---
# <span data-ttu-id="2916e-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2916e-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2916e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2916e-102">SYNOPSIS</span></span>
<span data-ttu-id="2916e-103">將入站 NAT 規則配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2916e-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="2916e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2916e-104">SYNTAX</span></span>

### <span data-ttu-id="2916e-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="2916e-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2916e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2916e-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2916e-107">說明</span><span class="sxs-lookup"><span data-stu-id="2916e-107">DESCRIPTION</span></span>
<span data-ttu-id="2916e-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會將入站網路位址轉譯 (NAT) 規則設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2916e-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="2916e-109">示例</span><span class="sxs-lookup"><span data-stu-id="2916e-109">EXAMPLES</span></span>

### <span data-ttu-id="2916e-110">範例1：將入站 NAT 規則配置新增至負載平衡器</span><span class="sxs-lookup"><span data-stu-id="2916e-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="2916e-111">第一個命令會取得名為 MyloadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="2916e-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="2916e-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzLoadBalancerInboundNatRuleConfig** ，這會將輸入的 NAT 規則設定新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2916e-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="2916e-113">參數</span><span class="sxs-lookup"><span data-stu-id="2916e-113">PARAMETERS</span></span>

### <span data-ttu-id="2916e-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2916e-114">-BackendPort</span></span>
<span data-ttu-id="2916e-115">指定規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="2916e-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="2916e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2916e-116">-DefaultProfile</span></span>
<span data-ttu-id="2916e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2916e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2916e-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2916e-118">-EnableFloatingIP</span></span>
<span data-ttu-id="2916e-119">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2916e-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2916e-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2916e-120">-EnableTcpReset</span></span>
<span data-ttu-id="2916e-121">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="2916e-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2916e-122">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="2916e-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2916e-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2916e-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2916e-124">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2916e-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="2916e-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2916e-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2916e-126">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="2916e-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2916e-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2916e-127">-FrontendPort</span></span>
<span data-ttu-id="2916e-128">指定與規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="2916e-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="2916e-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2916e-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2916e-130">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="2916e-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2916e-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2916e-131">-LoadBalancer</span></span>
<span data-ttu-id="2916e-132">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="2916e-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="2916e-133">這個 Cmdlet 會將入站 NAT 規則配置新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2916e-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2916e-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2916e-134">-Name</span></span>
<span data-ttu-id="2916e-135">指定要新增的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2916e-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="2916e-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="2916e-136">-Protocol</span></span>
<span data-ttu-id="2916e-137">指定與入站 NAT 規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2916e-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="2916e-138">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="2916e-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="2916e-139">-確認</span><span class="sxs-lookup"><span data-stu-id="2916e-139">-Confirm</span></span>
<span data-ttu-id="2916e-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2916e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2916e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2916e-141">-WhatIf</span></span>
<span data-ttu-id="2916e-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2916e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2916e-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2916e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2916e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2916e-144">CommonParameters</span></span>
<span data-ttu-id="2916e-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2916e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2916e-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2916e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2916e-147">輸入</span><span class="sxs-lookup"><span data-stu-id="2916e-147">INPUTS</span></span>

### <span data-ttu-id="2916e-148">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2916e-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2916e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="2916e-149">System.String</span></span>

### <span data-ttu-id="2916e-150">System.object</span><span class="sxs-lookup"><span data-stu-id="2916e-150">System.Int32</span></span>

### <span data-ttu-id="2916e-151">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2916e-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="2916e-152">輸出</span><span class="sxs-lookup"><span data-stu-id="2916e-152">OUTPUTS</span></span>

### <span data-ttu-id="2916e-153">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2916e-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2916e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="2916e-154">NOTES</span></span>

## <span data-ttu-id="2916e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="2916e-155">RELATED LINKS</span></span>

[<span data-ttu-id="2916e-156">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2916e-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2916e-157">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2916e-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2916e-158">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2916e-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2916e-159">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2916e-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2916e-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2916e-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="2916e-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2916e-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


