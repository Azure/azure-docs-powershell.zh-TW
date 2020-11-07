---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626375"
---
# <span data-ttu-id="ec270-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec270-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="ec270-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec270-102">SYNOPSIS</span></span>
<span data-ttu-id="ec270-103">建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ec270-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec270-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec270-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec270-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec270-105">DESCRIPTION</span></span>
<span data-ttu-id="ec270-106">**新的-AzureRmLoadBalancer** Cmdlet 會建立 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ec270-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="ec270-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec270-107">EXAMPLES</span></span>

### <span data-ttu-id="ec270-108">範例1：建立負載平衡器</span><span class="sxs-lookup"><span data-stu-id="ec270-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ec270-109">部署負載平衡器需要您先建立數個物件，且前七個命令會示範如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="ec270-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="ec270-110">第八個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ec270-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="ec270-111">第九個和最後一個命令會取得新的負載平衡器，以確保它已成功建立。</span><span class="sxs-lookup"><span data-stu-id="ec270-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="ec270-112">請注意，這個範例只顯示如何建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ec270-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="ec270-113">您也必須使用 Add-AzureRmNetworkInterfaceIpConfig Cmdlet 來設定它，才能將 Nic 指派給不同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec270-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="ec270-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec270-114">PARAMETERS</span></span>

### <span data-ttu-id="ec270-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec270-115">-AsJob</span></span>
<span data-ttu-id="ec270-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec270-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec270-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ec270-117">-BackendAddressPool</span></span>
<span data-ttu-id="ec270-118">指定要與負載平衡器建立關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="ec270-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec270-119">-DefaultProfile</span></span>
<span data-ttu-id="ec270-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec270-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec270-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ec270-121">-Force</span></span>
<span data-ttu-id="ec270-122">指示這個 Cmdlet 會建立負載平衡器，即使已存在相同名稱的負載平衡器也一樣。</span><span class="sxs-lookup"><span data-stu-id="ec270-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="ec270-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec270-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ec270-124">指定要與負載平衡器相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="ec270-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="ec270-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ec270-126">-InboundNatRule</span></span>
<span data-ttu-id="ec270-127">指定輸入網路位址轉譯 (NAT) 規則的清單，以與負載平衡器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="ec270-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="ec270-128">-LoadBalancingRule</span></span>
<span data-ttu-id="ec270-129">指定要與負載平衡器建立關聯的負載平衡規則清單。</span><span class="sxs-lookup"><span data-stu-id="ec270-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-130">-位置</span><span class="sxs-lookup"><span data-stu-id="ec270-130">-Location</span></span>
<span data-ttu-id="ec270-131">指定要建立負載平衡器的區域。</span><span class="sxs-lookup"><span data-stu-id="ec270-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="ec270-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec270-132">-Name</span></span>
<span data-ttu-id="ec270-133">指定此所建立的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec270-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="ec270-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="ec270-134">-OutboundRule</span></span>
<span data-ttu-id="ec270-135">輸出規則。</span><span class="sxs-lookup"><span data-stu-id="ec270-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-136">探測器</span><span class="sxs-lookup"><span data-stu-id="ec270-136">-Probe</span></span>
<span data-ttu-id="ec270-137">指定要與負載平衡器建立關聯的探測器清單。</span><span class="sxs-lookup"><span data-stu-id="ec270-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec270-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec270-138">-ResourceGroupName</span></span>
<span data-ttu-id="ec270-139">指定要建立負載平衡器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec270-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="ec270-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="ec270-140">-Sku</span></span>
<span data-ttu-id="ec270-141">負載平衡器 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="ec270-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="ec270-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec270-142">-Tag</span></span>
<span data-ttu-id="ec270-143">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ec270-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ec270-144">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ec270-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec270-145">-確認</span><span class="sxs-lookup"><span data-stu-id="ec270-145">-Confirm</span></span>
<span data-ttu-id="ec270-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec270-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec270-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec270-147">-WhatIf</span></span>
<span data-ttu-id="ec270-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec270-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec270-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec270-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec270-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec270-150">CommonParameters</span></span>
<span data-ttu-id="ec270-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec270-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec270-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec270-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec270-153">輸入</span><span class="sxs-lookup"><span data-stu-id="ec270-153">INPUTS</span></span>

### <span data-ttu-id="ec270-154">System.object</span><span class="sxs-lookup"><span data-stu-id="ec270-154">System.String</span></span>

### <span data-ttu-id="ec270-155">[System.object]。清單 \` 1 [PSFrontendIPConfiguration，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec270-156">[System.object]。清單 \` 1 [PSBackendAddressPool，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec270-157">[System.object]。清單 \` 1 [PSProbe，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec270-158">[System.object]。清單 \` 1 [PSInboundNatRule，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec270-159">[System.object]。清單 \` 1 [PSLoadBalancingRule，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec270-160">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec270-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ec270-161">[System.object]。清單 \` 1 [PSInboundNatPool，6.4.1.0. network，版本 =，Culture = 中性，PublicKeyToken = null]]。））））</span><span class="sxs-lookup"><span data-stu-id="ec270-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ec270-162">輸出</span><span class="sxs-lookup"><span data-stu-id="ec270-162">OUTPUTS</span></span>

### <span data-ttu-id="ec270-163">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec270-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ec270-164">筆記</span><span class="sxs-lookup"><span data-stu-id="ec270-164">NOTES</span></span>

## <span data-ttu-id="ec270-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec270-165">RELATED LINKS</span></span>

[<span data-ttu-id="ec270-166">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ec270-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ec270-167">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec270-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ec270-168">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec270-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="ec270-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec270-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
