---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448325"
---
# <span data-ttu-id="52322-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52322-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="52322-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52322-102">SYNOPSIS</span></span>
<span data-ttu-id="52322-103">移除 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="52322-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52322-104">句法</span><span class="sxs-lookup"><span data-stu-id="52322-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52322-105">說明</span><span class="sxs-lookup"><span data-stu-id="52322-105">DESCRIPTION</span></span>
<span data-ttu-id="52322-106">**AzureRmExpressRouteCircuitConnectionConfig** Cmdlet 會移除與指定快速路由線路相關聯的 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="52322-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="52322-107">示例</span><span class="sxs-lookup"><span data-stu-id="52322-107">EXAMPLES</span></span>

### <span data-ttu-id="52322-108">範例1：從 ExpressRoute 回路中移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="52322-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="52322-109">範例2：使用 ExpressRoute 線路中的管道移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="52322-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="52322-110">參數</span><span class="sxs-lookup"><span data-stu-id="52322-110">PARAMETERS</span></span>

### <span data-ttu-id="52322-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52322-111">-DefaultProfile</span></span>
<span data-ttu-id="52322-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52322-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52322-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52322-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="52322-114">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="52322-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="52322-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="52322-115">-Name</span></span>
<span data-ttu-id="52322-116">要移除之電路連接設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="52322-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="52322-117">-確認</span><span class="sxs-lookup"><span data-stu-id="52322-117">-Confirm</span></span>
<span data-ttu-id="52322-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52322-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52322-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52322-119">-WhatIf</span></span>
<span data-ttu-id="52322-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52322-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52322-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52322-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52322-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52322-122">CommonParameters</span></span>
<span data-ttu-id="52322-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52322-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52322-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52322-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52322-125">輸入</span><span class="sxs-lookup"><span data-stu-id="52322-125">INPUTS</span></span>

### <span data-ttu-id="52322-126">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52322-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="52322-127">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="52322-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="52322-128">輸出</span><span class="sxs-lookup"><span data-stu-id="52322-128">OUTPUTS</span></span>

### <span data-ttu-id="52322-129">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52322-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="52322-130">筆記</span><span class="sxs-lookup"><span data-stu-id="52322-130">NOTES</span></span>

## <span data-ttu-id="52322-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="52322-131">RELATED LINKS</span></span>

[<span data-ttu-id="52322-132">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52322-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="52322-133">AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52322-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52322-134">附加 AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52322-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52322-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52322-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52322-136">新-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52322-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="52322-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52322-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="52322-138">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52322-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
