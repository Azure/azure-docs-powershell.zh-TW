---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916081"
---
# <span data-ttu-id="8735c-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8735c-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8735c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8735c-102">SYNOPSIS</span></span>
<span data-ttu-id="8735c-103">將內入 NAT 規則組組新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8735c-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="8735c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8735c-104">SYNTAX</span></span>

### <span data-ttu-id="8735c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8735c-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8735c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8735c-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8735c-107">描述</span><span class="sxs-lookup"><span data-stu-id="8735c-107">DESCRIPTION</span></span>
<span data-ttu-id="8735c-108">**Add-AzLoadBalancerInboundNatRuleConfig** Cmdlet 會將輸入網路位址轉譯 (NAT) 規則組配置新增到 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8735c-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="8735c-109">例子</span><span class="sxs-lookup"><span data-stu-id="8735c-109">EXAMPLES</span></span>

### <span data-ttu-id="8735c-110">範例 1：將內入 NAT 規則組組新增到負載平衡器</span><span class="sxs-lookup"><span data-stu-id="8735c-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="8735c-111">第一個命令會取得名為 MyloadBalancer 的負載平衡器，然後將它儲存在變數 $slb。</span><span class="sxs-lookup"><span data-stu-id="8735c-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="8735c-112">第二個命令會使用管線運算子，將 $slb 中的負載平衡器傳遞到 **Add-AzLoadBalancerInboundNatRuleConfig，** 這會將輸入 NAT 規則組式新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8735c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="8735c-113">最後一個命令會設定為載入平衡器，如果您沒有執行 Set-AzLoadBalancer，您的變更將不會套用至載入平衡器。</span><span class="sxs-lookup"><span data-stu-id="8735c-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="8735c-114">參數</span><span class="sxs-lookup"><span data-stu-id="8735c-114">PARAMETERS</span></span>

### <span data-ttu-id="8735c-115">-後端埠</span><span class="sxs-lookup"><span data-stu-id="8735c-115">-BackendPort</span></span>
<span data-ttu-id="8735c-116">指定與規則組配置相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="8735c-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="8735c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8735c-117">-DefaultProfile</span></span>
<span data-ttu-id="8735c-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8735c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8735c-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8735c-119">-EnableFloatingIP</span></span>
<span data-ttu-id="8735c-120">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8735c-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8735c-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8735c-121">-EnableTcpReset</span></span>
<span data-ttu-id="8735c-122">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="8735c-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="8735c-123">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="8735c-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8735c-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8735c-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8735c-125">指定要與輸入 NAT 規則群組原則建立關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="8735c-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="8735c-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8735c-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8735c-127">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8735c-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8735c-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8735c-128">-FrontendPort</span></span>
<span data-ttu-id="8735c-129">指定符合規則配置的前端埠。</span><span class="sxs-lookup"><span data-stu-id="8735c-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="8735c-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8735c-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8735c-131">指定在負載平衡器中維持交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="8735c-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8735c-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8735c-132">-LoadBalancer</span></span>
<span data-ttu-id="8735c-133">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="8735c-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="8735c-134">此 Cmdlet 會新增輸入 NAT 規則設定至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8735c-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8735c-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="8735c-135">-Name</span></span>
<span data-ttu-id="8735c-136">指定要新增的輸入 NAT 規則組名。</span><span class="sxs-lookup"><span data-stu-id="8735c-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="8735c-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="8735c-137">-Protocol</span></span>
<span data-ttu-id="8735c-138">指定與內入 NAT 規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8735c-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="8735c-139">此參數可接受的值為：Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="8735c-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="8735c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="8735c-140">-Confirm</span></span>
<span data-ttu-id="8735c-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8735c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8735c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8735c-142">-WhatIf</span></span>
<span data-ttu-id="8735c-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8735c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8735c-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8735c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8735c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8735c-145">CommonParameters</span></span>
<span data-ttu-id="8735c-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8735c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8735c-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8735c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8735c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8735c-148">INPUTS</span></span>

### <span data-ttu-id="8735c-149">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8735c-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="8735c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8735c-150">System.String</span></span>

### <span data-ttu-id="8735c-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8735c-151">System.Int32</span></span>

### <span data-ttu-id="8735c-152">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8735c-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="8735c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8735c-153">OUTPUTS</span></span>

### <span data-ttu-id="8735c-154">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8735c-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8735c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8735c-155">NOTES</span></span>

## <span data-ttu-id="8735c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8735c-156">RELATED LINKS</span></span>

[<span data-ttu-id="8735c-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8735c-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8735c-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8735c-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8735c-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8735c-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8735c-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8735c-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8735c-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8735c-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="8735c-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8735c-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


