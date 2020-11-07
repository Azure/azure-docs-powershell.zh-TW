---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 7abc575915eb65bf6c14994833bad64e6c7cd561
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801257"
---
# <span data-ttu-id="2bc8e-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bc8e-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="2bc8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc8e-103">建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bc8e-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2bc8e-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc8e-106">**新的-AzureRmLoadBalancer** Cmdlet 會建立 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="2bc8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2bc8e-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc8e-108">範例1：建立負載平衡器</span><span class="sxs-lookup"><span data-stu-id="2bc8e-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="2bc8e-109">部署負載平衡器需要您先建立數個物件，且前七個命令會示範如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="2bc8e-110">第八個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="2bc8e-111">第九個和最後一個命令會取得新的負載平衡器，以確保它已成功建立。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="2bc8e-112">請注意，這個範例只顯示如何建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="2bc8e-113">您也必須使用 Add-AzureRmNetworkInterfaceIpConfig Cmdlet 來設定它，才能將 Nic 指派給不同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="2bc8e-114">參數</span><span class="sxs-lookup"><span data-stu-id="2bc8e-114">PARAMETERS</span></span>

### <span data-ttu-id="2bc8e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bc8e-115">-AsJob</span></span>
<span data-ttu-id="2bc8e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2bc8e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bc8e-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2bc8e-117">-BackendAddressPool</span></span>
<span data-ttu-id="2bc8e-118">指定要與負載平衡器建立關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="2bc8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8e-119">-DefaultProfile</span></span>
<span data-ttu-id="2bc8e-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc8e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2bc8e-121">-Force</span></span>
<span data-ttu-id="2bc8e-122">指示這個 Cmdlet 會建立負載平衡器，即使已存在相同名稱的負載平衡器也一樣。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="2bc8e-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc8e-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2bc8e-124">指定要與負載平衡器相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="2bc8e-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="2bc8e-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="2bc8e-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2bc8e-126">-InboundNatRule</span></span>
<span data-ttu-id="2bc8e-127">指定輸入網路位址轉譯 (NAT) 規則的清單，以與負載平衡器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="2bc8e-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="2bc8e-128">-LoadBalancingRule</span></span>
<span data-ttu-id="2bc8e-129">指定要與負載平衡器建立關聯的負載平衡規則清單。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="2bc8e-130">-位置</span><span class="sxs-lookup"><span data-stu-id="2bc8e-130">-Location</span></span>
<span data-ttu-id="2bc8e-131">指定要建立負載平衡器的區域。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bc8e-132">-Name</span></span>
<span data-ttu-id="2bc8e-133">指定此所建立的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-134">探測器</span><span class="sxs-lookup"><span data-stu-id="2bc8e-134">-Probe</span></span>
<span data-ttu-id="2bc8e-135">指定要與負載平衡器建立關聯的探測器清單。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="2bc8e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc8e-136">-ResourceGroupName</span></span>
<span data-ttu-id="2bc8e-137">指定要建立負載平衡器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="2bc8e-138">-Sku</span></span>
<span data-ttu-id="2bc8e-139">負載平衡器 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="2bc8e-140">-Tag</span></span>
<span data-ttu-id="2bc8e-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2bc8e-142">例如：</span><span class="sxs-lookup"><span data-stu-id="2bc8e-142">For example:</span></span>

<span data-ttu-id="2bc8e-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2bc8e-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-144">-確認</span><span class="sxs-lookup"><span data-stu-id="2bc8e-144">-Confirm</span></span>
<span data-ttu-id="2bc8e-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc8e-146">-WhatIf</span></span>
<span data-ttu-id="2bc8e-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc8e-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc8e-149">CommonParameters</span></span>
<span data-ttu-id="2bc8e-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc8e-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bc8e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc8e-152">輸入</span><span class="sxs-lookup"><span data-stu-id="2bc8e-152">INPUTS</span></span>

## <span data-ttu-id="2bc8e-153">輸出</span><span class="sxs-lookup"><span data-stu-id="2bc8e-153">OUTPUTS</span></span>

### <span data-ttu-id="2bc8e-154">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2bc8e-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2bc8e-155">筆記</span><span class="sxs-lookup"><span data-stu-id="2bc8e-155">NOTES</span></span>

## <span data-ttu-id="2bc8e-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bc8e-156">RELATED LINKS</span></span>

[<span data-ttu-id="2bc8e-157">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2bc8e-157">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2bc8e-158">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bc8e-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2bc8e-159">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bc8e-159">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="2bc8e-160">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bc8e-160">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
