---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0c619b306d6dece23006d351f666637afe9f852a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446738"
---
# <span data-ttu-id="8db5e-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8db5e-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8db5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8db5e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db5e-103">句法</span><span class="sxs-lookup"><span data-stu-id="8db5e-103">SYNTAX</span></span>

### <span data-ttu-id="8db5e-104">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8db5e-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db5e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8db5e-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db5e-106">說明</span><span class="sxs-lookup"><span data-stu-id="8db5e-106">DESCRIPTION</span></span>

## <span data-ttu-id="8db5e-107">示例</span><span class="sxs-lookup"><span data-stu-id="8db5e-107">EXAMPLES</span></span>

### <span data-ttu-id="8db5e-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="8db5e-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="8db5e-109">參數</span><span class="sxs-lookup"><span data-stu-id="8db5e-109">PARAMETERS</span></span>

### <span data-ttu-id="8db5e-110">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8db5e-110">-AuthorizationKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-111">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="8db5e-111">-ConnectionType</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-112">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="8db5e-112">-EnableBgp</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8db5e-113">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-114">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="8db5e-114">-IpsecPolicies</span></span>
<span data-ttu-id="8db5e-115">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="8db5e-115">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-116">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="8db5e-116">-LocalNetworkGateway2</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-117">-位置</span><span class="sxs-lookup"><span data-stu-id="8db5e-117">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8db5e-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-119">對等</span><span class="sxs-lookup"><span data-stu-id="8db5e-119">-Peer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-120">-PeerId</span><span class="sxs-lookup"><span data-stu-id="8db5e-120">-PeerId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db5e-121">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-122">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8db5e-122">-RoutingWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-123">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8db5e-123">-SharedKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="8db5e-124">-Tag</span></span>
<span data-ttu-id="8db5e-125">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8db5e-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8db5e-126">例如：</span><span class="sxs-lookup"><span data-stu-id="8db5e-126">For example:</span></span>

<span data-ttu-id="8db5e-127">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8db5e-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-128">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="8db5e-128">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="8db5e-129">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="8db5e-129">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-130">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="8db5e-130">-VirtualNetworkGateway1</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-131">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="8db5e-131">-VirtualNetworkGateway2</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="8db5e-132">-Confirm</span></span>
<span data-ttu-id="8db5e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8db5e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db5e-134">-WhatIf</span></span>
<span data-ttu-id="8db5e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8db5e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8db5e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8db5e-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db5e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db5e-137">-DefaultProfile</span></span>
<span data-ttu-id="8db5e-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8db5e-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db5e-139">CommonParameters</span></span>
<span data-ttu-id="8db5e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8db5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db5e-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8db5e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db5e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8db5e-142">INPUTS</span></span>

## <span data-ttu-id="8db5e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8db5e-143">OUTPUTS</span></span>

### <span data-ttu-id="8db5e-144">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8db5e-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8db5e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8db5e-145">NOTES</span></span>

## <span data-ttu-id="8db5e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8db5e-146">RELATED LINKS</span></span>

[<span data-ttu-id="8db5e-147">AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8db5e-147">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8db5e-148">移除-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8db5e-148">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8db5e-149">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8db5e-149">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
