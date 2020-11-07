---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: b01e0ecb48a5a4c27fc79448ca0e4d71e820d292
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965514"
---
# <span data-ttu-id="72b61-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72b61-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="72b61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72b61-102">SYNOPSIS</span></span>
<span data-ttu-id="72b61-103">移除 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="72b61-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="72b61-104">句法</span><span class="sxs-lookup"><span data-stu-id="72b61-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72b61-105">說明</span><span class="sxs-lookup"><span data-stu-id="72b61-105">DESCRIPTION</span></span>
<span data-ttu-id="72b61-106">**AzExpressRouteCircuitConnectionConfig** Cmdlet 會移除與指定快速路由線路相關聯的 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="72b61-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="72b61-107">示例</span><span class="sxs-lookup"><span data-stu-id="72b61-107">EXAMPLES</span></span>

### <span data-ttu-id="72b61-108">範例1：從 ExpressRoute 回路中移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="72b61-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="72b61-109">範例2：使用 ExpressRoute 線路中的管道移除電路連線設定</span><span class="sxs-lookup"><span data-stu-id="72b61-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="72b61-110">參數</span><span class="sxs-lookup"><span data-stu-id="72b61-110">PARAMETERS</span></span>

### <span data-ttu-id="72b61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b61-111">-DefaultProfile</span></span>
<span data-ttu-id="72b61-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72b61-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72b61-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72b61-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="72b61-114">包含要移除之對等設定的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="72b61-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="72b61-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="72b61-115">-Name</span></span>
<span data-ttu-id="72b61-116">要移除之電路連接設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="72b61-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="72b61-117">-確認</span><span class="sxs-lookup"><span data-stu-id="72b61-117">-Confirm</span></span>
<span data-ttu-id="72b61-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72b61-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72b61-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b61-119">-WhatIf</span></span>
<span data-ttu-id="72b61-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72b61-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72b61-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72b61-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72b61-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b61-122">CommonParameters</span></span>
<span data-ttu-id="72b61-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72b61-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b61-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72b61-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b61-125">輸入</span><span class="sxs-lookup"><span data-stu-id="72b61-125">INPUTS</span></span>

### <span data-ttu-id="72b61-126">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72b61-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="72b61-127">輸出</span><span class="sxs-lookup"><span data-stu-id="72b61-127">OUTPUTS</span></span>

### <span data-ttu-id="72b61-128">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72b61-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="72b61-129">筆記</span><span class="sxs-lookup"><span data-stu-id="72b61-129">NOTES</span></span>

## <span data-ttu-id="72b61-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="72b61-130">RELATED LINKS</span></span>

[<span data-ttu-id="72b61-131">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72b61-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="72b61-132">AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72b61-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72b61-133">附加 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72b61-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72b61-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72b61-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72b61-135">新-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72b61-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72b61-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72b61-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="72b61-137">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72b61-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)