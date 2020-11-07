---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801622"
---
# <span data-ttu-id="bbd47-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd47-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="bbd47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbd47-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd47-103">在負載平衡器中新增規則配置。</span><span class="sxs-lookup"><span data-stu-id="bbd47-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd47-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbd47-104">SYNTAX</span></span>

### <span data-ttu-id="bbd47-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd47-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbd47-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bbd47-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd47-107">說明</span><span class="sxs-lookup"><span data-stu-id="bbd47-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd47-108">**AzureRmLoadBalancerRuleConfig** Cmdlet 會將規則配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbd47-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bbd47-109">示例</span><span class="sxs-lookup"><span data-stu-id="bbd47-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd47-110">範例1：在負載平衡器中新增規則配置</span><span class="sxs-lookup"><span data-stu-id="bbd47-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="bbd47-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bbd47-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="bbd47-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzureRmLoadBalancerRuleConfig** ，這會新增名為 NewRule 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="bbd47-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="bbd47-113">參數</span><span class="sxs-lookup"><span data-stu-id="bbd47-113">PARAMETERS</span></span>

### <span data-ttu-id="bbd47-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbd47-114">-BackendAddressPool</span></span>
<span data-ttu-id="bbd47-115">指定要與負載平衡器規則配置相關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="bbd47-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bbd47-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="bbd47-117">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbd47-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bbd47-118">-BackendPort</span></span>
<span data-ttu-id="bbd47-119">指定與負載平衡器規則設定相符的流量後端埠。</span><span class="sxs-lookup"><span data-stu-id="bbd47-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd47-120">-DefaultProfile</span></span>
<span data-ttu-id="bbd47-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbd47-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd47-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="bbd47-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="bbd47-123">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="bbd47-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="bbd47-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bbd47-124">-EnableFloatingIP</span></span>
<span data-ttu-id="bbd47-125">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bbd47-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd47-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bbd47-127">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="bbd47-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bbd47-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bbd47-129">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="bbd47-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bbd47-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bbd47-130">-FrontendPort</span></span>
<span data-ttu-id="bbd47-131">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="bbd47-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bbd47-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bbd47-133">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbd47-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="bbd47-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbd47-134">-LoadBalancer</span></span>
<span data-ttu-id="bbd47-135">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="bbd47-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="bbd47-136">這個 Cmdlet 會將規則配置新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbd47-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbd47-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="bbd47-137">-LoadDistribution</span></span>
<span data-ttu-id="bbd47-138">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="bbd47-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="bbd47-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbd47-139">-Name</span></span>
<span data-ttu-id="bbd47-140">指定負載平衡器規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbd47-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-141">探測器</span><span class="sxs-lookup"><span data-stu-id="bbd47-141">-Probe</span></span>
<span data-ttu-id="bbd47-142">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="bbd47-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="bbd47-143">-ProbeId</span></span>
<span data-ttu-id="bbd47-144">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbd47-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbd47-145">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbd47-145">-Protocol</span></span>
<span data-ttu-id="bbd47-146">Specfies 負載平衡器規則所相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bbd47-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="bbd47-147">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="bbd47-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="bbd47-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd47-148">CommonParameters</span></span>
<span data-ttu-id="bbd47-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbd47-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd47-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbd47-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd47-151">輸入</span><span class="sxs-lookup"><span data-stu-id="bbd47-151">INPUTS</span></span>

### <span data-ttu-id="bbd47-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbd47-152">PSLoadBalancer</span></span>
<span data-ttu-id="bbd47-153">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bbd47-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bbd47-154">輸出</span><span class="sxs-lookup"><span data-stu-id="bbd47-154">OUTPUTS</span></span>

### <span data-ttu-id="bbd47-155">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbd47-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbd47-156">筆記</span><span class="sxs-lookup"><span data-stu-id="bbd47-156">NOTES</span></span>

## <span data-ttu-id="bbd47-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbd47-157">RELATED LINKS</span></span>

[<span data-ttu-id="bbd47-158">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbd47-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bbd47-159">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd47-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbd47-160">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd47-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbd47-161">移除-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd47-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbd47-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd47-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


