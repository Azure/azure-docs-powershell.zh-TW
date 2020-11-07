---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: fcf908f0c67a81ad9ff82eec3aad82f14ac6d1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789070"
---
# <span data-ttu-id="44daa-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="44daa-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="44daa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44daa-102">SYNOPSIS</span></span>
<span data-ttu-id="44daa-103">移除在虛擬網路閘道資源上設定的 Vpn 自訂 ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="44daa-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="44daa-104">句法</span><span class="sxs-lookup"><span data-stu-id="44daa-104">SYNTAX</span></span>

### <span data-ttu-id="44daa-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="44daa-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44daa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="44daa-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44daa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44daa-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44daa-108">說明</span><span class="sxs-lookup"><span data-stu-id="44daa-108">DESCRIPTION</span></span>
<span data-ttu-id="44daa-109">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="44daa-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="44daa-110">**AzVpnClientIpsecParameter** Cmdlet 會移除您在虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，然後根據傳遞的 VirtualNetworkGateway 名稱和資源組名稱，在 vpn 閘道上設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="44daa-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="44daa-111">示例</span><span class="sxs-lookup"><span data-stu-id="44daa-111">EXAMPLES</span></span>

### <span data-ttu-id="44daa-112">1：刪除虛擬網路閘道上設定的 vpn ipsec 參數</span><span class="sxs-lookup"><span data-stu-id="44daa-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="44daa-113">刪除在您的虛擬網路閘道上設定的 vpn 自訂 ipsec 參數，名稱為 "myRG" 中的 [myGateway "。</span><span class="sxs-lookup"><span data-stu-id="44daa-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="44daa-114">這個命令會傳回 bool 物件，顯示刪除成功或失敗的情況。</span><span class="sxs-lookup"><span data-stu-id="44daa-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="44daa-115">注意：這將會導致在您的虛擬網路閘道設定預設的 vpn ipsec 原則。</span><span class="sxs-lookup"><span data-stu-id="44daa-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="44daa-116">參數</span><span class="sxs-lookup"><span data-stu-id="44daa-116">PARAMETERS</span></span>

### <span data-ttu-id="44daa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44daa-117">-DefaultProfile</span></span>
<span data-ttu-id="44daa-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44daa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44daa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44daa-119">-InputObject</span></span>
<span data-ttu-id="44daa-120">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="44daa-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="44daa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44daa-121">-ResourceGroupName</span></span>
<span data-ttu-id="44daa-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="44daa-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44daa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44daa-123">-ResourceId</span></span>
<span data-ttu-id="44daa-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="44daa-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="44daa-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="44daa-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="44daa-126">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="44daa-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44daa-127">-確認</span><span class="sxs-lookup"><span data-stu-id="44daa-127">-Confirm</span></span>
<span data-ttu-id="44daa-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="44daa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44daa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44daa-129">-WhatIf</span></span>
<span data-ttu-id="44daa-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44daa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44daa-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44daa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44daa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44daa-132">CommonParameters</span></span>
<span data-ttu-id="44daa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44daa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44daa-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="44daa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44daa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="44daa-135">INPUTS</span></span>

### <span data-ttu-id="44daa-136">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="44daa-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="44daa-137">System.object</span><span class="sxs-lookup"><span data-stu-id="44daa-137">System.String</span></span>

## <span data-ttu-id="44daa-138">輸出</span><span class="sxs-lookup"><span data-stu-id="44daa-138">OUTPUTS</span></span>

### <span data-ttu-id="44daa-139">System.object</span><span class="sxs-lookup"><span data-stu-id="44daa-139">System.Boolean</span></span>

## <span data-ttu-id="44daa-140">筆記</span><span class="sxs-lookup"><span data-stu-id="44daa-140">NOTES</span></span>

## <span data-ttu-id="44daa-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="44daa-141">RELATED LINKS</span></span>

[<span data-ttu-id="44daa-142">AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="44daa-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="44daa-143">新-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="44daa-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="44daa-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="44daa-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
