---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: dc28df7630cbb2c9e239fe31f99ad3361e5c1f54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789334"
---
# <span data-ttu-id="09f4d-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09f4d-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="09f4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="09f4d-103">建立負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="09f4d-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="09f4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="09f4d-104">SYNTAX</span></span>

### <span data-ttu-id="09f4d-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="09f4d-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f4d-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="09f4d-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f4d-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09f4d-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f4d-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09f4d-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f4d-109">說明</span><span class="sxs-lookup"><span data-stu-id="09f4d-109">DESCRIPTION</span></span>
<span data-ttu-id="09f4d-110">**新的-AzLoadBalancerFrontendIpConfig** Cmdlet 會為 Azure 負載平衡器建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="09f4d-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="09f4d-111">示例</span><span class="sxs-lookup"><span data-stu-id="09f4d-111">EXAMPLES</span></span>

### <span data-ttu-id="09f4d-112">範例1：建立負載平衡器的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="09f4d-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="09f4d-113">第一個命令會在名為 [MyResourceGroup] 的資源群組中建立名為 MyPublicIP 的動態公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="09f4d-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="09f4d-114">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="09f4d-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="09f4d-115">參數</span><span class="sxs-lookup"><span data-stu-id="09f4d-115">PARAMETERS</span></span>

### <span data-ttu-id="09f4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f4d-116">-DefaultProfile</span></span>
<span data-ttu-id="09f4d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09f4d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f4d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="09f4d-118">-Name</span></span>
<span data-ttu-id="09f4d-119">指定此 Cmdlet 所建立的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="09f4d-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="09f4d-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="09f4d-120">-PrivateIpAddress</span></span>
<span data-ttu-id="09f4d-121">指定負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="09f4d-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="09f4d-122">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="09f4d-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="09f4d-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="09f4d-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="09f4d-124">IP 配置的私人 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="09f4d-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="09f4d-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09f4d-125">-PublicIpAddress</span></span>
<span data-ttu-id="09f4d-126">指定要與前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="09f4d-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="09f4d-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="09f4d-127">-PublicIpAddressId</span></span>
<span data-ttu-id="09f4d-128">指定要與前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="09f4d-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="09f4d-129">-子網</span><span class="sxs-lookup"><span data-stu-id="09f4d-129">-Subnet</span></span>
<span data-ttu-id="09f4d-130">指定要建立前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="09f4d-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="09f4d-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="09f4d-131">-SubnetId</span></span>
<span data-ttu-id="09f4d-132">指定要在其中建立前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="09f4d-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="09f4d-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="09f4d-133">-Zone</span></span>
<span data-ttu-id="09f4d-134">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="09f4d-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="09f4d-135">-確認</span><span class="sxs-lookup"><span data-stu-id="09f4d-135">-Confirm</span></span>
<span data-ttu-id="09f4d-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="09f4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f4d-137">-WhatIf</span></span>
<span data-ttu-id="09f4d-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09f4d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09f4d-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09f4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f4d-140">CommonParameters</span></span>
<span data-ttu-id="09f4d-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09f4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f4d-142">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09f4d-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f4d-143">輸入</span><span class="sxs-lookup"><span data-stu-id="09f4d-143">INPUTS</span></span>

### <span data-ttu-id="09f4d-144">System.object</span><span class="sxs-lookup"><span data-stu-id="09f4d-144">System.String</span></span>

### <span data-ttu-id="09f4d-145">System.object []</span><span class="sxs-lookup"><span data-stu-id="09f4d-145">System.String[]</span></span>

### <span data-ttu-id="09f4d-146">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09f4d-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="09f4d-147">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09f4d-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="09f4d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="09f4d-148">OUTPUTS</span></span>

### <span data-ttu-id="09f4d-149">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09f4d-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="09f4d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="09f4d-150">NOTES</span></span>

## <span data-ttu-id="09f4d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="09f4d-151">RELATED LINKS</span></span>

[<span data-ttu-id="09f4d-152">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09f4d-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="09f4d-153">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09f4d-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="09f4d-154">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09f4d-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="09f4d-155">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09f4d-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="09f4d-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09f4d-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


