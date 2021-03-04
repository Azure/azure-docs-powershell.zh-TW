---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a0d5adbc1e3fb2b38ded91431ab0cf349c541ebd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904894"
---
# <span data-ttu-id="d2360-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2360-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d2360-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2360-102">SYNOPSIS</span></span>
<span data-ttu-id="d2360-103">設定負載平衡器之內入 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="d2360-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d2360-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2360-104">SYNTAX</span></span>

### <span data-ttu-id="d2360-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d2360-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2360-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2360-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2360-107">描述</span><span class="sxs-lookup"><span data-stu-id="d2360-107">DESCRIPTION</span></span>
<span data-ttu-id="d2360-108">**Set-AzLoadBalancerInboundNatRuleConfig** Cmdlet 會為 Azure 負載平衡器設定輸入網路位址轉譯 (NAT) 規則設定。</span><span class="sxs-lookup"><span data-stu-id="d2360-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d2360-109">例子</span><span class="sxs-lookup"><span data-stu-id="d2360-109">EXAMPLES</span></span>

### <span data-ttu-id="d2360-110">範例 1：修改負載平衡器上的內入 NAT 規則組</span><span class="sxs-lookup"><span data-stu-id="d2360-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="d2360-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在$slb變數中。</span><span class="sxs-lookup"><span data-stu-id="d2360-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="d2360-112">第二個命令會使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerInboundNatRuleConfig，為它新增輸入 NAT 規則組式。</span><span class="sxs-lookup"><span data-stu-id="d2360-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="d2360-113">第三個命令會將負載平衡器傳遞至 **Set-AzLoadBalancerInboundNatRuleConfig，** 這可保存及更新輸入 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="d2360-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="d2360-114">請注意，規則設定是在未啟用浮動 IP 的情況下設定，前一個命令已啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="d2360-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="d2360-115">參數</span><span class="sxs-lookup"><span data-stu-id="d2360-115">PARAMETERS</span></span>

### <span data-ttu-id="d2360-116">-後端埠</span><span class="sxs-lookup"><span data-stu-id="d2360-116">-BackendPort</span></span>
<span data-ttu-id="d2360-117">指定符合此規則組配置的流量後端埠。</span><span class="sxs-lookup"><span data-stu-id="d2360-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="d2360-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2360-118">-DefaultProfile</span></span>
<span data-ttu-id="d2360-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2360-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2360-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d2360-120">-EnableFloatingIP</span></span>
<span data-ttu-id="d2360-121">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d2360-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d2360-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d2360-122">-EnableTcpReset</span></span>
<span data-ttu-id="d2360-123">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="d2360-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d2360-124">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="d2360-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d2360-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2360-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d2360-126">指定要與輸入 NAT 規則群組原則建立關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="d2360-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d2360-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d2360-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d2360-128">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2360-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d2360-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2360-129">-FrontendPort</span></span>
<span data-ttu-id="d2360-130">指定與負載平衡器規則組配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="d2360-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="d2360-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d2360-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d2360-132">指定在負載平衡器中維持交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="d2360-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d2360-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2360-133">-LoadBalancer</span></span>
<span data-ttu-id="d2360-134">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="d2360-134">Specifies a load balancer.</span></span>
<span data-ttu-id="d2360-135">此 Cmdlet 會為此參數指定的負載平衡器設定輸入 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="d2360-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2360-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2360-136">-Name</span></span>
<span data-ttu-id="d2360-137">指定輸入 NAT 規則組名。</span><span class="sxs-lookup"><span data-stu-id="d2360-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d2360-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d2360-138">-Protocol</span></span>
<span data-ttu-id="d2360-139">指定與內入 NAT 規則組配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d2360-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="d2360-140">此參數可接受的值為：Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="d2360-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d2360-141">-確認</span><span class="sxs-lookup"><span data-stu-id="d2360-141">-Confirm</span></span>
<span data-ttu-id="d2360-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d2360-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2360-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2360-143">-WhatIf</span></span>
<span data-ttu-id="d2360-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2360-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2360-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2360-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2360-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2360-146">CommonParameters</span></span>
<span data-ttu-id="d2360-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2360-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2360-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d2360-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2360-149">輸入</span><span class="sxs-lookup"><span data-stu-id="d2360-149">INPUTS</span></span>

### <span data-ttu-id="d2360-150">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2360-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d2360-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d2360-151">System.String</span></span>

### <span data-ttu-id="d2360-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d2360-152">System.Int32</span></span>

### <span data-ttu-id="d2360-153">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2360-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d2360-154">輸出</span><span class="sxs-lookup"><span data-stu-id="d2360-154">OUTPUTS</span></span>

### <span data-ttu-id="d2360-155">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2360-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d2360-156">筆記</span><span class="sxs-lookup"><span data-stu-id="d2360-156">NOTES</span></span>

## <span data-ttu-id="d2360-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2360-157">RELATED LINKS</span></span>

[<span data-ttu-id="d2360-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2360-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d2360-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2360-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d2360-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2360-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d2360-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2360-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d2360-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2360-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


