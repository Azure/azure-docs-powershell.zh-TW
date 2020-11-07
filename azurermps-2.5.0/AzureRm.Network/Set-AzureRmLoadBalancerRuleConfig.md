---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 59e20a557c0e32d35dd853a0b3ff7e619ec2a955
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800730"
---
# <span data-ttu-id="bc1af-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="bc1af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc1af-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1af-103">設定負載平衡器規則配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="bc1af-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc1af-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc1af-104">SYNTAX</span></span>

### <span data-ttu-id="bc1af-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc1af-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc1af-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bc1af-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc1af-107">說明</span><span class="sxs-lookup"><span data-stu-id="bc1af-107">DESCRIPTION</span></span>
<span data-ttu-id="bc1af-108">**AzureRmLoadBalancerRuleConfig** Cmdlet 會設定負載平衡器規則配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="bc1af-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="bc1af-109">示例</span><span class="sxs-lookup"><span data-stu-id="bc1af-109">EXAMPLES</span></span>

### <span data-ttu-id="bc1af-110">範例1：修改負載平衡規則配置</span><span class="sxs-lookup"><span data-stu-id="bc1af-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="bc1af-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="bc1af-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="bc1af-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerRuleConfig，這會將名為 NewRule 的規則新增至它。</span><span class="sxs-lookup"><span data-stu-id="bc1af-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="bc1af-113">第三個命令會將負載平衡器傳遞至 AzureRmLoadBalancerRuleConfig，這會設定新的規則 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="bc1af-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="bc1af-114">請注意，此設定不會啟用 [浮動 IP 位址]，這是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="bc1af-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="bc1af-115">參數</span><span class="sxs-lookup"><span data-stu-id="bc1af-115">PARAMETERS</span></span>

### <span data-ttu-id="bc1af-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc1af-116">-BackendAddressPool</span></span>
<span data-ttu-id="bc1af-117">指定要與負載平衡器規則相關聯的 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="bc1af-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc1af-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="bc1af-119">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc1af-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bc1af-120">-BackendPort</span></span>
<span data-ttu-id="bc1af-121">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="bc1af-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1af-122">-DefaultProfile</span></span>
<span data-ttu-id="bc1af-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc1af-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="bc1af-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="bc1af-125">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="bc1af-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bc1af-126">-EnableFloatingIP</span></span>
<span data-ttu-id="bc1af-127">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bc1af-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc1af-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bc1af-129">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="bc1af-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bc1af-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bc1af-131">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="bc1af-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bc1af-132">-FrontendPort</span></span>
<span data-ttu-id="bc1af-133">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="bc1af-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bc1af-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bc1af-135">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc1af-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bc1af-136">-LoadBalancer</span></span>
<span data-ttu-id="bc1af-137">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bc1af-137">Specifies a load balancer.</span></span>
<span data-ttu-id="bc1af-138">這個 Cmdlet 會針對此參數指定的負載平衡器設定目標狀態規則配置。</span><span class="sxs-lookup"><span data-stu-id="bc1af-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="bc1af-139">-LoadDistribution</span></span>
<span data-ttu-id="bc1af-140">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="bc1af-140">Specifies a load distribution.</span></span>
<span data-ttu-id="bc1af-141">此參數可接受的值為： SourceIP 和 SourceIPProtocol。</span><span class="sxs-lookup"><span data-stu-id="bc1af-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc1af-142">-Name</span></span>
<span data-ttu-id="bc1af-143">指定負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc1af-143">Specifies the name of a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-144">探測器</span><span class="sxs-lookup"><span data-stu-id="bc1af-144">-Probe</span></span>
<span data-ttu-id="bc1af-145">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="bc1af-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="bc1af-146">-ProbeId</span></span>
<span data-ttu-id="bc1af-147">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc1af-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-148">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bc1af-148">-Protocol</span></span>
<span data-ttu-id="bc1af-149">指定由負載等化器規則所相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bc1af-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="bc1af-150">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="bc1af-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1af-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1af-151">CommonParameters</span></span>
<span data-ttu-id="bc1af-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc1af-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1af-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc1af-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1af-154">輸入</span><span class="sxs-lookup"><span data-stu-id="bc1af-154">INPUTS</span></span>

### <span data-ttu-id="bc1af-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bc1af-155">PSLoadBalancer</span></span>
<span data-ttu-id="bc1af-156">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bc1af-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bc1af-157">輸出</span><span class="sxs-lookup"><span data-stu-id="bc1af-157">OUTPUTS</span></span>

### <span data-ttu-id="bc1af-158">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bc1af-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bc1af-159">筆記</span><span class="sxs-lookup"><span data-stu-id="bc1af-159">NOTES</span></span>

## <span data-ttu-id="bc1af-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc1af-160">RELATED LINKS</span></span>

[<span data-ttu-id="bc1af-161">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc1af-162">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc1af-163">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc1af-164">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bc1af-165">移除-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bc1af-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


