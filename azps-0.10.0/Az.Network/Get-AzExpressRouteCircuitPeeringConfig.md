---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794430"
---
# <span data-ttu-id="c2c92-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c2c92-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c2c92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2c92-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c92-103">取得 ExpressRoute 線路對等設定。</span><span class="sxs-lookup"><span data-stu-id="c2c92-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="c2c92-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2c92-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c92-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2c92-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c92-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet 會針對 ExpressRoute 回路檢索對等關係的設定。</span><span class="sxs-lookup"><span data-stu-id="c2c92-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c2c92-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2c92-107">EXAMPLES</span></span>

### <span data-ttu-id="c2c92-108">範例1：顯示 ExpressRoute 回路的對等設定</span><span class="sxs-lookup"><span data-stu-id="c2c92-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="c2c92-109">參數</span><span class="sxs-lookup"><span data-stu-id="c2c92-109">PARAMETERS</span></span>

### <span data-ttu-id="c2c92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c92-110">-DefaultProfile</span></span>
<span data-ttu-id="c2c92-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2c92-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c92-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2c92-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c2c92-113">包含對等設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="c2c92-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="c2c92-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2c92-114">-Name</span></span>
<span data-ttu-id="c2c92-115">要檢索之對等配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2c92-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="c2c92-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c92-116">CommonParameters</span></span>
<span data-ttu-id="c2c92-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2c92-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c92-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2c92-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c92-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c2c92-119">INPUTS</span></span>

### <span data-ttu-id="c2c92-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2c92-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="c2c92-121">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c2c92-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="c2c92-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c2c92-122">OUTPUTS</span></span>

### <span data-ttu-id="c2c92-123">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2c92-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c2c92-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c2c92-124">NOTES</span></span>

## <span data-ttu-id="c2c92-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2c92-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2c92-126">附加 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c2c92-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c2c92-127">新-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c2c92-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c2c92-128">移除-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c2c92-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c2c92-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c2c92-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
