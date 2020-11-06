---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622157"
---
# <span data-ttu-id="45219-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45219-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="45219-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45219-102">SYNOPSIS</span></span>
<span data-ttu-id="45219-103">在負載平衡器中新增前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="45219-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="45219-104">句法</span><span class="sxs-lookup"><span data-stu-id="45219-104">SYNTAX</span></span>

### <span data-ttu-id="45219-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="45219-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45219-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="45219-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45219-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="45219-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45219-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="45219-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45219-109">說明</span><span class="sxs-lookup"><span data-stu-id="45219-109">DESCRIPTION</span></span>
<span data-ttu-id="45219-110">**AzLoadBalancerFrontendIpConifg** Cmdlet 會將前端 IP 配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="45219-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="45219-111">示例</span><span class="sxs-lookup"><span data-stu-id="45219-111">EXAMPLES</span></span>

### <span data-ttu-id="45219-112">範例1使用動態 IP 位址新增前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="45219-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="45219-113">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="45219-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="45219-114">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="45219-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="45219-115">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $MySubnet 的變數中所儲存之子網上的動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45219-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="45219-116">範例2使用靜態 IP 位址新增前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="45219-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="45219-117">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="45219-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="45219-118">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="45219-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="45219-119">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $Subnet 的變數中所儲存之子網上的靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45219-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="45219-120">範例3新增含公用 IP 位址的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="45219-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="45219-121">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並將結果儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="45219-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="45219-122">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $PublicIp 變數中的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45219-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="45219-123">參數</span><span class="sxs-lookup"><span data-stu-id="45219-123">PARAMETERS</span></span>

### <span data-ttu-id="45219-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45219-124">-DefaultProfile</span></span>
<span data-ttu-id="45219-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45219-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45219-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45219-126">-LoadBalancer</span></span>
<span data-ttu-id="45219-127">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="45219-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="45219-128">這個 Cmdlet 會將前端 IP 設定新增至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="45219-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="45219-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="45219-129">-Name</span></span>
<span data-ttu-id="45219-130">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="45219-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="45219-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="45219-131">-PrivateIpAddress</span></span>
<span data-ttu-id="45219-132">指定要與前端 IP 配置相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45219-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="45219-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="45219-133">-PublicIpAddress</span></span>
<span data-ttu-id="45219-134">指定要與前端 IP 設定關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45219-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="45219-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="45219-135">-PublicIpAddressId</span></span>
<span data-ttu-id="45219-136">Specifes 要新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="45219-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="45219-137">-子網</span><span class="sxs-lookup"><span data-stu-id="45219-137">-Subnet</span></span>
<span data-ttu-id="45219-138">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="45219-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="45219-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="45219-139">-SubnetId</span></span>
<span data-ttu-id="45219-140">指定要在其中新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="45219-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="45219-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="45219-141">-Zone</span></span>
<span data-ttu-id="45219-142">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="45219-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="45219-143">-確認</span><span class="sxs-lookup"><span data-stu-id="45219-143">-Confirm</span></span>
<span data-ttu-id="45219-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45219-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45219-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45219-145">-WhatIf</span></span>
<span data-ttu-id="45219-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45219-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45219-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45219-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45219-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45219-148">CommonParameters</span></span>
<span data-ttu-id="45219-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45219-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45219-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45219-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45219-151">輸入</span><span class="sxs-lookup"><span data-stu-id="45219-151">INPUTS</span></span>

### <span data-ttu-id="45219-152">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45219-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="45219-153">System.object</span><span class="sxs-lookup"><span data-stu-id="45219-153">System.String</span></span>

### <span data-ttu-id="45219-154">System.object []</span><span class="sxs-lookup"><span data-stu-id="45219-154">System.String[]</span></span>

### <span data-ttu-id="45219-155">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45219-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="45219-156">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45219-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="45219-157">輸出</span><span class="sxs-lookup"><span data-stu-id="45219-157">OUTPUTS</span></span>

### <span data-ttu-id="45219-158">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45219-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45219-159">筆記</span><span class="sxs-lookup"><span data-stu-id="45219-159">NOTES</span></span>

## <span data-ttu-id="45219-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="45219-160">RELATED LINKS</span></span>

[<span data-ttu-id="45219-161">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45219-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="45219-162">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45219-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="45219-163">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="45219-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="45219-164">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45219-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="45219-165">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45219-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="45219-166">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45219-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


