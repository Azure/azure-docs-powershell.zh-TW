---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128862"
---
# <span data-ttu-id="54c82-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54c82-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="54c82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54c82-102">SYNOPSIS</span></span>
<span data-ttu-id="54c82-103">建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-103">Creates a load balancer.</span></span>

## <span data-ttu-id="54c82-104">句法</span><span class="sxs-lookup"><span data-stu-id="54c82-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c82-105">說明</span><span class="sxs-lookup"><span data-stu-id="54c82-105">DESCRIPTION</span></span>
<span data-ttu-id="54c82-106">**新的-AzLoadBalancer** Cmdlet 會建立 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="54c82-107">示例</span><span class="sxs-lookup"><span data-stu-id="54c82-107">EXAMPLES</span></span>

### <span data-ttu-id="54c82-108">範例1：建立負載平衡器</span><span class="sxs-lookup"><span data-stu-id="54c82-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="54c82-109">部署負載平衡器需要您先建立數個物件，且前七個命令會示範如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="54c82-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="54c82-110">第八個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="54c82-111">第九個和最後一個命令會取得新的負載平衡器，以確保它已成功建立。</span><span class="sxs-lookup"><span data-stu-id="54c82-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="54c82-112">請注意，這個範例只顯示如何建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="54c82-113">您也必須使用 Add-AzNetworkInterfaceIpConfig Cmdlet 來設定它，才能將 Nic 指派給不同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="54c82-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="54c82-114">範例2：建立全域負載平衡器</span><span class="sxs-lookup"><span data-stu-id="54c82-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="54c82-115">若要部署全域負載平衡器，您必須先建立多個物件，且前五個命令會示範如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="54c82-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="54c82-116">第六個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="54c82-117">第七個與最後一個命令會取得新的負載平衡器，以確保它已成功建立。</span><span class="sxs-lookup"><span data-stu-id="54c82-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="54c82-118">請注意，這個範例只顯示如何建立全域負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="54c82-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="54c82-119">您也必須使用 New-AzLoadBalancerBackendAddressConfig Cmdlet 來設定它，才能將區域負載等化器前端 ipconfig id 指派給它的後端位址集區</span><span class="sxs-lookup"><span data-stu-id="54c82-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="54c82-120">參數</span><span class="sxs-lookup"><span data-stu-id="54c82-120">PARAMETERS</span></span>

### <span data-ttu-id="54c82-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c82-121">-AsJob</span></span>
<span data-ttu-id="54c82-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54c82-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54c82-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54c82-123">-BackendAddressPool</span></span>
<span data-ttu-id="54c82-124">指定要與負載平衡器建立關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="54c82-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c82-125">-DefaultProfile</span></span>
<span data-ttu-id="54c82-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54c82-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c82-127">-Force</span><span class="sxs-lookup"><span data-stu-id="54c82-127">-Force</span></span>
<span data-ttu-id="54c82-128">指示這個 Cmdlet 會建立負載平衡器，即使已存在相同名稱的負載平衡器也一樣。</span><span class="sxs-lookup"><span data-stu-id="54c82-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="54c82-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="54c82-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="54c82-130">指定要與負載平衡器相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="54c82-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="54c82-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="54c82-132">-InboundNatRule</span></span>
<span data-ttu-id="54c82-133">指定輸入網路位址轉譯 (NAT) 規則的清單，以與負載平衡器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="54c82-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="54c82-134">-LoadBalancingRule</span></span>
<span data-ttu-id="54c82-135">指定要與負載平衡器建立關聯的負載平衡規則清單。</span><span class="sxs-lookup"><span data-stu-id="54c82-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-136">-位置</span><span class="sxs-lookup"><span data-stu-id="54c82-136">-Location</span></span>
<span data-ttu-id="54c82-137">指定要建立負載平衡器的區域。</span><span class="sxs-lookup"><span data-stu-id="54c82-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="54c82-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="54c82-138">-Name</span></span>
<span data-ttu-id="54c82-139">指定此所建立的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c82-139">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="54c82-140">-OutboundRule</span></span>
<span data-ttu-id="54c82-141">輸出規則。</span><span class="sxs-lookup"><span data-stu-id="54c82-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-142">探測器</span><span class="sxs-lookup"><span data-stu-id="54c82-142">-Probe</span></span>
<span data-ttu-id="54c82-143">指定要與負載平衡器建立關聯的探測器清單。</span><span class="sxs-lookup"><span data-stu-id="54c82-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c82-144">-ResourceGroupName</span></span>
<span data-ttu-id="54c82-145">指定要建立負載平衡器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c82-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="54c82-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="54c82-146">-Sku</span></span>
<span data-ttu-id="54c82-147">負載平衡器 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="54c82-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="54c82-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="54c82-148">-Tag</span></span>
<span data-ttu-id="54c82-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="54c82-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54c82-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="54c82-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-151">層級</span><span class="sxs-lookup"><span data-stu-id="54c82-151">-Tier</span></span>
<span data-ttu-id="54c82-152">負載平衡器 Sku 層。</span><span class="sxs-lookup"><span data-stu-id="54c82-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="54c82-153">-確認</span><span class="sxs-lookup"><span data-stu-id="54c82-153">-Confirm</span></span>
<span data-ttu-id="54c82-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54c82-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c82-155">-WhatIf</span></span>
<span data-ttu-id="54c82-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54c82-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c82-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54c82-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c82-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c82-158">CommonParameters</span></span>
<span data-ttu-id="54c82-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54c82-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c82-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="54c82-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c82-161">輸入</span><span class="sxs-lookup"><span data-stu-id="54c82-161">INPUTS</span></span>

### <span data-ttu-id="54c82-162">System.object</span><span class="sxs-lookup"><span data-stu-id="54c82-162">System.String</span></span>

### <span data-ttu-id="54c82-163">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54c82-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="54c82-164">PSFrontendIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="54c82-165">PSBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="54c82-166">PSLoadBalancingRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="54c82-167">PSProbe [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="54c82-168">PSInboundNatRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="54c82-169">PSInboundNatPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="54c82-170">PSOutboundRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="54c82-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="54c82-171">輸出</span><span class="sxs-lookup"><span data-stu-id="54c82-171">OUTPUTS</span></span>

### <span data-ttu-id="54c82-172">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="54c82-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="54c82-173">筆記</span><span class="sxs-lookup"><span data-stu-id="54c82-173">NOTES</span></span>

## <span data-ttu-id="54c82-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="54c82-174">RELATED LINKS</span></span>

[<span data-ttu-id="54c82-175">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54c82-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54c82-176">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54c82-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="54c82-177">移除-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54c82-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="54c82-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54c82-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
