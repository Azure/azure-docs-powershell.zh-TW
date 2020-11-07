---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802314"
---
# <span data-ttu-id="0ce06-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce06-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ce06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ce06-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce06-103">句法</span><span class="sxs-lookup"><span data-stu-id="0ce06-103">SYNTAX</span></span>

### <span data-ttu-id="0ce06-104">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0ce06-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce06-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce06-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce06-106">說明</span><span class="sxs-lookup"><span data-stu-id="0ce06-106">DESCRIPTION</span></span>

## <span data-ttu-id="0ce06-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ce06-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce06-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="0ce06-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="0ce06-109">參數</span><span class="sxs-lookup"><span data-stu-id="0ce06-109">PARAMETERS</span></span>

### <span data-ttu-id="0ce06-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ce06-110">-AsJob</span></span>
<span data-ttu-id="0ce06-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0ce06-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ce06-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0ce06-112">-AuthorizationKey</span></span>
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

### <span data-ttu-id="0ce06-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="0ce06-113">-ConnectionType</span></span>
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

### <span data-ttu-id="0ce06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce06-114">-DefaultProfile</span></span>
<span data-ttu-id="0ce06-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ce06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce06-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0ce06-116">-EnableBgp</span></span>
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

### <span data-ttu-id="0ce06-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0ce06-117">-Force</span></span>
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

### <span data-ttu-id="0ce06-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="0ce06-118">-IpsecPolicies</span></span>
<span data-ttu-id="0ce06-119">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="0ce06-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="0ce06-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="0ce06-120">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="0ce06-121">-位置</span><span class="sxs-lookup"><span data-stu-id="0ce06-121">-Location</span></span>
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

### <span data-ttu-id="0ce06-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ce06-122">-Name</span></span>
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

### <span data-ttu-id="0ce06-123">對等</span><span class="sxs-lookup"><span data-stu-id="0ce06-123">-Peer</span></span>
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

### <span data-ttu-id="0ce06-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="0ce06-124">-PeerId</span></span>
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

### <span data-ttu-id="0ce06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce06-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0ce06-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="0ce06-126">-RoutingWeight</span></span>
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

### <span data-ttu-id="0ce06-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="0ce06-127">-SharedKey</span></span>
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

### <span data-ttu-id="0ce06-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ce06-128">-Tag</span></span>
<span data-ttu-id="0ce06-129">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0ce06-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0ce06-130">例如：</span><span class="sxs-lookup"><span data-stu-id="0ce06-130">For example:</span></span>

<span data-ttu-id="0ce06-131">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0ce06-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0ce06-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="0ce06-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="0ce06-133">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="0ce06-133">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="0ce06-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="0ce06-134">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="0ce06-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="0ce06-135">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="0ce06-136">-確認</span><span class="sxs-lookup"><span data-stu-id="0ce06-136">-Confirm</span></span>
<span data-ttu-id="0ce06-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0ce06-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce06-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce06-138">-WhatIf</span></span>
<span data-ttu-id="0ce06-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ce06-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce06-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ce06-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce06-141">CommonParameters</span></span>
<span data-ttu-id="0ce06-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ce06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce06-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ce06-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce06-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0ce06-144">INPUTS</span></span>

## <span data-ttu-id="0ce06-145">輸出</span><span class="sxs-lookup"><span data-stu-id="0ce06-145">OUTPUTS</span></span>

### <span data-ttu-id="0ce06-146">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0ce06-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ce06-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0ce06-147">NOTES</span></span>

## <span data-ttu-id="0ce06-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ce06-148">RELATED LINKS</span></span>

[<span data-ttu-id="0ce06-149">AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce06-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0ce06-150">移除-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce06-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0ce06-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce06-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
