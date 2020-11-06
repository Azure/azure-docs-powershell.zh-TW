---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 204d70753d3a4ae80e05dfff90d4a5b50b47ab58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456016"
---
# <span data-ttu-id="f6f42-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f6f42-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f6f42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6f42-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f42-103">取得 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="f6f42-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f42-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6f42-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f42-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6f42-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f42-106">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會針對 ExpressRoute 回路檢索對等關係的設定。</span><span class="sxs-lookup"><span data-stu-id="f6f42-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f6f42-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6f42-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f42-108">範例1：顯示 ExpressRoute 回路的對等設定</span><span class="sxs-lookup"><span data-stu-id="f6f42-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f6f42-109">參數</span><span class="sxs-lookup"><span data-stu-id="f6f42-109">PARAMETERS</span></span>

### <span data-ttu-id="f6f42-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f42-110">-DefaultProfile</span></span>
<span data-ttu-id="f6f42-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6f42-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f42-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6f42-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f6f42-113">包含對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="f6f42-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f42-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6f42-114">-Name</span></span>
<span data-ttu-id="f6f42-115">要檢索之對等配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6f42-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6f42-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f42-116">CommonParameters</span></span>
<span data-ttu-id="f6f42-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6f42-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f42-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6f42-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f42-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f6f42-119">INPUTS</span></span>

### <span data-ttu-id="f6f42-120">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6f42-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="f6f42-121">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f6f42-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="f6f42-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f6f42-122">OUTPUTS</span></span>

### <span data-ttu-id="f6f42-123">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6f42-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f6f42-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f6f42-124">NOTES</span></span>

## <span data-ttu-id="f6f42-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6f42-125">RELATED LINKS</span></span>

[<span data-ttu-id="f6f42-126">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f6f42-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f6f42-127">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f6f42-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f6f42-128">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f6f42-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f6f42-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6f42-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
