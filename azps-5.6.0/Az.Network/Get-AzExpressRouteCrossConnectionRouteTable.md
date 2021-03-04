---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908822"
---
# <span data-ttu-id="11531-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="11531-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="11531-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11531-102">SYNOPSIS</span></span>
<span data-ttu-id="11531-103">從 ExpressRoute 交叉連接獲得路由資料表。</span><span class="sxs-lookup"><span data-stu-id="11531-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="11531-104">語法</span><span class="sxs-lookup"><span data-stu-id="11531-104">SYNTAX</span></span>

### <span data-ttu-id="11531-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="11531-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11531-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="11531-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11531-107">描述</span><span class="sxs-lookup"><span data-stu-id="11531-107">DESCRIPTION</span></span>
<span data-ttu-id="11531-108">**Get-AzExpressRouteCrossConnectionRouteTable** Cmdlet 會取得 ExpressRoute 回路的詳細路由資料表。</span><span class="sxs-lookup"><span data-stu-id="11531-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="11531-109">路由資料表會顯示所有路由，或可以篩選以顯示特定對等類型的路由。</span><span class="sxs-lookup"><span data-stu-id="11531-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="11531-110">您可以使用路由資料表驗證對等配置和連接。</span><span class="sxs-lookup"><span data-stu-id="11531-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="11531-111">例子</span><span class="sxs-lookup"><span data-stu-id="11531-111">EXAMPLES</span></span>

### <span data-ttu-id="11531-112">範例 1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="11531-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="11531-113">參數</span><span class="sxs-lookup"><span data-stu-id="11531-113">PARAMETERS</span></span>

### <span data-ttu-id="11531-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="11531-114">-CrossConnectionName</span></span>
<span data-ttu-id="11531-115">Express Route 交叉連接的名稱</span><span class="sxs-lookup"><span data-stu-id="11531-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11531-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11531-116">-DefaultProfile</span></span>
<span data-ttu-id="11531-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11531-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11531-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="11531-118">-DevicePath</span></span>
<span data-ttu-id="11531-119">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="11531-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="11531-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="11531-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="11531-121">Express Route 交叉連接</span><span class="sxs-lookup"><span data-stu-id="11531-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11531-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="11531-122">-PeeringType</span></span>
<span data-ttu-id="11531-123">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="11531-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="11531-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11531-124">-ResourceGroupName</span></span>
<span data-ttu-id="11531-125">包含 ExpressRoute 交叉連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="11531-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11531-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11531-126">CommonParameters</span></span>
<span data-ttu-id="11531-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11531-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11531-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11531-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11531-129">輸入</span><span class="sxs-lookup"><span data-stu-id="11531-129">INPUTS</span></span>

### <span data-ttu-id="11531-130">沒有</span><span class="sxs-lookup"><span data-stu-id="11531-130">None</span></span>
<span data-ttu-id="11531-131">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="11531-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11531-132">輸出</span><span class="sxs-lookup"><span data-stu-id="11531-132">OUTPUTS</span></span>

### <span data-ttu-id="11531-133">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="11531-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="11531-134">筆記</span><span class="sxs-lookup"><span data-stu-id="11531-134">NOTES</span></span>

## <span data-ttu-id="11531-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="11531-135">RELATED LINKS</span></span>

[<span data-ttu-id="11531-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="11531-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="11531-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11531-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
