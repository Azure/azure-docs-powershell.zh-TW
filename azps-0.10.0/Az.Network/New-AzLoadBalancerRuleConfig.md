---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794266"
---
# <span data-ttu-id="cee23-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cee23-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="cee23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cee23-102">SYNOPSIS</span></span>
<span data-ttu-id="cee23-103">為負載平衡器建立規則配置。</span><span class="sxs-lookup"><span data-stu-id="cee23-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="cee23-104">句法</span><span class="sxs-lookup"><span data-stu-id="cee23-104">SYNTAX</span></span>

### <span data-ttu-id="cee23-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cee23-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cee23-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cee23-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee23-107">說明</span><span class="sxs-lookup"><span data-stu-id="cee23-107">DESCRIPTION</span></span>
<span data-ttu-id="cee23-108">**新的-AzLoadBalancerRuleConfig** Cmdlet 會建立 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="cee23-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cee23-109">示例</span><span class="sxs-lookup"><span data-stu-id="cee23-109">EXAMPLES</span></span>

### <span data-ttu-id="cee23-110">1：建立 Azure 負載平衡器的規則配置</span><span class="sxs-lookup"><span data-stu-id="cee23-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="cee23-111">前三個命令會在下一個命令中設定公用 IP、前端及規則配置的探測。</span><span class="sxs-lookup"><span data-stu-id="cee23-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="cee23-112">向下的命令會建立一個名為 MyLBrule 的新規則，並提供特定的規格。</span><span class="sxs-lookup"><span data-stu-id="cee23-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="cee23-113">參數</span><span class="sxs-lookup"><span data-stu-id="cee23-113">PARAMETERS</span></span>

### <span data-ttu-id="cee23-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cee23-114">-BackendAddressPool</span></span>
<span data-ttu-id="cee23-115">指定要與負載平衡器規則配置相關聯的 **BackendAddressPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="cee23-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cee23-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="cee23-117">指定要與負載平衡器規則設定相關聯之 **BackendAddressPool** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cee23-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="cee23-118">-BackendPort</span></span>
<span data-ttu-id="cee23-119">指定此負載平衡器規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="cee23-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee23-120">-DefaultProfile</span></span>
<span data-ttu-id="cee23-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cee23-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee23-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="cee23-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="cee23-123">為後端池中的虛擬機器配置 SNAT，以使用在負載平衡規則前端指定的 publicIP 位址。</span><span class="sxs-lookup"><span data-stu-id="cee23-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="cee23-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="cee23-124">-EnableFloatingIP</span></span>
<span data-ttu-id="cee23-125">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cee23-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="cee23-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cee23-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="cee23-127">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="cee23-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cee23-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="cee23-129">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="cee23-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="cee23-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="cee23-130">-FrontendPort</span></span>
<span data-ttu-id="cee23-131">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="cee23-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cee23-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="cee23-133">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="cee23-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="cee23-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="cee23-134">-LoadDistribution</span></span>
<span data-ttu-id="cee23-135">指定負載分配。</span><span class="sxs-lookup"><span data-stu-id="cee23-135">Specifies a load distribution.</span></span>
<span data-ttu-id="cee23-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cee23-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cee23-137">設置</span><span class="sxs-lookup"><span data-stu-id="cee23-137">Default</span></span>
- <span data-ttu-id="cee23-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="cee23-138">SourceIP</span></span>
- <span data-ttu-id="cee23-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="cee23-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="cee23-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="cee23-140">-Name</span></span>
<span data-ttu-id="cee23-141">指定此 Cmdlet 所建立之負載平衡規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cee23-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cee23-142">探測器</span><span class="sxs-lookup"><span data-stu-id="cee23-142">-Probe</span></span>
<span data-ttu-id="cee23-143">指定要與負載平衡器規則設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="cee23-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="cee23-144">-ProbeId</span></span>
<span data-ttu-id="cee23-145">指定要與負載平衡器規則設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="cee23-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="cee23-146">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="cee23-146">-Protocol</span></span>
<span data-ttu-id="cee23-147">指定與負載平衡器規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cee23-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="cee23-148">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="cee23-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="cee23-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee23-149">CommonParameters</span></span>
<span data-ttu-id="cee23-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cee23-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee23-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cee23-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee23-152">輸入</span><span class="sxs-lookup"><span data-stu-id="cee23-152">INPUTS</span></span>

## <span data-ttu-id="cee23-153">輸出</span><span class="sxs-lookup"><span data-stu-id="cee23-153">OUTPUTS</span></span>

### <span data-ttu-id="cee23-154">PSLoadBalancingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cee23-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="cee23-155">筆記</span><span class="sxs-lookup"><span data-stu-id="cee23-155">NOTES</span></span>

## <span data-ttu-id="cee23-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cee23-156">RELATED LINKS</span></span>

[<span data-ttu-id="cee23-157">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cee23-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cee23-158">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cee23-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cee23-159">移除-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cee23-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cee23-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cee23-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


