---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: 423061d4aeaba16d0edf6bbe122f9fbe3f078218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625994"
---
# <span data-ttu-id="c41b1-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c41b1-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="c41b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c41b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c41b1-103">建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c41b1-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c41b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c41b1-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c41b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="c41b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c41b1-106">**新的-AzureRmLoadBalancer** Cmdlet 會建立 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c41b1-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="c41b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="c41b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c41b1-108">範例1：建立負載平衡器</span><span class="sxs-lookup"><span data-stu-id="c41b1-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="c41b1-109">部署負載平衡器需要您先建立數個物件，且前七個命令會示範如何建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="c41b1-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="c41b1-110">第八個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c41b1-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="c41b1-111">第九個和最後一個命令會取得新的負載平衡器，以確保它已成功建立。</span><span class="sxs-lookup"><span data-stu-id="c41b1-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="c41b1-112">請注意，這個範例只顯示如何建立負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c41b1-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="c41b1-113">您也必須使用 Add-AzureRmNetworkInterfaceIpConfig Cmdlet 來設定它，才能將 Nic 指派給不同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c41b1-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="c41b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="c41b1-114">PARAMETERS</span></span>

### <span data-ttu-id="c41b1-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c41b1-115">-BackendAddressPool</span></span>
<span data-ttu-id="c41b1-116">指定要與負載平衡器建立關聯的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="c41b1-116">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c41b1-117">-Force</span></span>
<span data-ttu-id="c41b1-118">指示這個 Cmdlet 會建立負載平衡器，即使已存在相同名稱的負載平衡器也一樣。</span><span class="sxs-lookup"><span data-stu-id="c41b1-118">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="c41b1-119">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c41b1-119">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c41b1-120">指定要與負載平衡器相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="c41b1-120">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-121">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c41b1-121">-InboundNatPool</span></span>
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

### <span data-ttu-id="c41b1-122">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c41b1-122">-InboundNatRule</span></span>
<span data-ttu-id="c41b1-123">指定輸入網路位址轉譯 (NAT) 規則的清單，以與負載平衡器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="c41b1-123">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-124">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="c41b1-124">-LoadBalancingRule</span></span>
<span data-ttu-id="c41b1-125">指定要與負載平衡器建立關聯的負載平衡規則清單。</span><span class="sxs-lookup"><span data-stu-id="c41b1-125">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-126">-位置</span><span class="sxs-lookup"><span data-stu-id="c41b1-126">-Location</span></span>
<span data-ttu-id="c41b1-127">指定要建立負載平衡器的區域。</span><span class="sxs-lookup"><span data-stu-id="c41b1-127">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="c41b1-128">-Name</span></span>
<span data-ttu-id="c41b1-129">指定此所建立的負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c41b1-129">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="c41b1-130">探測器</span><span class="sxs-lookup"><span data-stu-id="c41b1-130">-Probe</span></span>
<span data-ttu-id="c41b1-131">指定要與負載平衡器建立關聯的探測器清單。</span><span class="sxs-lookup"><span data-stu-id="c41b1-131">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41b1-132">-ResourceGroupName</span></span>
<span data-ttu-id="c41b1-133">指定要建立負載平衡器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c41b1-133">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="c41b1-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="c41b1-134">-Sku</span></span>
<span data-ttu-id="c41b1-135">負載平衡器 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="c41b1-135">The load balancer Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41b1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="c41b1-136">-Tag</span></span>
<span data-ttu-id="c41b1-137">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c41b1-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c41b1-138">例如：</span><span class="sxs-lookup"><span data-stu-id="c41b1-138">For example:</span></span>

<span data-ttu-id="c41b1-139">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c41b1-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c41b1-140">-確認</span><span class="sxs-lookup"><span data-stu-id="c41b1-140">-Confirm</span></span>
<span data-ttu-id="c41b1-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c41b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41b1-142">-WhatIf</span></span>
<span data-ttu-id="c41b1-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c41b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c41b1-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c41b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41b1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41b1-145">-DefaultProfile</span></span>
<span data-ttu-id="c41b1-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c41b1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c41b1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41b1-147">CommonParameters</span></span>
<span data-ttu-id="c41b1-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c41b1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41b1-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c41b1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41b1-150">輸入</span><span class="sxs-lookup"><span data-stu-id="c41b1-150">INPUTS</span></span>

## <span data-ttu-id="c41b1-151">輸出</span><span class="sxs-lookup"><span data-stu-id="c41b1-151">OUTPUTS</span></span>

### <span data-ttu-id="c41b1-152">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c41b1-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c41b1-153">筆記</span><span class="sxs-lookup"><span data-stu-id="c41b1-153">NOTES</span></span>

## <span data-ttu-id="c41b1-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="c41b1-154">RELATED LINKS</span></span>

[<span data-ttu-id="c41b1-155">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c41b1-155">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c41b1-156">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c41b1-156">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c41b1-157">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c41b1-157">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="c41b1-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c41b1-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
