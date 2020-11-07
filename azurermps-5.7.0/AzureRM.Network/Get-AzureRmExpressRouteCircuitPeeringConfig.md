---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 223f2a02dcf6d2310109b41587126f374a6733b1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626648"
---
# <span data-ttu-id="8c38e-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8c38e-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8c38e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c38e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c38e-103">取得 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="8c38e-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c38e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c38e-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c38e-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c38e-105">DESCRIPTION</span></span>
<span data-ttu-id="8c38e-106">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet 會針對 ExpressRoute 回路檢索對等關係的設定。</span><span class="sxs-lookup"><span data-stu-id="8c38e-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8c38e-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c38e-107">EXAMPLES</span></span>

### <span data-ttu-id="8c38e-108">範例1：顯示 ExpressRoute 回路的對等設定</span><span class="sxs-lookup"><span data-stu-id="8c38e-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="8c38e-109">參數</span><span class="sxs-lookup"><span data-stu-id="8c38e-109">PARAMETERS</span></span>

### <span data-ttu-id="8c38e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c38e-110">-DefaultProfile</span></span>
<span data-ttu-id="8c38e-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c38e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c38e-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8c38e-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8c38e-113">包含對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="8c38e-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c38e-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c38e-114">-Name</span></span>
<span data-ttu-id="8c38e-115">要檢索之對等配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c38e-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c38e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c38e-116">CommonParameters</span></span>
<span data-ttu-id="8c38e-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c38e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c38e-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c38e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c38e-119">輸入</span><span class="sxs-lookup"><span data-stu-id="8c38e-119">INPUTS</span></span>

### <span data-ttu-id="8c38e-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8c38e-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8c38e-121">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8c38e-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8c38e-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8c38e-122">OUTPUTS</span></span>

### <span data-ttu-id="8c38e-123">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c38e-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="8c38e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="8c38e-124">NOTES</span></span>

## <span data-ttu-id="8c38e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c38e-125">RELATED LINKS</span></span>

[<span data-ttu-id="8c38e-126">附加 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8c38e-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8c38e-127">新-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8c38e-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8c38e-128">移除-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8c38e-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8c38e-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8c38e-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
