---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136342"
---
# <span data-ttu-id="9e78b-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9e78b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e78b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e78b-103">在負載平衡器中新增前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="9e78b-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="9e78b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e78b-104">SYNTAX</span></span>

### <span data-ttu-id="9e78b-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="9e78b-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e78b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9e78b-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e78b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e78b-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e78b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e78b-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e78b-109">說明</span><span class="sxs-lookup"><span data-stu-id="9e78b-109">DESCRIPTION</span></span>
<span data-ttu-id="9e78b-110">**AzLoadBalancerFrontendIpConfig** Cmdlet 會將前端 IP 配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="9e78b-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="9e78b-111">示例</span><span class="sxs-lookup"><span data-stu-id="9e78b-111">EXAMPLES</span></span>

### <span data-ttu-id="9e78b-112">範例1使用動態 IP 位址新增前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="9e78b-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="9e78b-113">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="9e78b-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="9e78b-114">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9e78b-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="9e78b-115">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $MySubnet 的變數中所儲存之子網上的動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9e78b-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="9e78b-116">範例2使用靜態 IP 位址新增前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="9e78b-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="9e78b-117">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="9e78b-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="9e78b-118">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9e78b-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="9e78b-119">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $Subnet 的變數中所儲存之子網上的靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9e78b-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="9e78b-120">範例3新增含公用 IP 位址的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="9e78b-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="9e78b-121">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並將結果儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9e78b-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="9e78b-122">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $PublicIp 變數中的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9e78b-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="9e78b-123">參數</span><span class="sxs-lookup"><span data-stu-id="9e78b-123">PARAMETERS</span></span>

### <span data-ttu-id="9e78b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e78b-124">-DefaultProfile</span></span>
<span data-ttu-id="9e78b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e78b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e78b-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9e78b-126">-LoadBalancer</span></span>
<span data-ttu-id="9e78b-127">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="9e78b-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="9e78b-128">這個 Cmdlet 會將前端 IP 設定新增至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="9e78b-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e78b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e78b-129">-Name</span></span>
<span data-ttu-id="9e78b-130">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="9e78b-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="9e78b-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e78b-131">-PrivateIpAddress</span></span>
<span data-ttu-id="9e78b-132">指定要與前端 IP 配置相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9e78b-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9e78b-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9e78b-134">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="9e78b-134">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e78b-135">-PublicIpAddress</span></span>
<span data-ttu-id="9e78b-136">指定要與前端 IP 設定關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9e78b-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9e78b-137">-PublicIpAddressId</span></span>
<span data-ttu-id="9e78b-138">指定要在其中新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e78b-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-139">-子網</span><span class="sxs-lookup"><span data-stu-id="9e78b-139">-Subnet</span></span>
<span data-ttu-id="9e78b-140">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="9e78b-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9e78b-141">-SubnetId</span></span>
<span data-ttu-id="9e78b-142">指定要在其中新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e78b-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9e78b-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e78b-143">-Zone</span></span>
<span data-ttu-id="9e78b-144">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="9e78b-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9e78b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="9e78b-145">-Confirm</span></span>
<span data-ttu-id="9e78b-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e78b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e78b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e78b-147">-WhatIf</span></span>
<span data-ttu-id="9e78b-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e78b-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e78b-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e78b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e78b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e78b-150">CommonParameters</span></span>
<span data-ttu-id="9e78b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e78b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e78b-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e78b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e78b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="9e78b-153">INPUTS</span></span>

### <span data-ttu-id="9e78b-154">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e78b-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9e78b-155">System.object</span><span class="sxs-lookup"><span data-stu-id="9e78b-155">System.String</span></span>

### <span data-ttu-id="9e78b-156">System.object []</span><span class="sxs-lookup"><span data-stu-id="9e78b-156">System.String[]</span></span>

### <span data-ttu-id="9e78b-157">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e78b-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="9e78b-158">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e78b-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9e78b-159">輸出</span><span class="sxs-lookup"><span data-stu-id="9e78b-159">OUTPUTS</span></span>

### <span data-ttu-id="9e78b-160">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e78b-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9e78b-161">筆記</span><span class="sxs-lookup"><span data-stu-id="9e78b-161">NOTES</span></span>

## <span data-ttu-id="9e78b-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e78b-162">RELATED LINKS</span></span>

[<span data-ttu-id="9e78b-163">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9e78b-164">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e78b-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9e78b-165">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e78b-166">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9e78b-167">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9e78b-168">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e78b-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

