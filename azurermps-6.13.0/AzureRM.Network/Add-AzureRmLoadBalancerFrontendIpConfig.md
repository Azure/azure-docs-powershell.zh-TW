---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446963"
---
# <span data-ttu-id="8c0f8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8c0f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0f8-103">在負載平衡器中新增前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c0f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c0f8-104">SYNTAX</span></span>

### <span data-ttu-id="8c0f8-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="8c0f8-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="8c0f8-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c0f8-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0f8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c0f8-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0f8-109">說明</span><span class="sxs-lookup"><span data-stu-id="8c0f8-109">DESCRIPTION</span></span>
<span data-ttu-id="8c0f8-110">**AzureRmLoadBalancerFrontendIpConifg** Cmdlet 會將前端 IP 配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="8c0f8-111">示例</span><span class="sxs-lookup"><span data-stu-id="8c0f8-111">EXAMPLES</span></span>

### <span data-ttu-id="8c0f8-112">範例1使用動態 IP 位址新增前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="8c0f8-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="8c0f8-113">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzureRmVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="8c0f8-114">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="8c0f8-115">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $MySubnet 的變數中所儲存之子網上的動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="8c0f8-116">範例2使用靜態 IP 位址新增前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="8c0f8-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="8c0f8-117">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzureRmVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="8c0f8-118">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="8c0f8-119">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $Subnet 的變數中所儲存之子網上的靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="8c0f8-120">範例3新增含公用 IP 位址的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="8c0f8-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="8c0f8-121">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並將結果儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="8c0f8-122">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $PublicIp 變數中的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="8c0f8-123">參數</span><span class="sxs-lookup"><span data-stu-id="8c0f8-123">PARAMETERS</span></span>

### <span data-ttu-id="8c0f8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0f8-124">-DefaultProfile</span></span>
<span data-ttu-id="8c0f8-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c0f8-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c0f8-126">-LoadBalancer</span></span>
<span data-ttu-id="8c0f8-127">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="8c0f8-128">這個 Cmdlet 會將前端 IP 設定新增至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c0f8-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c0f8-129">-Name</span></span>
<span data-ttu-id="8c0f8-130">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="8c0f8-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c0f8-131">-PrivateIpAddress</span></span>
<span data-ttu-id="8c0f8-132">指定要與前端 IP 配置相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8c0f8-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c0f8-133">-PublicIpAddress</span></span>
<span data-ttu-id="8c0f8-134">指定要與前端 IP 設定關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8c0f8-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8c0f8-135">-PublicIpAddressId</span></span>
<span data-ttu-id="8c0f8-136">Specifes 要新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8c0f8-137">-子網</span><span class="sxs-lookup"><span data-stu-id="8c0f8-137">-Subnet</span></span>
<span data-ttu-id="8c0f8-138">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8c0f8-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8c0f8-139">-SubnetId</span></span>
<span data-ttu-id="8c0f8-140">指定要在其中新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8c0f8-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="8c0f8-141">-Zone</span></span>
<span data-ttu-id="8c0f8-142">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0f8-143">-確認</span><span class="sxs-lookup"><span data-stu-id="8c0f8-143">-Confirm</span></span>
<span data-ttu-id="8c0f8-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0f8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0f8-145">-WhatIf</span></span>
<span data-ttu-id="8c0f8-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c0f8-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0f8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0f8-148">CommonParameters</span></span>
<span data-ttu-id="8c0f8-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0f8-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c0f8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0f8-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8c0f8-151">INPUTS</span></span>

### <span data-ttu-id="8c0f8-152">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="8c0f8-153">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8c0f8-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="8c0f8-154">[System.object]。清單 \` 1 [[system.object，字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8c0f8-155">輸出</span><span class="sxs-lookup"><span data-stu-id="8c0f8-155">OUTPUTS</span></span>

### <span data-ttu-id="8c0f8-156">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8c0f8-157">筆記</span><span class="sxs-lookup"><span data-stu-id="8c0f8-157">NOTES</span></span>

## <span data-ttu-id="8c0f8-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c0f8-158">RELATED LINKS</span></span>

[<span data-ttu-id="8c0f8-159">AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8c0f8-160">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8c0f8-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8c0f8-161">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8c0f8-162">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8c0f8-163">移除-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8c0f8-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


