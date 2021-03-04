---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 2bc63fb21de63dc35855acad53c7e42a13caf215
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916906"
---
# <span data-ttu-id="55338-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55338-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="55338-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55338-102">SYNOPSIS</span></span>
<span data-ttu-id="55338-103">建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-103">Creates a load balancer.</span></span>

## <span data-ttu-id="55338-104">語法</span><span class="sxs-lookup"><span data-stu-id="55338-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55338-105">描述</span><span class="sxs-lookup"><span data-stu-id="55338-105">DESCRIPTION</span></span>
<span data-ttu-id="55338-106">**New-AzLoadBalancer** Cmdlet 會建立 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="55338-107">例子</span><span class="sxs-lookup"><span data-stu-id="55338-107">EXAMPLES</span></span>

### <span data-ttu-id="55338-108">範例 1：建立負載平衡器</span><span class="sxs-lookup"><span data-stu-id="55338-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="55338-109">部署負載平衡器需要您先建立多個物件，而前七個命令會顯示如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="55338-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="55338-110">第八個命令在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="55338-111">第九個及最後一個命令會取得新的負載平衡器，以確保已成功建立。</span><span class="sxs-lookup"><span data-stu-id="55338-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="55338-112">請注意，此範例只會顯示如何建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="55338-113">您也必須使用 Add-AzNetworkInterfaceIpConfig Cmdlet 進行設定，以將 NIC 指派給不同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55338-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="55338-114">範例 2：建立全域負載平衡器</span><span class="sxs-lookup"><span data-stu-id="55338-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="55338-115">部署全域負載平衡器需要您先建立多個物件，而前五個命令會顯示如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="55338-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="55338-116">第六個命令在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="55338-117">第七個及最後一個命令會取得新的負載平衡器，以確保已成功建立。</span><span class="sxs-lookup"><span data-stu-id="55338-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="55338-118">請注意，此範例只會顯示如何建立全域負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="55338-119">您也必須使用 New-AzLoadBalancerBackendAddressConfig Cmdlet 進行設定，以將地區負載平衡器 frontend ipconfig 識別碼指派至其後端位址集區</span><span class="sxs-lookup"><span data-stu-id="55338-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="55338-120">參數</span><span class="sxs-lookup"><span data-stu-id="55338-120">PARAMETERS</span></span>

### <span data-ttu-id="55338-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55338-121">-AsJob</span></span>
<span data-ttu-id="55338-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55338-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55338-123">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="55338-123">-BackendAddressPool</span></span>
<span data-ttu-id="55338-124">指定要與負載平衡器關聯的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="55338-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="55338-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55338-125">-DefaultProfile</span></span>
<span data-ttu-id="55338-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55338-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55338-127">-強制</span><span class="sxs-lookup"><span data-stu-id="55338-127">-Force</span></span>
<span data-ttu-id="55338-128">表示此 Cmdlet 會建立負載平衡器，即使已存在相同名稱的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="55338-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="55338-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="55338-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="55338-130">指定要與負載平衡器關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="55338-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="55338-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="55338-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="55338-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="55338-132">-InboundNatRule</span></span>
<span data-ttu-id="55338-133">指定 NAT 的輸入網路位址轉譯 (NAT) 與負載平衡器關聯的規則。</span><span class="sxs-lookup"><span data-stu-id="55338-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="55338-134">-LoadBalruleRule</span><span class="sxs-lookup"><span data-stu-id="55338-134">-LoadBalancingRule</span></span>
<span data-ttu-id="55338-135">指定要與負載平衡器關聯的負載平衡規則清單。</span><span class="sxs-lookup"><span data-stu-id="55338-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="55338-136">-位置</span><span class="sxs-lookup"><span data-stu-id="55338-136">-Location</span></span>
<span data-ttu-id="55338-137">指定要建立負載平衡器的區域。</span><span class="sxs-lookup"><span data-stu-id="55338-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="55338-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="55338-138">-Name</span></span>
<span data-ttu-id="55338-139">指定此建立之負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="55338-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="55338-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="55338-140">-OutboundRule</span></span>
<span data-ttu-id="55338-141">這是外發規則。</span><span class="sxs-lookup"><span data-stu-id="55338-141">The outbound rules.</span></span>

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

### <span data-ttu-id="55338-142">-進位</span><span class="sxs-lookup"><span data-stu-id="55338-142">-Probe</span></span>
<span data-ttu-id="55338-143">指定要與負載平衡器關聯的專案清單。</span><span class="sxs-lookup"><span data-stu-id="55338-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="55338-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55338-144">-ResourceGroupName</span></span>
<span data-ttu-id="55338-145">指定要建立負載平衡器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="55338-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="55338-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="55338-146">-Sku</span></span>
<span data-ttu-id="55338-147">負載平衡器 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="55338-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="55338-148">-標記</span><span class="sxs-lookup"><span data-stu-id="55338-148">-Tag</span></span>
<span data-ttu-id="55338-149">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="55338-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55338-150">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="55338-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55338-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="55338-151">-Tier</span></span>
<span data-ttu-id="55338-152">負載平衡器 SKU Tier。</span><span class="sxs-lookup"><span data-stu-id="55338-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="55338-153">-確認</span><span class="sxs-lookup"><span data-stu-id="55338-153">-Confirm</span></span>
<span data-ttu-id="55338-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55338-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55338-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55338-155">-WhatIf</span></span>
<span data-ttu-id="55338-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55338-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55338-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55338-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55338-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55338-158">CommonParameters</span></span>
<span data-ttu-id="55338-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55338-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55338-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55338-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55338-161">輸入</span><span class="sxs-lookup"><span data-stu-id="55338-161">INPUTS</span></span>

### <span data-ttu-id="55338-162">System.String</span><span class="sxs-lookup"><span data-stu-id="55338-162">System.String</span></span>

### <span data-ttu-id="55338-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="55338-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55338-164">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="55338-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="55338-165">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="55338-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="55338-166">Microsoft.Azure.Commands.Network.models.PSLoadBalrule[]</span><span class="sxs-lookup"><span data-stu-id="55338-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="55338-167">Microsoft.Azure.Commands.Network.models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="55338-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="55338-168">Microsoft.Azure.Commands.Network.models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="55338-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="55338-169">Microsoft.Azure.Commands.Network.models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="55338-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="55338-170">Microsoft.Azure.Commands.Network.models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="55338-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="55338-171">輸出</span><span class="sxs-lookup"><span data-stu-id="55338-171">OUTPUTS</span></span>

### <span data-ttu-id="55338-172">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55338-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55338-173">筆記</span><span class="sxs-lookup"><span data-stu-id="55338-173">NOTES</span></span>

## <span data-ttu-id="55338-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="55338-174">RELATED LINKS</span></span>

[<span data-ttu-id="55338-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="55338-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="55338-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55338-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="55338-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55338-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="55338-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55338-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
