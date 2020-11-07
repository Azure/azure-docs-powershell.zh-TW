---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794518"
---
# <span data-ttu-id="26716-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26716-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="26716-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26716-102">SYNOPSIS</span></span>
<span data-ttu-id="26716-103">在負載平衡器中新增前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="26716-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="26716-104">句法</span><span class="sxs-lookup"><span data-stu-id="26716-104">SYNTAX</span></span>

### <span data-ttu-id="26716-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="26716-105">SetByResourceSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26716-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="26716-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26716-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="26716-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26716-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="26716-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26716-109">說明</span><span class="sxs-lookup"><span data-stu-id="26716-109">DESCRIPTION</span></span>
<span data-ttu-id="26716-110">**AzLoadBalancerFrontendIpConifg** Cmdlet 會將前端 IP 配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="26716-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="26716-111">示例</span><span class="sxs-lookup"><span data-stu-id="26716-111">EXAMPLES</span></span>

### <span data-ttu-id="26716-112">範例1使用動態 IP 位址新增前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="26716-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="26716-113">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="26716-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="26716-114">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="26716-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="26716-115">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $MySubnet 的變數中所儲存之子網上的動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="26716-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="26716-116">範例2使用靜態 IP 位址新增前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="26716-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="26716-117">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="26716-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="26716-118">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="26716-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="26716-119">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $Subnet 的變數中所儲存之子網上的靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="26716-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="26716-120">範例3新增含公用 IP 位址的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="26716-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="26716-121">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並將結果儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="26716-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="26716-122">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $PublicIp 變數中的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="26716-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="26716-123">參數</span><span class="sxs-lookup"><span data-stu-id="26716-123">PARAMETERS</span></span>

### <span data-ttu-id="26716-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26716-124">-DefaultProfile</span></span>
<span data-ttu-id="26716-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26716-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26716-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26716-126">-LoadBalancer</span></span>
<span data-ttu-id="26716-127">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="26716-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="26716-128">這個 Cmdlet 會將前端 IP 設定新增至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="26716-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26716-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="26716-129">-Name</span></span>
<span data-ttu-id="26716-130">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="26716-130">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="26716-131">-PrivateIpAddress</span></span>
<span data-ttu-id="26716-132">指定要與前端 IP 配置相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="26716-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="26716-133">-PublicIpAddress</span></span>
<span data-ttu-id="26716-134">指定要與前端 IP 設定關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="26716-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="26716-135">-PublicIpAddressId</span></span>
<span data-ttu-id="26716-136">Specifes 要新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="26716-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-137">-子網</span><span class="sxs-lookup"><span data-stu-id="26716-137">-Subnet</span></span>
<span data-ttu-id="26716-138">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="26716-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="26716-139">-SubnetId</span></span>
<span data-ttu-id="26716-140">指定要在其中新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="26716-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26716-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="26716-141">-Zone</span></span>
<span data-ttu-id="26716-142">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="26716-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="26716-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26716-143">CommonParameters</span></span>
<span data-ttu-id="26716-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26716-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26716-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26716-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26716-146">輸入</span><span class="sxs-lookup"><span data-stu-id="26716-146">INPUTS</span></span>

### <span data-ttu-id="26716-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26716-147">PSLoadBalancer</span></span>
<span data-ttu-id="26716-148">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="26716-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="26716-149">輸出</span><span class="sxs-lookup"><span data-stu-id="26716-149">OUTPUTS</span></span>

### <span data-ttu-id="26716-150">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26716-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26716-151">筆記</span><span class="sxs-lookup"><span data-stu-id="26716-151">NOTES</span></span>

## <span data-ttu-id="26716-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="26716-152">RELATED LINKS</span></span>

[<span data-ttu-id="26716-153">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26716-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="26716-154">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="26716-154">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="26716-155">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26716-155">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="26716-156">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26716-156">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="26716-157">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26716-157">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="26716-158">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26716-158">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


