---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: cf854be6ed6dd5a69ba730cf6da60884a493551e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412379"
---
# <span data-ttu-id="eb765-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eb765-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="eb765-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb765-102">SYNOPSIS</span></span>
<span data-ttu-id="eb765-103">移除 ExpressRoute 回路連接組。</span><span class="sxs-lookup"><span data-stu-id="eb765-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="eb765-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb765-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb765-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb765-105">DESCRIPTION</span></span>
<span data-ttu-id="eb765-106">**Remove-AzExpressRouteRouteCircuitConnectionConfig** Cmdlet 會移除與特定 Express Route 回路相關聯的 ExpressRoute 回路連接組。</span><span class="sxs-lookup"><span data-stu-id="eb765-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="eb765-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb765-107">EXAMPLES</span></span>

### <span data-ttu-id="eb765-108">範例 1：從 ExpressRoute 回路移除回路連接組</span><span class="sxs-lookup"><span data-stu-id="eb765-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="eb765-109">範例 2：從 ExpressRoute 回路使用管道移除回路連接組</span><span class="sxs-lookup"><span data-stu-id="eb765-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="eb765-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb765-110">PARAMETERS</span></span>

### <span data-ttu-id="eb765-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb765-111">-DefaultProfile</span></span>
<span data-ttu-id="eb765-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb765-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb765-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="eb765-114">包含要移除之對等配置的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="eb765-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="eb765-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb765-115">-Name</span></span>
<span data-ttu-id="eb765-116">要移除的回路連接組名。</span><span class="sxs-lookup"><span data-stu-id="eb765-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="eb765-117">-確認</span><span class="sxs-lookup"><span data-stu-id="eb765-117">-Confirm</span></span>
<span data-ttu-id="eb765-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb765-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb765-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb765-119">-WhatIf</span></span>
<span data-ttu-id="eb765-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb765-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb765-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb765-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb765-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb765-122">CommonParameters</span></span>
<span data-ttu-id="eb765-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb765-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb765-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eb765-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb765-125">輸入</span><span class="sxs-lookup"><span data-stu-id="eb765-125">INPUTS</span></span>

### <span data-ttu-id="eb765-126">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eb765-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eb765-127">OUTPUTS</span></span>

### <span data-ttu-id="eb765-128">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eb765-129">筆記</span><span class="sxs-lookup"><span data-stu-id="eb765-129">NOTES</span></span>

## <span data-ttu-id="eb765-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb765-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb765-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="eb765-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eb765-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="eb765-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eb765-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="eb765-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eb765-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)



[<span data-ttu-id="eb765-135">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-135">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="eb765-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eb765-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
