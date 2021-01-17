---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450134"
---
# <span data-ttu-id="12b40-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b40-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="12b40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12b40-102">SYNOPSIS</span></span>
<span data-ttu-id="12b40-103">更新負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="12b40-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="12b40-104">句法</span><span class="sxs-lookup"><span data-stu-id="12b40-104">SYNTAX</span></span>

### <span data-ttu-id="12b40-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="12b40-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b40-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="12b40-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b40-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12b40-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12b40-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12b40-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12b40-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="12b40-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12b40-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="12b40-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12b40-111">說明</span><span class="sxs-lookup"><span data-stu-id="12b40-111">DESCRIPTION</span></span>
<span data-ttu-id="12b40-112">**AzLoadBalancerFrontendIpConfig** Cmdlet 會更新負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="12b40-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="12b40-113">示例</span><span class="sxs-lookup"><span data-stu-id="12b40-113">EXAMPLES</span></span>

### <span data-ttu-id="12b40-114">範例1：修改負載平衡器的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="12b40-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="12b40-115">第一個命令會取得名為 Subnet 的虛擬子網，然後將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="12b40-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="12b40-116">第二個命令會取得名為 MyLoadBalancer 的關聯負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="12b40-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="12b40-117">第三個命令使用管線運算子，將負載平衡器傳送 $slb 至 AzLoadBalancerFrontendIpConfig，這會建立名為 NewFrontend $slb 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="12b40-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="12b40-118">第四個命令會將負載平衡器 $slb **設定為 AzLoadBalancerFrontendIpConfig**，這會儲存並更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="12b40-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="12b40-119">參數</span><span class="sxs-lookup"><span data-stu-id="12b40-119">PARAMETERS</span></span>

### <span data-ttu-id="12b40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b40-120">-DefaultProfile</span></span>
<span data-ttu-id="12b40-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12b40-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b40-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12b40-122">-LoadBalancer</span></span>
<span data-ttu-id="12b40-123">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="12b40-123">Specifies a load balancer.</span></span>
<span data-ttu-id="12b40-124">這個 Cmdlet 會針對此參數指定的負載平衡器更新前端設定。</span><span class="sxs-lookup"><span data-stu-id="12b40-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="12b40-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="12b40-125">-Name</span></span>
<span data-ttu-id="12b40-126">指定要設定的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="12b40-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="12b40-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="12b40-127">-PrivateIpAddress</span></span>
<span data-ttu-id="12b40-128">指定與要設定的前端 IP 設定相關聯之負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="12b40-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="12b40-129">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="12b40-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="12b40-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="12b40-131">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="12b40-131">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="12b40-132">-PublicIpAddress</span></span>
<span data-ttu-id="12b40-133">指定與要設定的前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="12b40-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="12b40-134">-PublicIpAddressId</span></span>
<span data-ttu-id="12b40-135">指定與這個 Cmdlet 所設定之前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="12b40-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="12b40-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="12b40-137">指定要與前端 IP 配置相關聯的 **PublicIpAddressPrefix** 物件。</span><span class="sxs-lookup"><span data-stu-id="12b40-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="12b40-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="12b40-139">指定要與前端 IP 設定相關聯之 **PublicIpAddressPrefix** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="12b40-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-140">-子網</span><span class="sxs-lookup"><span data-stu-id="12b40-140">-Subnet</span></span>
<span data-ttu-id="12b40-141">指定包含此 Cmdlet 所設定之前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="12b40-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="12b40-142">-SubnetId</span></span>
<span data-ttu-id="12b40-143">指定包含此 Cmdlet 所設定之前端 IP 配置的子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="12b40-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="12b40-144">-Zone</span></span>
<span data-ttu-id="12b40-145">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="12b40-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b40-146">-確認</span><span class="sxs-lookup"><span data-stu-id="12b40-146">-Confirm</span></span>
<span data-ttu-id="12b40-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12b40-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b40-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b40-148">-WhatIf</span></span>
<span data-ttu-id="12b40-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12b40-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12b40-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12b40-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b40-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b40-151">CommonParameters</span></span>
<span data-ttu-id="12b40-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12b40-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b40-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12b40-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b40-154">輸入</span><span class="sxs-lookup"><span data-stu-id="12b40-154">INPUTS</span></span>

### <span data-ttu-id="12b40-155">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12b40-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="12b40-156">System.object</span><span class="sxs-lookup"><span data-stu-id="12b40-156">System.String</span></span>

### <span data-ttu-id="12b40-157">System.object []</span><span class="sxs-lookup"><span data-stu-id="12b40-157">System.String[]</span></span>

### <span data-ttu-id="12b40-158">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12b40-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="12b40-159">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12b40-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="12b40-160">輸出</span><span class="sxs-lookup"><span data-stu-id="12b40-160">OUTPUTS</span></span>

### <span data-ttu-id="12b40-161">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12b40-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12b40-162">筆記</span><span class="sxs-lookup"><span data-stu-id="12b40-162">NOTES</span></span>

## <span data-ttu-id="12b40-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="12b40-163">RELATED LINKS</span></span>

[<span data-ttu-id="12b40-164">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b40-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="12b40-165">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12b40-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="12b40-166">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b40-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="12b40-167">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12b40-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="12b40-168">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b40-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="12b40-169">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="12b40-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


