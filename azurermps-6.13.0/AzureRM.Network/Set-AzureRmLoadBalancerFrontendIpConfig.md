---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624040"
---
# <span data-ttu-id="ffe89-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffe89-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ffe89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffe89-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe89-103">在負載平衡器中設定前端 IP 配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ffe89-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe89-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffe89-104">SYNTAX</span></span>

### <span data-ttu-id="ffe89-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="ffe89-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe89-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="ffe89-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe89-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffe89-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe89-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffe89-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffe89-109">說明</span><span class="sxs-lookup"><span data-stu-id="ffe89-109">DESCRIPTION</span></span>
<span data-ttu-id="ffe89-110">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet 會針對 Azure 負載平衡器中的前端 IP 配置設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ffe89-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="ffe89-111">示例</span><span class="sxs-lookup"><span data-stu-id="ffe89-111">EXAMPLES</span></span>

### <span data-ttu-id="ffe89-112">範例1：修改負載平衡器的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="ffe89-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="ffe89-113">第一個命令會取得名為 Subnet 的虛擬子網，然後將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="ffe89-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ffe89-114">第二個命令會取得名為 MyLoadBalancer 的關聯負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="ffe89-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ffe89-115">第三個命令使用管線運算子，將負載平衡器傳送 $slb 至 AzureRmLoadBalancerFrontendIpConfig，這會建立名為 NewFrontend $slb 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="ffe89-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="ffe89-116">第四個命令會將負載平衡器 $slb **設定為 AzureRmLoadBalancerFrontendIpConfig** ，這會儲存並更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="ffe89-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="ffe89-117">參數</span><span class="sxs-lookup"><span data-stu-id="ffe89-117">PARAMETERS</span></span>

### <span data-ttu-id="ffe89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe89-118">-DefaultProfile</span></span>
<span data-ttu-id="ffe89-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffe89-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffe89-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ffe89-120">-LoadBalancer</span></span>
<span data-ttu-id="ffe89-121">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ffe89-121">Specifies a load balancer.</span></span>
<span data-ttu-id="ffe89-122">這個 Cmdlet 會針對此參數指定的負載平衡器，設定前端配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ffe89-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffe89-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffe89-123">-Name</span></span>
<span data-ttu-id="ffe89-124">指定要設定的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe89-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="ffe89-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffe89-125">-PrivateIpAddress</span></span>
<span data-ttu-id="ffe89-126">指定與要設定的前端 IP 設定相關聯之負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ffe89-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="ffe89-127">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ffe89-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="ffe89-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffe89-128">-PublicIpAddress</span></span>
<span data-ttu-id="ffe89-129">指定與要設定的前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="ffe89-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="ffe89-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ffe89-130">-PublicIpAddressId</span></span>
<span data-ttu-id="ffe89-131">指定與這個 Cmdlet 所設定之前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffe89-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ffe89-132">-子網</span><span class="sxs-lookup"><span data-stu-id="ffe89-132">-Subnet</span></span>
<span data-ttu-id="ffe89-133">指定包含此 Cmdlet 所設定之前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="ffe89-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ffe89-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ffe89-134">-SubnetId</span></span>
<span data-ttu-id="ffe89-135">指定包含此 Cmdlet 所設定之前端 IP 配置的子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffe89-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ffe89-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="ffe89-136">-Zone</span></span>
<span data-ttu-id="ffe89-137">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="ffe89-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="ffe89-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ffe89-138">-Confirm</span></span>
<span data-ttu-id="ffe89-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffe89-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffe89-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffe89-140">-WhatIf</span></span>
<span data-ttu-id="ffe89-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffe89-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffe89-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffe89-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffe89-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe89-143">CommonParameters</span></span>
<span data-ttu-id="ffe89-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffe89-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe89-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffe89-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe89-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ffe89-146">INPUTS</span></span>

### <span data-ttu-id="ffe89-147">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffe89-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ffe89-148">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ffe89-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="ffe89-149">[System.object]。清單 \` 1 [[system.object，字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ffe89-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ffe89-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ffe89-150">OUTPUTS</span></span>

### <span data-ttu-id="ffe89-151">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffe89-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ffe89-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ffe89-152">NOTES</span></span>

## <span data-ttu-id="ffe89-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffe89-153">RELATED LINKS</span></span>

[<span data-ttu-id="ffe89-154">附加 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffe89-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ffe89-155">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ffe89-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ffe89-156">AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffe89-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ffe89-157">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ffe89-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ffe89-158">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffe89-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ffe89-159">移除-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffe89-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


