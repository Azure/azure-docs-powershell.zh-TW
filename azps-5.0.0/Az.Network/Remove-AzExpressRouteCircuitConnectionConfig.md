---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141088"
---
# <span data-ttu-id="52469-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52469-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="52469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52469-102">SYNOPSIS</span></span>
<span data-ttu-id="52469-103">移除 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="52469-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="52469-104">句法</span><span class="sxs-lookup"><span data-stu-id="52469-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52469-105">說明</span><span class="sxs-lookup"><span data-stu-id="52469-105">DESCRIPTION</span></span>
<span data-ttu-id="52469-106">**AzExpressRouteCircuitConnectionConfig** Cmdlet 會移除與指定快速路由線路相關聯的 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="52469-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="52469-107">示例</span><span class="sxs-lookup"><span data-stu-id="52469-107">EXAMPLES</span></span>

### <span data-ttu-id="52469-108">範例1：從 ExpressRoute 回路中移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="52469-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="52469-109">範例2：使用 ExpressRoute 線路中的管道移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="52469-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="52469-110">範例3：從特定位址族的 ExpressRoute 電路中移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="52469-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="52469-111">範例4：使用管道從特定位址族的 ExpressRoute 電路中移除電路連接設定</span><span class="sxs-lookup"><span data-stu-id="52469-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="52469-112">參數</span><span class="sxs-lookup"><span data-stu-id="52469-112">PARAMETERS</span></span>

### <span data-ttu-id="52469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52469-113">-DefaultProfile</span></span>
<span data-ttu-id="52469-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52469-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52469-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52469-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="52469-116">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="52469-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52469-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="52469-117">-Name</span></span>
<span data-ttu-id="52469-118">要移除之電路連接設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="52469-118">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="52469-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="52469-119">-AddressPrefixType</span></span>
<span data-ttu-id="52469-120">指定需要從 config 中移除的位址族</span><span class="sxs-lookup"><span data-stu-id="52469-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52469-121">-確認</span><span class="sxs-lookup"><span data-stu-id="52469-121">-Confirm</span></span>
<span data-ttu-id="52469-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52469-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52469-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52469-123">-WhatIf</span></span>
<span data-ttu-id="52469-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52469-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52469-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52469-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52469-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52469-126">CommonParameters</span></span>
<span data-ttu-id="52469-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52469-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52469-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52469-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52469-129">輸入</span><span class="sxs-lookup"><span data-stu-id="52469-129">INPUTS</span></span>

### <span data-ttu-id="52469-130">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52469-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="52469-131">輸出</span><span class="sxs-lookup"><span data-stu-id="52469-131">OUTPUTS</span></span>

### <span data-ttu-id="52469-132">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52469-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="52469-133">筆記</span><span class="sxs-lookup"><span data-stu-id="52469-133">NOTES</span></span>

## <span data-ttu-id="52469-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="52469-134">RELATED LINKS</span></span>

[<span data-ttu-id="52469-135">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52469-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="52469-136">AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52469-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52469-137">附加 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52469-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52469-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52469-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52469-139">新-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52469-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52469-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52469-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="52469-141">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52469-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)