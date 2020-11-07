---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800462"
---
# <span data-ttu-id="c1f7d-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c1f7d-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="c1f7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f7d-103">從 ExpressRoute 回路取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1f7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1f7d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1f7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1f7d-106">**AzureRmExpressRouteCircuitARPTable** Cmdlet 會從 ExpressRoute 回路的兩個介面中檢索 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="c1f7d-107">ARP 表格提供特定對等的 IPv4 位址到 MAC 位址的對應。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="c1f7d-108">您可以使用 ARP 資料表來驗證第2層設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="c1f7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f7d-110">範例1：顯示 ExpressRoute 對等的 ARP 資料表</span><span class="sxs-lookup"><span data-stu-id="c1f7d-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="c1f7d-111">參數</span><span class="sxs-lookup"><span data-stu-id="c1f7d-111">PARAMETERS</span></span>

### <span data-ttu-id="c1f7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f7d-112">-DefaultProfile</span></span>
<span data-ttu-id="c1f7d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1f7d-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c1f7d-114">-DevicePath</span></span>
<span data-ttu-id="c1f7d-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c1f7d-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="c1f7d-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c1f7d-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c1f7d-117">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="c1f7d-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c1f7d-118">-PeeringType</span></span>
<span data-ttu-id="c1f7d-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c1f7d-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c1f7d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f7d-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1f7d-121">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="c1f7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f7d-122">CommonParameters</span></span>
<span data-ttu-id="c1f7d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f7d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1f7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f7d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c1f7d-125">INPUTS</span></span>

## <span data-ttu-id="c1f7d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c1f7d-126">OUTPUTS</span></span>

### <span data-ttu-id="c1f7d-127">PSExpressRouteCircuitArpTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c1f7d-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="c1f7d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c1f7d-128">NOTES</span></span>

## <span data-ttu-id="c1f7d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1f7d-129">RELATED LINKS</span></span>

[<span data-ttu-id="c1f7d-130">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1f7d-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c1f7d-131">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1f7d-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c1f7d-132">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c1f7d-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
