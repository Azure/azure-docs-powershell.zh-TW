---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f1c6790ba733004a565087b261e0ca9b42f9688b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621455"
---
# <span data-ttu-id="27a15-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27a15-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="27a15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27a15-102">SYNOPSIS</span></span>
<span data-ttu-id="27a15-103">更新負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="27a15-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="27a15-104">句法</span><span class="sxs-lookup"><span data-stu-id="27a15-104">SYNTAX</span></span>

### <span data-ttu-id="27a15-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="27a15-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27a15-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="27a15-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27a15-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27a15-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27a15-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27a15-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27a15-109">說明</span><span class="sxs-lookup"><span data-stu-id="27a15-109">DESCRIPTION</span></span>
<span data-ttu-id="27a15-110">**AzLoadBalancerFrontendIpConfig** Cmdlet 會更新負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="27a15-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="27a15-111">示例</span><span class="sxs-lookup"><span data-stu-id="27a15-111">EXAMPLES</span></span>

### <span data-ttu-id="27a15-112">範例1：修改負載平衡器的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="27a15-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="27a15-113">第一個命令會取得名為 Subnet 的虛擬子網，然後將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="27a15-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="27a15-114">第二個命令會取得名為 MyLoadBalancer 的關聯負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="27a15-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="27a15-115">第三個命令使用管線運算子，將負載平衡器傳送 $slb 至 AzLoadBalancerFrontendIpConfig，這會建立名為 NewFrontend $slb 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="27a15-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="27a15-116">第四個命令會將負載平衡器 $slb **設定為 AzLoadBalancerFrontendIpConfig** ，這會儲存並更新前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="27a15-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="27a15-117">參數</span><span class="sxs-lookup"><span data-stu-id="27a15-117">PARAMETERS</span></span>

### <span data-ttu-id="27a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a15-118">-DefaultProfile</span></span>
<span data-ttu-id="27a15-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27a15-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a15-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27a15-120">-LoadBalancer</span></span>
<span data-ttu-id="27a15-121">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="27a15-121">Specifies a load balancer.</span></span>
<span data-ttu-id="27a15-122">這個 Cmdlet 會針對此參數指定的負載平衡器更新前端設定。</span><span class="sxs-lookup"><span data-stu-id="27a15-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="27a15-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="27a15-123">-Name</span></span>
<span data-ttu-id="27a15-124">指定要設定的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="27a15-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="27a15-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="27a15-125">-PrivateIpAddress</span></span>
<span data-ttu-id="27a15-126">指定與要設定的前端 IP 設定相關聯之負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="27a15-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="27a15-127">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="27a15-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="27a15-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27a15-128">-PublicIpAddress</span></span>
<span data-ttu-id="27a15-129">指定與要設定的前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="27a15-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="27a15-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="27a15-130">-PublicIpAddressId</span></span>
<span data-ttu-id="27a15-131">指定與這個 Cmdlet 所設定之前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27a15-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="27a15-132">-子網</span><span class="sxs-lookup"><span data-stu-id="27a15-132">-Subnet</span></span>
<span data-ttu-id="27a15-133">指定包含此 Cmdlet 所設定之前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="27a15-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="27a15-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="27a15-134">-SubnetId</span></span>
<span data-ttu-id="27a15-135">指定包含此 Cmdlet 所設定之前端 IP 配置的子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27a15-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="27a15-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="27a15-136">-Zone</span></span>
<span data-ttu-id="27a15-137">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="27a15-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="27a15-138">-確認</span><span class="sxs-lookup"><span data-stu-id="27a15-138">-Confirm</span></span>
<span data-ttu-id="27a15-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27a15-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a15-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a15-140">-WhatIf</span></span>
<span data-ttu-id="27a15-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27a15-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27a15-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27a15-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a15-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a15-143">CommonParameters</span></span>
<span data-ttu-id="27a15-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27a15-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a15-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27a15-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a15-146">輸入</span><span class="sxs-lookup"><span data-stu-id="27a15-146">INPUTS</span></span>

### <span data-ttu-id="27a15-147">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27a15-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="27a15-148">System.object</span><span class="sxs-lookup"><span data-stu-id="27a15-148">System.String</span></span>

### <span data-ttu-id="27a15-149">System.object []</span><span class="sxs-lookup"><span data-stu-id="27a15-149">System.String[]</span></span>

### <span data-ttu-id="27a15-150">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27a15-150">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="27a15-151">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27a15-151">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="27a15-152">輸出</span><span class="sxs-lookup"><span data-stu-id="27a15-152">OUTPUTS</span></span>

### <span data-ttu-id="27a15-153">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27a15-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27a15-154">筆記</span><span class="sxs-lookup"><span data-stu-id="27a15-154">NOTES</span></span>

## <span data-ttu-id="27a15-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="27a15-155">RELATED LINKS</span></span>

[<span data-ttu-id="27a15-156">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27a15-156">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27a15-157">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27a15-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27a15-158">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27a15-158">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27a15-159">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27a15-159">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="27a15-160">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27a15-160">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27a15-161">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27a15-161">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


