---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438736"
---
# <span data-ttu-id="279e0-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="279e0-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="279e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="279e0-102">SYNOPSIS</span></span>
<span data-ttu-id="279e0-103">為現有的虛擬網路閘道設定 vpn ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="279e0-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="279e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="279e0-104">SYNTAX</span></span>

### <span data-ttu-id="279e0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="279e0-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279e0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="279e0-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279e0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="279e0-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="279e0-108">DESCRIPTION</span></span>
<span data-ttu-id="279e0-109">**AzVpnClientIpsecParameter** Cmdlet 會為現有的虛擬網路閘道設定 vpn ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="279e0-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="279e0-110">建立虛擬網路閘道之後，它會在閘道上設定預設的 vpn ipsec 原則組。</span><span class="sxs-lookup"><span data-stu-id="279e0-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="279e0-111">在此情況下，指向 [網站使用者] 想要使用特定的自訂 ipsec 原則連線至 VPN 閘道，使用者必須先在 VPN 閘道設定該 ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="279e0-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="279e0-112">**AzVpnClientIpsecParameter** 提供一種方式來執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="279e0-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="279e0-113">示例</span><span class="sxs-lookup"><span data-stu-id="279e0-113">EXAMPLES</span></span>

### <span data-ttu-id="279e0-114">範例1：將自訂 vpn ipsec 原則設定成現有的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="279e0-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="279e0-115">這個範例會將自訂的 vpn ipsec 原則設定為從名為 ContosoResourceGroup 的資源群組 ContosoVirtualGateway 的現有虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="279e0-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="279e0-116">New-AzVpnClientIpsecParameter Cmdlet 是用來建立 vpn ipsec 參數物件，其中使用的是使用者可針對 ResourceGroup 中任何現有虛擬網路閘道設定的一個或所有參數值。</span><span class="sxs-lookup"><span data-stu-id="279e0-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="279e0-117">這個建立的 VpnClientIPsecParameters 物件會傳遞給 Set-AzVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂原則，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="279e0-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="279e0-118">這個命令會傳回 VpnClientIPsecParameters 的物件，其中會顯示設定的參數。</span><span class="sxs-lookup"><span data-stu-id="279e0-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="279e0-119">參數</span><span class="sxs-lookup"><span data-stu-id="279e0-119">PARAMETERS</span></span>

### <span data-ttu-id="279e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279e0-120">-DefaultProfile</span></span>
<span data-ttu-id="279e0-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="279e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279e0-122">-InputObject</span></span>
<span data-ttu-id="279e0-123">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="279e0-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="279e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="279e0-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="279e0-125">The resource group name.</span></span>

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

### <span data-ttu-id="279e0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279e0-126">-ResourceId</span></span>
<span data-ttu-id="279e0-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="279e0-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="279e0-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="279e0-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="279e0-129">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="279e0-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="279e0-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="279e0-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="279e0-131">Vpn 用戶端 ipsec 參數。</span><span class="sxs-lookup"><span data-stu-id="279e0-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="279e0-132">這個參數值可以使用 PS 命令來構造： [新-AzVpnClientIpsecParameter]</span><span class="sxs-lookup"><span data-stu-id="279e0-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="279e0-133">-確認</span><span class="sxs-lookup"><span data-stu-id="279e0-133">-Confirm</span></span>
<span data-ttu-id="279e0-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="279e0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279e0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279e0-135">-WhatIf</span></span>
<span data-ttu-id="279e0-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="279e0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279e0-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="279e0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279e0-138">CommonParameters</span></span>
<span data-ttu-id="279e0-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="279e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279e0-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="279e0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279e0-141">輸入</span><span class="sxs-lookup"><span data-stu-id="279e0-141">INPUTS</span></span>

### <span data-ttu-id="279e0-142">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="279e0-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="279e0-143">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="279e0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="279e0-144">System.object</span><span class="sxs-lookup"><span data-stu-id="279e0-144">System.String</span></span>

## <span data-ttu-id="279e0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="279e0-145">OUTPUTS</span></span>

### <span data-ttu-id="279e0-146">PSVpnClientIPsecParameters 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="279e0-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="279e0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="279e0-147">NOTES</span></span>

## <span data-ttu-id="279e0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="279e0-148">RELATED LINKS</span></span>

[<span data-ttu-id="279e0-149">AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="279e0-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="279e0-150">新-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="279e0-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="279e0-151">移除-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="279e0-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
