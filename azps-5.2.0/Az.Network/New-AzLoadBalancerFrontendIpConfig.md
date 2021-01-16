---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275936"
---
# <span data-ttu-id="7903c-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7903c-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7903c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7903c-102">SYNOPSIS</span></span>
<span data-ttu-id="7903c-103">建立負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7903c-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7903c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7903c-104">SYNTAX</span></span>

### <span data-ttu-id="7903c-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="7903c-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7903c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7903c-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7903c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7903c-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7903c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7903c-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7903c-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7903c-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7903c-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7903c-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7903c-111">說明</span><span class="sxs-lookup"><span data-stu-id="7903c-111">DESCRIPTION</span></span>
<span data-ttu-id="7903c-112">**新的-AzLoadBalancerFrontendIpConfig** Cmdlet 會為 Azure 負載平衡器建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7903c-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7903c-113">示例</span><span class="sxs-lookup"><span data-stu-id="7903c-113">EXAMPLES</span></span>

### <span data-ttu-id="7903c-114">範例1：建立負載平衡器的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="7903c-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="7903c-115">第一個命令會在名為 [MyResourceGroup] 的資源群組中建立名為 MyPublicIP 的動態公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="7903c-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="7903c-116">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="7903c-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="7903c-117">範例2：使用 IP 首碼為負載平衡器建立前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="7903c-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="7903c-118">第一個命令會在名為 MyResourceGroup 的資源群組中，建立名為 MyPublicIP 長度為28的公用 ip 首碼，然後將其儲存在 $publicipprefix 變數中。</span><span class="sxs-lookup"><span data-stu-id="7903c-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="7903c-119">第二個命令會使用 $publicipprefix 中的公用 IP 首碼，建立名為 FrontendIpConfig01 的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7903c-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="7903c-120">參數</span><span class="sxs-lookup"><span data-stu-id="7903c-120">PARAMETERS</span></span>

### <span data-ttu-id="7903c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7903c-121">-DefaultProfile</span></span>
<span data-ttu-id="7903c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7903c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7903c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7903c-123">-Name</span></span>
<span data-ttu-id="7903c-124">指定此 Cmdlet 所建立的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="7903c-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7903c-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7903c-125">-PrivateIpAddress</span></span>
<span data-ttu-id="7903c-126">指定負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7903c-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="7903c-127">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="7903c-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="7903c-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7903c-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7903c-129">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="7903c-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="7903c-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7903c-130">-PublicIpAddress</span></span>
<span data-ttu-id="7903c-131">指定要與前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="7903c-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7903c-132">-PublicIpAddressId</span></span>
<span data-ttu-id="7903c-133">指定要與前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7903c-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7903c-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="7903c-135">指定要與前端 IP 配置相關聯的 **PublicIpAddressPrefix** 物件。</span><span class="sxs-lookup"><span data-stu-id="7903c-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="7903c-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="7903c-137">指定要與前端 IP 設定相關聯之 **PublicIpAddressPrefix** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7903c-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-138">-子網</span><span class="sxs-lookup"><span data-stu-id="7903c-138">-Subnet</span></span>
<span data-ttu-id="7903c-139">指定要建立前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="7903c-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7903c-140">-SubnetId</span></span>
<span data-ttu-id="7903c-141">指定要在其中建立前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="7903c-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7903c-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="7903c-142">-Zone</span></span>
<span data-ttu-id="7903c-143">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="7903c-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7903c-144">-確認</span><span class="sxs-lookup"><span data-stu-id="7903c-144">-Confirm</span></span>
<span data-ttu-id="7903c-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7903c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7903c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7903c-146">-WhatIf</span></span>
<span data-ttu-id="7903c-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7903c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7903c-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7903c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7903c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7903c-149">CommonParameters</span></span>
<span data-ttu-id="7903c-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7903c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7903c-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7903c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7903c-152">輸入</span><span class="sxs-lookup"><span data-stu-id="7903c-152">INPUTS</span></span>

### <span data-ttu-id="7903c-153">System.object</span><span class="sxs-lookup"><span data-stu-id="7903c-153">System.String</span></span>

### <span data-ttu-id="7903c-154">System.object []</span><span class="sxs-lookup"><span data-stu-id="7903c-154">System.String[]</span></span>

### <span data-ttu-id="7903c-155">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7903c-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7903c-156">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7903c-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7903c-157">輸出</span><span class="sxs-lookup"><span data-stu-id="7903c-157">OUTPUTS</span></span>

### <span data-ttu-id="7903c-158">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7903c-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7903c-159">筆記</span><span class="sxs-lookup"><span data-stu-id="7903c-159">NOTES</span></span>

## <span data-ttu-id="7903c-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="7903c-160">RELATED LINKS</span></span>

[<span data-ttu-id="7903c-161">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7903c-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7903c-162">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7903c-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7903c-163">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7903c-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7903c-164">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7903c-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7903c-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7903c-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


