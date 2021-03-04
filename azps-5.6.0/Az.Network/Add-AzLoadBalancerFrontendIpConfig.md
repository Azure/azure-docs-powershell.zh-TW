---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d68c4329eee7c75889db48fb55772bf903417170
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901997"
---
# <span data-ttu-id="f5518-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f5518-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5518-102">SYNOPSIS</span></span>
<span data-ttu-id="f5518-103">新增前端 IP 組配置至負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f5518-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="f5518-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5518-104">SYNTAX</span></span>

### <span data-ttu-id="f5518-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5518-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5518-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f5518-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5518-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5518-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5518-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5518-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5518-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f5518-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5518-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f5518-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5518-111">描述</span><span class="sxs-lookup"><span data-stu-id="f5518-111">DESCRIPTION</span></span>
<span data-ttu-id="f5518-112">**Add-AzLoadBalancerFrontendIpConfig** Cmdlet 會新增前端 IP 組配置至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f5518-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f5518-113">例子</span><span class="sxs-lookup"><span data-stu-id="f5518-113">EXAMPLES</span></span>

### <span data-ttu-id="f5518-114">範例 1 使用動態 IP 位址新增前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="f5518-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="f5518-115">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，然後使用管線將結果傳遞給 **Get-AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="f5518-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f5518-116">命令接著會將結果儲存在名為 $Subnet。</span><span class="sxs-lookup"><span data-stu-id="f5518-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f5518-117">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給 **Add-AzLoadBalancerFrontendIpConfig** Cmdlet，此 Cmdlet 會新增前端 IP 組配置至負載平衡器，並包含儲存在變數 $MySubnet 中的子網動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5518-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="f5518-118">範例 2 使用靜態 IP 位址新增前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="f5518-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="f5518-119">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，然後使用管線將結果傳遞給 **Get-AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="f5518-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="f5518-120">命令接著會將結果儲存在名為 $Subnet。</span><span class="sxs-lookup"><span data-stu-id="f5518-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="f5518-121">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞至 **Add-AzLoadBalancerFrontendIpConfig** Cmdlet，此 Cmdlet 會將前端 IP 組配置新增到負載平衡器，並包含儲存在變數 $Subnet 中的子網之靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5518-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="f5518-122">範例 3 使用公用 IP 位址新增前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="f5518-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="f5518-123">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並儲存在名為 myPub 的變數$PublicIp。</span><span class="sxs-lookup"><span data-stu-id="f5518-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="f5518-124">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞至 **Add-AzLoadBalancerFrontendIpConfig** Cmdlet，此 Cmdlet 會將前端 IP 組配置新增到載入平衡器，並將公用 IP 位址儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f5518-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="f5518-125">範例 4 新增具有公用 IP 首碼的前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="f5518-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="f5518-126">第一個命令會取得名為 MyPubPrefix 的 Azure 公用 IP 首碼，並儲存在名為 myPubPrefix 的變數$PublicIpPrefix。</span><span class="sxs-lookup"><span data-stu-id="f5518-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="f5518-127">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞至 **Add-AzLoadBalancerFrontendIpConfig** Cmdlet，此 Cmdlet 會將前端 IP 組配置新增到負載平衡器，並將公用 IP 首碼儲存在名為 $PublicIpPrefix 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f5518-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="f5518-128">參數</span><span class="sxs-lookup"><span data-stu-id="f5518-128">PARAMETERS</span></span>

### <span data-ttu-id="f5518-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5518-129">-DefaultProfile</span></span>
<span data-ttu-id="f5518-130">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5518-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5518-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5518-131">-LoadBalancer</span></span>
<span data-ttu-id="f5518-132">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="f5518-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f5518-133">此 Cmdlet 會新增前端 IP 設定至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f5518-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5518-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5518-134">-Name</span></span>
<span data-ttu-id="f5518-135">指定要新增的前端 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="f5518-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="f5518-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5518-136">-PrivateIpAddress</span></span>
<span data-ttu-id="f5518-137">指定要與前端 IP 群組原則關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5518-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f5518-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f5518-139">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="f5518-139">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="f5518-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5518-140">-PublicIpAddress</span></span>
<span data-ttu-id="f5518-141">指定要與前端 IP 群組原則關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f5518-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f5518-142">-PublicIpAddressId</span></span>
<span data-ttu-id="f5518-143">指定要新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5518-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f5518-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="f5518-145">指定要與前端 IP 群組原則關聯的公用 IP 位址前置詞物件。</span><span class="sxs-lookup"><span data-stu-id="f5518-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="f5518-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="f5518-147">指定要與前端 IP 群組原則關聯的公用 IP 位址前置詞物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5518-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-148">-子網</span><span class="sxs-lookup"><span data-stu-id="f5518-148">-Subnet</span></span>
<span data-ttu-id="f5518-149">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="f5518-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-150">-子網Id</span><span class="sxs-lookup"><span data-stu-id="f5518-150">-SubnetId</span></span>
<span data-ttu-id="f5518-151">指定要新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5518-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f5518-152">-區域</span><span class="sxs-lookup"><span data-stu-id="f5518-152">-Zone</span></span>
<span data-ttu-id="f5518-153">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="f5518-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f5518-154">-確認</span><span class="sxs-lookup"><span data-stu-id="f5518-154">-Confirm</span></span>
<span data-ttu-id="f5518-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5518-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5518-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5518-156">-WhatIf</span></span>
<span data-ttu-id="f5518-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5518-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5518-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5518-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5518-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5518-159">CommonParameters</span></span>
<span data-ttu-id="f5518-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5518-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5518-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5518-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5518-162">輸入</span><span class="sxs-lookup"><span data-stu-id="f5518-162">INPUTS</span></span>

### <span data-ttu-id="f5518-163">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5518-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f5518-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f5518-164">System.String</span></span>

### <span data-ttu-id="f5518-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f5518-165">System.String[]</span></span>

### <span data-ttu-id="f5518-166">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f5518-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f5518-167">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5518-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f5518-168">輸出</span><span class="sxs-lookup"><span data-stu-id="f5518-168">OUTPUTS</span></span>

### <span data-ttu-id="f5518-169">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5518-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f5518-170">筆記</span><span class="sxs-lookup"><span data-stu-id="f5518-170">NOTES</span></span>

## <span data-ttu-id="f5518-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5518-171">RELATED LINKS</span></span>

[<span data-ttu-id="f5518-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f5518-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f5518-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f5518-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f5518-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f5518-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f5518-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5518-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


