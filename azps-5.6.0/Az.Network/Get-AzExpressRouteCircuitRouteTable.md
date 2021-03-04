---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 28a61e18f01f550f1b1ffd924119da3323905ad1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913158"
---
# <span data-ttu-id="f4331-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4331-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="f4331-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4331-102">SYNOPSIS</span></span>
<span data-ttu-id="f4331-103">從 ExpressRoute 回路中獲得路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f4331-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f4331-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4331-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4331-105">描述</span><span class="sxs-lookup"><span data-stu-id="f4331-105">DESCRIPTION</span></span>
<span data-ttu-id="f4331-106">**Get-AzExpressRouteCircuitRouteTable** Cmdlet 會取得 ExpressRoute 回路的詳細路由資料表。</span><span class="sxs-lookup"><span data-stu-id="f4331-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="f4331-107">路由資料表會顯示所有路由，或可以篩選以顯示特定對等類型的路由。</span><span class="sxs-lookup"><span data-stu-id="f4331-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="f4331-108">您可以使用路由資料表驗證對等配置和連接。</span><span class="sxs-lookup"><span data-stu-id="f4331-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="f4331-109">例子</span><span class="sxs-lookup"><span data-stu-id="f4331-109">EXAMPLES</span></span>

### <span data-ttu-id="f4331-110">範例 1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="f4331-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f4331-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4331-111">PARAMETERS</span></span>

### <span data-ttu-id="f4331-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4331-112">-DefaultProfile</span></span>
<span data-ttu-id="f4331-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4331-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4331-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f4331-114">-DevicePath</span></span>
<span data-ttu-id="f4331-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f4331-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f4331-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f4331-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f4331-117">要檢查的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="f4331-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f4331-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f4331-118">-PeeringType</span></span>
<span data-ttu-id="f4331-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f4331-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4331-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4331-120">-ResourceGroupName</span></span>
<span data-ttu-id="f4331-121">包含 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f4331-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f4331-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4331-122">CommonParameters</span></span>
<span data-ttu-id="f4331-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4331-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4331-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4331-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4331-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f4331-125">INPUTS</span></span>

### <span data-ttu-id="f4331-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f4331-126">System.String</span></span>

## <span data-ttu-id="f4331-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f4331-127">OUTPUTS</span></span>

### <span data-ttu-id="f4331-128">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="f4331-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="f4331-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f4331-129">NOTES</span></span>

## <span data-ttu-id="f4331-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4331-130">RELATED LINKS</span></span>

[<span data-ttu-id="f4331-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f4331-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f4331-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4331-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f4331-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="f4331-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
