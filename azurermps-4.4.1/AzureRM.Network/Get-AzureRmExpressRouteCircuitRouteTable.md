---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: d2be2927be03895f80a537f70e80c53e246e16f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451639"
---
# <span data-ttu-id="c9162-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9162-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="c9162-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9162-102">SYNOPSIS</span></span>
<span data-ttu-id="c9162-103">從 ExpressRoute 回路取得路由表。</span><span class="sxs-lookup"><span data-stu-id="c9162-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9162-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9162-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9162-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9162-105">DESCRIPTION</span></span>
<span data-ttu-id="c9162-106">**AzureRmExpressRouteCircuitRouteTable** Cmdlet 會檢索 ExpressRoute 回路的詳細路由表。</span><span class="sxs-lookup"><span data-stu-id="c9162-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="c9162-107">[路由] 表格會顯示所有路由，或可以篩選，以顯示特定對等類型的路線。</span><span class="sxs-lookup"><span data-stu-id="c9162-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="c9162-108">您可以使用路由表來驗證對等設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="c9162-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="c9162-109">示例</span><span class="sxs-lookup"><span data-stu-id="c9162-109">EXAMPLES</span></span>

### <span data-ttu-id="c9162-110">範例1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="c9162-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="c9162-111">參數</span><span class="sxs-lookup"><span data-stu-id="c9162-111">PARAMETERS</span></span>

### <span data-ttu-id="c9162-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c9162-112">-DevicePath</span></span>
<span data-ttu-id="c9162-113">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c9162-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9162-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c9162-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c9162-115">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="c9162-115">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9162-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c9162-116">-PeeringType</span></span>
<span data-ttu-id="c9162-117">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c9162-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9162-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9162-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9162-119">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9162-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9162-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9162-120">-DefaultProfile</span></span>
<span data-ttu-id="c9162-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9162-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9162-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9162-122">CommonParameters</span></span>
<span data-ttu-id="c9162-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9162-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9162-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9162-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9162-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c9162-125">INPUTS</span></span>

## <span data-ttu-id="c9162-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c9162-126">OUTPUTS</span></span>

### <span data-ttu-id="c9162-127">PSExpressRouteCircuitRoutesTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c9162-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="c9162-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c9162-128">NOTES</span></span>

## <span data-ttu-id="c9162-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9162-129">RELATED LINKS</span></span>

[<span data-ttu-id="c9162-130">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c9162-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c9162-131">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c9162-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c9162-132">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c9162-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
