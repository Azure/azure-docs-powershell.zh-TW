---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b64e24bb816ce7d01b99c0dbaa808ecdac99a082
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451467"
---
# <span data-ttu-id="b3a61-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b3a61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3a61-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a61-103">在負載平衡器中新增前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="b3a61-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a61-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3a61-104">SYNTAX</span></span>

### <span data-ttu-id="b3a61-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="b3a61-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a61-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="b3a61-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a61-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b3a61-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a61-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b3a61-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a61-109">說明</span><span class="sxs-lookup"><span data-stu-id="b3a61-109">DESCRIPTION</span></span>
<span data-ttu-id="b3a61-110">**AzureRmLoadBalancerFrontendIpConifg** Cmdlet 會將前端 IP 配置新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b3a61-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b3a61-111">示例</span><span class="sxs-lookup"><span data-stu-id="b3a61-111">EXAMPLES</span></span>

### <span data-ttu-id="b3a61-112">範例1使用動態 IP 位址新增前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="b3a61-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b3a61-113">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzureRmVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="b3a61-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b3a61-114">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b3a61-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b3a61-115">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $MySubnet 的變數中所儲存之子網上的動態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3a61-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="b3a61-116">範例2使用靜態 IP 位址新增前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="b3a61-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b3a61-117">第一個命令會取得名為 MyVnet 的 Azure 虛擬網路，並使用管線將結果傳遞到 **AzureRmVirtualNetworkSubnetConfig** Cmdlet，以取得名為 MySubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="b3a61-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b3a61-118">然後，該命令會將結果儲存在名為 $Subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b3a61-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b3a61-119">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $Subnet 的變數中所儲存之子網上的靜態私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3a61-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="b3a61-120">範例3新增含公用 IP 位址的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="b3a61-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b3a61-121">第一個命令會取得名為 MyPub 的 Azure 公用 IP 位址，並將結果儲存在名為 $PublicIp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b3a61-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="b3a61-122">第二個命令會取得名為 MyLB 的負載平衡器，並將結果傳遞給載入 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet，該 Cmdlet 會將前端 ip 配置加上名為 $PublicIp 變數中的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3a61-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="b3a61-123">參數</span><span class="sxs-lookup"><span data-stu-id="b3a61-123">PARAMETERS</span></span>

### <span data-ttu-id="b3a61-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a61-124">-DefaultProfile</span></span>
<span data-ttu-id="b3a61-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3a61-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3a61-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3a61-126">-LoadBalancer</span></span>
<span data-ttu-id="b3a61-127">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3a61-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b3a61-128">這個 Cmdlet 會將前端 IP 設定新增至此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b3a61-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3a61-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3a61-129">-Name</span></span>
<span data-ttu-id="b3a61-130">指定要新增的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b3a61-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="b3a61-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b3a61-131">-PrivateIpAddress</span></span>
<span data-ttu-id="b3a61-132">指定要與前端 IP 配置相關聯的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3a61-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b3a61-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b3a61-133">-PublicIpAddress</span></span>
<span data-ttu-id="b3a61-134">指定要與前端 IP 設定關聯的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3a61-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b3a61-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b3a61-135">-PublicIpAddressId</span></span>
<span data-ttu-id="b3a61-136">Specifes 要新增前端 IP 配置的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3a61-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b3a61-137">-子網</span><span class="sxs-lookup"><span data-stu-id="b3a61-137">-Subnet</span></span>
<span data-ttu-id="b3a61-138">指定要新增前端 IP 配置的子網物件。</span><span class="sxs-lookup"><span data-stu-id="b3a61-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b3a61-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b3a61-139">-SubnetId</span></span>
<span data-ttu-id="b3a61-140">指定要在其中新增前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3a61-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b3a61-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="b3a61-141">-Zone</span></span>
<span data-ttu-id="b3a61-142">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="b3a61-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b3a61-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a61-143">CommonParameters</span></span>
<span data-ttu-id="b3a61-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3a61-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a61-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3a61-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a61-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b3a61-146">INPUTS</span></span>

### <span data-ttu-id="b3a61-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3a61-147">PSLoadBalancer</span></span>
<span data-ttu-id="b3a61-148">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b3a61-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b3a61-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b3a61-149">OUTPUTS</span></span>

### <span data-ttu-id="b3a61-150">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3a61-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b3a61-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b3a61-151">NOTES</span></span>

## <span data-ttu-id="b3a61-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3a61-152">RELATED LINKS</span></span>

[<span data-ttu-id="b3a61-153">AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b3a61-154">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3a61-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b3a61-155">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b3a61-156">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b3a61-157">移除-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b3a61-158">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3a61-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


