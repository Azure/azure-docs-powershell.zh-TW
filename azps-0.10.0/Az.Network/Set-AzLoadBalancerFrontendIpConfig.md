---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795422"
---
# <span data-ttu-id="f254e-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f254e-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f254e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f254e-102">SYNOPSIS</span></span>
<span data-ttu-id="f254e-103">在負載平衡器中設定前端 IP 配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f254e-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="f254e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f254e-104">SYNTAX</span></span>

### <span data-ttu-id="f254e-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="f254e-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f254e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f254e-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f254e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f254e-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f254e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f254e-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f254e-109">說明</span><span class="sxs-lookup"><span data-stu-id="f254e-109">DESCRIPTION</span></span>
<span data-ttu-id="f254e-110">**AzLoadBalancerFrontendIpConfig** Cmdlet 會針對 Azure 負載平衡器中的前端 IP 配置設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f254e-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="f254e-111">示例</span><span class="sxs-lookup"><span data-stu-id="f254e-111">EXAMPLES</span></span>

### <span data-ttu-id="f254e-112">範例1：修改負載平衡器的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="f254e-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="f254e-113">第一個命令會取得名為 Subnet 的虛擬子網，然後將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="f254e-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="f254e-114">第二個命令會取得名為 MyLoadBalancer 的關聯負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="f254e-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="f254e-115">第三個命令使用管線運算子，將負載平衡器傳送 $slb 至 AzLoadBalancerFrontendIpConfig，這會建立名為 NewFrontend $slb 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="f254e-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="f254e-116">第四個命令會將負載平衡器 $slb **設定為 AzLoadBalancerFrontendIpConfig** ，這會儲存並更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="f254e-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="f254e-117">參數</span><span class="sxs-lookup"><span data-stu-id="f254e-117">PARAMETERS</span></span>

### <span data-ttu-id="f254e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f254e-118">-DefaultProfile</span></span>
<span data-ttu-id="f254e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f254e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f254e-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f254e-120">-LoadBalancer</span></span>
<span data-ttu-id="f254e-121">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="f254e-121">Specifies a load balancer.</span></span>
<span data-ttu-id="f254e-122">這個 Cmdlet 會針對此參數指定的負載平衡器，設定前端配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f254e-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f254e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f254e-123">-Name</span></span>
<span data-ttu-id="f254e-124">指定要設定的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="f254e-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f254e-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f254e-125">-PrivateIpAddress</span></span>
<span data-ttu-id="f254e-126">指定與要設定的前端 IP 設定相關聯之負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f254e-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="f254e-127">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f254e-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="f254e-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f254e-128">-PublicIpAddress</span></span>
<span data-ttu-id="f254e-129">指定與要設定的前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="f254e-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f254e-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f254e-130">-PublicIpAddressId</span></span>
<span data-ttu-id="f254e-131">指定與這個 Cmdlet 所設定之前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f254e-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f254e-132">-子網</span><span class="sxs-lookup"><span data-stu-id="f254e-132">-Subnet</span></span>
<span data-ttu-id="f254e-133">指定包含此 Cmdlet 所設定之前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="f254e-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f254e-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f254e-134">-SubnetId</span></span>
<span data-ttu-id="f254e-135">指定包含此 Cmdlet 所設定之前端 IP 配置的子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f254e-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f254e-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="f254e-136">-Zone</span></span>
<span data-ttu-id="f254e-137">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="f254e-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f254e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f254e-138">CommonParameters</span></span>
<span data-ttu-id="f254e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f254e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f254e-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f254e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f254e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f254e-141">INPUTS</span></span>

### <span data-ttu-id="f254e-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f254e-142">PSLoadBalancer</span></span>
<span data-ttu-id="f254e-143">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f254e-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f254e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f254e-144">OUTPUTS</span></span>

### <span data-ttu-id="f254e-145">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f254e-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f254e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f254e-146">NOTES</span></span>

## <span data-ttu-id="f254e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f254e-147">RELATED LINKS</span></span>

[<span data-ttu-id="f254e-148">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f254e-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f254e-149">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f254e-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f254e-150">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f254e-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f254e-151">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f254e-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f254e-152">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f254e-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f254e-153">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f254e-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


