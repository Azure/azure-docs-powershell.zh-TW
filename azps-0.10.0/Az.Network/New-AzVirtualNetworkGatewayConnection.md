---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 7aede18c438faca196d696a69e7f7651edac132e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794230"
---
# <span data-ttu-id="b597a-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b597a-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b597a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b597a-102">SYNOPSIS</span></span>

## <span data-ttu-id="b597a-103">句法</span><span class="sxs-lookup"><span data-stu-id="b597a-103">SYNTAX</span></span>

### <span data-ttu-id="b597a-104">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b597a-104">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b597a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b597a-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b597a-106">說明</span><span class="sxs-lookup"><span data-stu-id="b597a-106">DESCRIPTION</span></span>

## <span data-ttu-id="b597a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b597a-107">EXAMPLES</span></span>

### <span data-ttu-id="b597a-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="b597a-108">1:</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="b597a-109">參數</span><span class="sxs-lookup"><span data-stu-id="b597a-109">PARAMETERS</span></span>

### <span data-ttu-id="b597a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b597a-110">-AsJob</span></span>
<span data-ttu-id="b597a-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b597a-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="b597a-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="b597a-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b597a-114">-DefaultProfile</span></span>
<span data-ttu-id="b597a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b597a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b597a-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b597a-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b597a-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="b597a-118">-IpsecPolicies</span></span>
<span data-ttu-id="b597a-119">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="b597a-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="b597a-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="b597a-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b597a-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b597a-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-123">對等</span><span class="sxs-lookup"><span data-stu-id="b597a-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="b597a-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b597a-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="b597a-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b597a-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b597a-128">-Tag</span></span>
<span data-ttu-id="b597a-129">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b597a-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b597a-130">例如：</span><span class="sxs-lookup"><span data-stu-id="b597a-130">For example:</span></span>

<span data-ttu-id="b597a-131">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b597a-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b597a-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b597a-133">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="b597a-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="b597a-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="b597a-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="b597a-136">-Confirm</span></span>
<span data-ttu-id="b597a-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b597a-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b597a-138">-WhatIf</span></span>
<span data-ttu-id="b597a-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b597a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b597a-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b597a-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b597a-141">CommonParameters</span></span>
<span data-ttu-id="b597a-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b597a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b597a-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b597a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b597a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b597a-144">INPUTS</span></span>

## <span data-ttu-id="b597a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b597a-145">OUTPUTS</span></span>

### <span data-ttu-id="b597a-146">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b597a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b597a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b597a-147">NOTES</span></span>

## <span data-ttu-id="b597a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b597a-148">RELATED LINKS</span></span>

[<span data-ttu-id="b597a-149">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b597a-149">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b597a-150">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b597a-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b597a-151">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b597a-151">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
