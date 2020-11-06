---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c7d0d5879b4c0ca7ee92a9f22d062241e1cb89a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449005"
---
# <span data-ttu-id="8db81-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8db81-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8db81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8db81-102">SYNOPSIS</span></span>
<span data-ttu-id="8db81-103">為負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="8db81-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db81-104">句法</span><span class="sxs-lookup"><span data-stu-id="8db81-104">SYNTAX</span></span>

### <span data-ttu-id="8db81-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8db81-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db81-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8db81-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db81-107">說明</span><span class="sxs-lookup"><span data-stu-id="8db81-107">DESCRIPTION</span></span>
<span data-ttu-id="8db81-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="8db81-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8db81-109">示例</span><span class="sxs-lookup"><span data-stu-id="8db81-109">EXAMPLES</span></span>

### <span data-ttu-id="8db81-110">範例1：修改負載平衡器上的輸入 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="8db81-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="8db81-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="8db81-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8db81-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerInboundNatRuleConfig，這會將輸入的 NAT 規則設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="8db81-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="8db81-113">第三個命令會將負載平衡器傳到 **AzureRmLoadBalancerInboundNatRuleConfig** ，這會儲存並更新入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="8db81-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="8db81-114">請注意，規則設定沒有啟用浮動 IP，而是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="8db81-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="8db81-115">參數</span><span class="sxs-lookup"><span data-stu-id="8db81-115">PARAMETERS</span></span>

### <span data-ttu-id="8db81-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8db81-116">-BackendPort</span></span>
<span data-ttu-id="8db81-117">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="8db81-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="8db81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db81-118">-DefaultProfile</span></span>
<span data-ttu-id="8db81-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8db81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db81-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8db81-120">-EnableFloatingIP</span></span>
<span data-ttu-id="8db81-121">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8db81-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8db81-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8db81-122">-EnableTcpReset</span></span>
<span data-ttu-id="8db81-123">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="8db81-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="8db81-124">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="8db81-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8db81-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8db81-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8db81-126">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="8db81-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="8db81-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8db81-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8db81-128">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="8db81-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8db81-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8db81-129">-FrontendPort</span></span>
<span data-ttu-id="8db81-130">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="8db81-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8db81-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8db81-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8db81-132">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="8db81-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8db81-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8db81-133">-LoadBalancer</span></span>
<span data-ttu-id="8db81-134">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8db81-134">Specifies a load balancer.</span></span>
<span data-ttu-id="8db81-135">這個 Cmdlet 為此參數指定的負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="8db81-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8db81-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="8db81-136">-Name</span></span>
<span data-ttu-id="8db81-137">指定入站 NAT 規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8db81-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="8db81-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="8db81-138">-Protocol</span></span>
<span data-ttu-id="8db81-139">指定與入站 NAT 規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8db81-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="8db81-140">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="8db81-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="8db81-141">-確認</span><span class="sxs-lookup"><span data-stu-id="8db81-141">-Confirm</span></span>
<span data-ttu-id="8db81-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8db81-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db81-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db81-143">-WhatIf</span></span>
<span data-ttu-id="8db81-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8db81-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db81-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8db81-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db81-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db81-146">CommonParameters</span></span>
<span data-ttu-id="8db81-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8db81-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db81-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8db81-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db81-149">輸入</span><span class="sxs-lookup"><span data-stu-id="8db81-149">INPUTS</span></span>

### <span data-ttu-id="8db81-150">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8db81-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="8db81-151">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8db81-151">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="8db81-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8db81-152">OUTPUTS</span></span>

### <span data-ttu-id="8db81-153">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8db81-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8db81-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8db81-154">NOTES</span></span>

## <span data-ttu-id="8db81-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8db81-155">RELATED LINKS</span></span>

[<span data-ttu-id="8db81-156">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8db81-156">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8db81-157">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8db81-157">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="8db81-158">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8db81-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8db81-159">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8db81-159">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8db81-160">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8db81-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


