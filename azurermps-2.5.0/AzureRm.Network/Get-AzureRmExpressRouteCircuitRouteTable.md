---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801266"
---
# <span data-ttu-id="76a28-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a28-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="76a28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76a28-102">SYNOPSIS</span></span>
<span data-ttu-id="76a28-103">從 ExpressRoute 回路取得路由表。</span><span class="sxs-lookup"><span data-stu-id="76a28-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a28-104">句法</span><span class="sxs-lookup"><span data-stu-id="76a28-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76a28-105">說明</span><span class="sxs-lookup"><span data-stu-id="76a28-105">DESCRIPTION</span></span>
<span data-ttu-id="76a28-106">**AzureRmExpressRouteCircuitRouteTable** Cmdlet 會檢索 ExpressRoute 回路的詳細路由表。</span><span class="sxs-lookup"><span data-stu-id="76a28-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="76a28-107">[路由] 表格會顯示所有路由，或可以篩選，以顯示特定對等類型的路線。</span><span class="sxs-lookup"><span data-stu-id="76a28-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="76a28-108">您可以使用路由表來驗證對等設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="76a28-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="76a28-109">示例</span><span class="sxs-lookup"><span data-stu-id="76a28-109">EXAMPLES</span></span>

### <span data-ttu-id="76a28-110">範例1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="76a28-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="76a28-111">參數</span><span class="sxs-lookup"><span data-stu-id="76a28-111">PARAMETERS</span></span>

### <span data-ttu-id="76a28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a28-112">-DefaultProfile</span></span>
<span data-ttu-id="76a28-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76a28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76a28-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="76a28-114">-DevicePath</span></span>
<span data-ttu-id="76a28-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="76a28-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a28-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="76a28-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="76a28-117">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="76a28-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a28-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="76a28-118">-PeeringType</span></span>
<span data-ttu-id="76a28-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="76a28-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a28-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a28-120">-ResourceGroupName</span></span>
<span data-ttu-id="76a28-121">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a28-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="76a28-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a28-122">CommonParameters</span></span>
<span data-ttu-id="76a28-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76a28-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a28-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76a28-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a28-125">輸入</span><span class="sxs-lookup"><span data-stu-id="76a28-125">INPUTS</span></span>

## <span data-ttu-id="76a28-126">輸出</span><span class="sxs-lookup"><span data-stu-id="76a28-126">OUTPUTS</span></span>

### <span data-ttu-id="76a28-127">PSExpressRouteCircuitRoutesTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76a28-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="76a28-128">筆記</span><span class="sxs-lookup"><span data-stu-id="76a28-128">NOTES</span></span>

## <span data-ttu-id="76a28-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="76a28-129">RELATED LINKS</span></span>

[<span data-ttu-id="76a28-130">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="76a28-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="76a28-131">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76a28-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="76a28-132">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="76a28-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
