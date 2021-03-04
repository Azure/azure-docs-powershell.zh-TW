---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ef9121f0962cc5ba06aa9c040d4647a1365fdf80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904901"
---
# <span data-ttu-id="25a26-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="25a26-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="25a26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25a26-102">SYNOPSIS</span></span>
<span data-ttu-id="25a26-103">更新負載平衡器前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="25a26-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="25a26-104">語法</span><span class="sxs-lookup"><span data-stu-id="25a26-104">SYNTAX</span></span>

### <span data-ttu-id="25a26-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="25a26-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a26-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="25a26-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a26-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="25a26-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25a26-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="25a26-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25a26-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="25a26-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25a26-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="25a26-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25a26-111">描述</span><span class="sxs-lookup"><span data-stu-id="25a26-111">DESCRIPTION</span></span>
<span data-ttu-id="25a26-112">**Set-AzLoadBalancerFrontendIpConfig** Cmdlet 會更新負載平衡器前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="25a26-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="25a26-113">例子</span><span class="sxs-lookup"><span data-stu-id="25a26-113">EXAMPLES</span></span>

### <span data-ttu-id="25a26-114">範例 1：修改負載平衡器前端 IP 組式</span><span class="sxs-lookup"><span data-stu-id="25a26-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="25a26-115">第一個命令會獲得名為子網的虛擬子網，然後將它儲存在$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="25a26-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="25a26-116">第二個命令會取得名為 MyLoadBalancer 的關聯負載平衡器，然後將它儲存在$slb變數中。</span><span class="sxs-lookup"><span data-stu-id="25a26-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="25a26-117">第三個命令使用管線運算子，將 $slb 中的負載平衡器傳遞到 Add-AzLoadBalancerFrontendIpConfig，這可建立名為 NewFrontend for $slb 的前端 IP 組$slb。</span><span class="sxs-lookup"><span data-stu-id="25a26-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="25a26-118">第四個命令會將 $slb 中的負載平衡器傳遞至 **Set-AzLoadBalancerFrontendIpConfig，** 以節省及更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="25a26-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="25a26-119">參數</span><span class="sxs-lookup"><span data-stu-id="25a26-119">PARAMETERS</span></span>

### <span data-ttu-id="25a26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a26-120">-DefaultProfile</span></span>
<span data-ttu-id="25a26-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25a26-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25a26-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25a26-122">-LoadBalancer</span></span>
<span data-ttu-id="25a26-123">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="25a26-123">Specifies a load balancer.</span></span>
<span data-ttu-id="25a26-124">此 Cmdlet 會更新此參數指定的負載平衡器前端設定。</span><span class="sxs-lookup"><span data-stu-id="25a26-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="25a26-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="25a26-125">-Name</span></span>
<span data-ttu-id="25a26-126">指定要設定前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="25a26-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="25a26-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="25a26-127">-PrivateIpAddress</span></span>
<span data-ttu-id="25a26-128">指定要設定前端 IP 設定之負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="25a26-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="25a26-129">只有在您同時指定子網參數時，才指定 *此* 參數。</span><span class="sxs-lookup"><span data-stu-id="25a26-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="25a26-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="25a26-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="25a26-131">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="25a26-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="25a26-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="25a26-132">-PublicIpAddress</span></span>
<span data-ttu-id="25a26-133">指定要設定與前端 IP 設定相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="25a26-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="25a26-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="25a26-134">-PublicIpAddressId</span></span>
<span data-ttu-id="25a26-135">指定與此 Cmdlet 所設定之前端 IP 設定相關聯的 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="25a26-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="25a26-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="25a26-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="25a26-137">指定要與前端 IP 群組原則關聯的 **PublicIpAddressPrefix** 物件。</span><span class="sxs-lookup"><span data-stu-id="25a26-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="25a26-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="25a26-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="25a26-139">指定要與前端 IP 群組原則關聯的 **PublicIpAddressPrefix** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="25a26-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="25a26-140">-子網</span><span class="sxs-lookup"><span data-stu-id="25a26-140">-Subnet</span></span>
<span data-ttu-id="25a26-141">指定 **包含此** Cmdlet 所設定之前端 IP 設定之子網物件。</span><span class="sxs-lookup"><span data-stu-id="25a26-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="25a26-142">-子網Id</span><span class="sxs-lookup"><span data-stu-id="25a26-142">-SubnetId</span></span>
<span data-ttu-id="25a26-143">指定包含此 Cmdlet 所設定之前端 IP 設定之子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="25a26-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="25a26-144">-區域</span><span class="sxs-lookup"><span data-stu-id="25a26-144">-Zone</span></span>
<span data-ttu-id="25a26-145">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="25a26-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="25a26-146">-確認</span><span class="sxs-lookup"><span data-stu-id="25a26-146">-Confirm</span></span>
<span data-ttu-id="25a26-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="25a26-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a26-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a26-148">-WhatIf</span></span>
<span data-ttu-id="25a26-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25a26-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25a26-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25a26-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a26-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a26-151">CommonParameters</span></span>
<span data-ttu-id="25a26-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25a26-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a26-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25a26-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a26-154">輸入</span><span class="sxs-lookup"><span data-stu-id="25a26-154">INPUTS</span></span>

### <span data-ttu-id="25a26-155">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25a26-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="25a26-156">System.String</span><span class="sxs-lookup"><span data-stu-id="25a26-156">System.String</span></span>

### <span data-ttu-id="25a26-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="25a26-157">System.String[]</span></span>

### <span data-ttu-id="25a26-158">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="25a26-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="25a26-159">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="25a26-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="25a26-160">輸出</span><span class="sxs-lookup"><span data-stu-id="25a26-160">OUTPUTS</span></span>

### <span data-ttu-id="25a26-161">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25a26-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="25a26-162">筆記</span><span class="sxs-lookup"><span data-stu-id="25a26-162">NOTES</span></span>

## <span data-ttu-id="25a26-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="25a26-163">RELATED LINKS</span></span>

[<span data-ttu-id="25a26-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="25a26-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="25a26-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25a26-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="25a26-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="25a26-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="25a26-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25a26-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="25a26-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="25a26-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="25a26-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="25a26-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


