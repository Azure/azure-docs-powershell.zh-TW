---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0299494ca775df60c94151f36efe554d0b876d22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621769"
---
# <span data-ttu-id="aa5cb-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa5cb-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="aa5cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5cb-103">建立負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="aa5cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa5cb-104">SYNTAX</span></span>

### <span data-ttu-id="aa5cb-105">SetByResourceSubnet (預設) </span><span class="sxs-lookup"><span data-stu-id="aa5cb-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5cb-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="aa5cb-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5cb-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa5cb-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5cb-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa5cb-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa5cb-109">說明</span><span class="sxs-lookup"><span data-stu-id="aa5cb-109">DESCRIPTION</span></span>
<span data-ttu-id="aa5cb-110">**新的-AzLoadBalancerFrontendIpConfig** Cmdlet 會為 Azure 負載平衡器建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="aa5cb-111">示例</span><span class="sxs-lookup"><span data-stu-id="aa5cb-111">EXAMPLES</span></span>

### <span data-ttu-id="aa5cb-112">範例1：建立負載平衡器的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="aa5cb-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="aa5cb-113">第一個命令會在名為 [MyResourceGroup] 的資源群組中建立名為 MyPublicIP 的動態公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="aa5cb-114">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="aa5cb-115">參數</span><span class="sxs-lookup"><span data-stu-id="aa5cb-115">PARAMETERS</span></span>

### <span data-ttu-id="aa5cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5cb-116">-DefaultProfile</span></span>
<span data-ttu-id="aa5cb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa5cb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa5cb-118">-Name</span></span>
<span data-ttu-id="aa5cb-119">指定此 Cmdlet 所建立的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aa5cb-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa5cb-120">-PrivateIpAddress</span></span>
<span data-ttu-id="aa5cb-121">指定負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="aa5cb-122">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="aa5cb-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa5cb-123">-PublicIpAddress</span></span>
<span data-ttu-id="aa5cb-124">指定要與前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="aa5cb-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="aa5cb-125">-PublicIpAddressId</span></span>
<span data-ttu-id="aa5cb-126">指定要與前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="aa5cb-127">-子網</span><span class="sxs-lookup"><span data-stu-id="aa5cb-127">-Subnet</span></span>
<span data-ttu-id="aa5cb-128">指定要建立前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="aa5cb-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="aa5cb-129">-SubnetId</span></span>
<span data-ttu-id="aa5cb-130">指定要在其中建立前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="aa5cb-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="aa5cb-131">-Zone</span></span>
<span data-ttu-id="aa5cb-132">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="aa5cb-133">-確認</span><span class="sxs-lookup"><span data-stu-id="aa5cb-133">-Confirm</span></span>
<span data-ttu-id="aa5cb-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa5cb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5cb-135">-WhatIf</span></span>
<span data-ttu-id="aa5cb-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa5cb-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa5cb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5cb-138">CommonParameters</span></span>
<span data-ttu-id="aa5cb-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5cb-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa5cb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5cb-141">輸入</span><span class="sxs-lookup"><span data-stu-id="aa5cb-141">INPUTS</span></span>

### <span data-ttu-id="aa5cb-142">System.object</span><span class="sxs-lookup"><span data-stu-id="aa5cb-142">System.String</span></span>

### <span data-ttu-id="aa5cb-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="aa5cb-143">System.String[]</span></span>

### <span data-ttu-id="aa5cb-144">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa5cb-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="aa5cb-145">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa5cb-145">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="aa5cb-146">輸出</span><span class="sxs-lookup"><span data-stu-id="aa5cb-146">OUTPUTS</span></span>

### <span data-ttu-id="aa5cb-147">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aa5cb-147">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="aa5cb-148">筆記</span><span class="sxs-lookup"><span data-stu-id="aa5cb-148">NOTES</span></span>

## <span data-ttu-id="aa5cb-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa5cb-149">RELATED LINKS</span></span>

[<span data-ttu-id="aa5cb-150">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa5cb-150">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aa5cb-151">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa5cb-151">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aa5cb-152">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa5cb-152">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="aa5cb-153">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa5cb-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="aa5cb-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa5cb-154">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


