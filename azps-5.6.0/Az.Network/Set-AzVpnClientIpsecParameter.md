---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 55a4f3c143355bf40672a1c3151d509b69062490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901925"
---
# <span data-ttu-id="13670-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="13670-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="13670-102">簡介</span><span class="sxs-lookup"><span data-stu-id="13670-102">SYNOPSIS</span></span>
<span data-ttu-id="13670-103">設定現有虛擬網路閘道的 vpn ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="13670-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="13670-104">語法</span><span class="sxs-lookup"><span data-stu-id="13670-104">SYNTAX</span></span>

### <span data-ttu-id="13670-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="13670-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13670-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13670-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13670-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13670-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13670-108">描述</span><span class="sxs-lookup"><span data-stu-id="13670-108">DESCRIPTION</span></span>
<span data-ttu-id="13670-109">**Set-Az VpnClientIpsecParameter** Cmdlet 會設定現有虛擬網路閘道的 vpn ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="13670-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="13670-110">建立虛擬網路閘道時，它會在閘道上設定一組預設的 vpn ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="13670-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="13670-111">萬一指向網站使用者想要使用特定自訂 ipsec 策略來連接到 VPN 閘道，使用者必須先在 VPN 閘道上設定該 ipsec 策略。</span><span class="sxs-lookup"><span data-stu-id="13670-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="13670-112">**Set-Az VpnClientIpsecParameter** 提供一種執行方式。</span><span class="sxs-lookup"><span data-stu-id="13670-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="13670-113">例子</span><span class="sxs-lookup"><span data-stu-id="13670-113">EXAMPLES</span></span>

### <span data-ttu-id="13670-114">範例 1：將自訂 vpn ipsec 策略設定為現有的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="13670-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="13670-115">此範例將自訂 vpn ipsec 策略設定為來自資源群組，名為 ContosoResourceGroup 的現有虛擬網路閘道 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="13670-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="13670-116">New-AzVpnClientIpsecParameter Cmdlet 用來建立 vpn ipsec 參數物件，使用使用者可針對 ResourceGroup 中任何現有虛擬網路閘道所設定之傳遞的一或所有參數值。</span><span class="sxs-lookup"><span data-stu-id="13670-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="13670-117">此建立 VpnClientIPsecParameters 物件會傳遞至 Set-AzVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂策略，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="13670-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="13670-118">此命令會返回 VpnClientIPsecParameters 的物件，該物件會顯示 set 參數。</span><span class="sxs-lookup"><span data-stu-id="13670-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="13670-119">參數</span><span class="sxs-lookup"><span data-stu-id="13670-119">PARAMETERS</span></span>

### <span data-ttu-id="13670-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13670-120">-DefaultProfile</span></span>
<span data-ttu-id="13670-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="13670-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13670-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13670-122">-InputObject</span></span>
<span data-ttu-id="13670-123">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="13670-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13670-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13670-124">-ResourceGroupName</span></span>
<span data-ttu-id="13670-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="13670-125">The resource group name.</span></span>

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

### <span data-ttu-id="13670-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13670-126">-ResourceId</span></span>
<span data-ttu-id="13670-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="13670-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13670-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="13670-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="13670-129">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="13670-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="13670-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="13670-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="13670-131">Vpn 用戶端 ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="13670-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="13670-132">此參數值可以使用 PS 命令 let：New-Az VpnClientIpsecParameter 建構</span><span class="sxs-lookup"><span data-stu-id="13670-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13670-133">-確認</span><span class="sxs-lookup"><span data-stu-id="13670-133">-Confirm</span></span>
<span data-ttu-id="13670-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="13670-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13670-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13670-135">-WhatIf</span></span>
<span data-ttu-id="13670-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13670-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13670-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13670-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13670-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13670-138">CommonParameters</span></span>
<span data-ttu-id="13670-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="13670-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13670-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="13670-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13670-141">輸入</span><span class="sxs-lookup"><span data-stu-id="13670-141">INPUTS</span></span>

### <span data-ttu-id="13670-142">Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="13670-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="13670-143">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13670-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="13670-144">System.String</span><span class="sxs-lookup"><span data-stu-id="13670-144">System.String</span></span>

## <span data-ttu-id="13670-145">輸出</span><span class="sxs-lookup"><span data-stu-id="13670-145">OUTPUTS</span></span>

### <span data-ttu-id="13670-146">Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="13670-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="13670-147">筆記</span><span class="sxs-lookup"><span data-stu-id="13670-147">NOTES</span></span>

## <span data-ttu-id="13670-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="13670-148">RELATED LINKS</span></span>

[<span data-ttu-id="13670-149">Get-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="13670-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="13670-150">New-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="13670-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="13670-151">Remove-Az VpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="13670-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
