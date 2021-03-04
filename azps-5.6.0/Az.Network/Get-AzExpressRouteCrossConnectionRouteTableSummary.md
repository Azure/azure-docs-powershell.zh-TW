---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: d5b6d1b9e5d3955b7ecbff9dec02405e030bbf33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908821"
---
# <span data-ttu-id="b7492-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7492-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="b7492-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7492-102">SYNOPSIS</span></span>
<span data-ttu-id="b7492-103">獲得 ExpressRoute 交叉連接的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="b7492-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="b7492-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7492-104">SYNTAX</span></span>

### <span data-ttu-id="b7492-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="b7492-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7492-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="b7492-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7492-107">描述</span><span class="sxs-lookup"><span data-stu-id="b7492-107">DESCRIPTION</span></span>
<span data-ttu-id="b7492-108">**Get-AzExpressRouteCrossConnectionRouteTableSummary Cmdlet** 會針對特定路由上下文，取得 BGP 相鄰資訊的摘要。</span><span class="sxs-lookup"><span data-stu-id="b7492-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b7492-109">此資訊很適合用於判斷路由上下文的建立時間，以及對等路由器所宣告的路由首碼數目。</span><span class="sxs-lookup"><span data-stu-id="b7492-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b7492-110">例子</span><span class="sxs-lookup"><span data-stu-id="b7492-110">EXAMPLES</span></span>

### <span data-ttu-id="b7492-111">範例 1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="b7492-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="b7492-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7492-112">PARAMETERS</span></span>

### <span data-ttu-id="b7492-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="b7492-113">-CrossConnectionName</span></span>
<span data-ttu-id="b7492-114">Express Route 交叉連接的名稱</span><span class="sxs-lookup"><span data-stu-id="b7492-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="b7492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7492-115">-DefaultProfile</span></span>
<span data-ttu-id="b7492-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7492-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7492-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b7492-117">-DevicePath</span></span>
<span data-ttu-id="b7492-118">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b7492-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="b7492-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7492-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b7492-120">Express Route 交叉連接</span><span class="sxs-lookup"><span data-stu-id="b7492-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="b7492-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b7492-121">-PeeringType</span></span>
<span data-ttu-id="b7492-122">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b7492-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b7492-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7492-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7492-124">包含 ExpressRoute 交叉連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b7492-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="b7492-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7492-125">CommonParameters</span></span>
<span data-ttu-id="b7492-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7492-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7492-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7492-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7492-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b7492-128">INPUTS</span></span>

### <span data-ttu-id="b7492-129">沒有</span><span class="sxs-lookup"><span data-stu-id="b7492-129">None</span></span>
<span data-ttu-id="b7492-130">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b7492-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7492-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b7492-131">OUTPUTS</span></span>

### <span data-ttu-id="b7492-132">Microsoft.Azure.Commands.Network.models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7492-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="b7492-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b7492-133">NOTES</span></span>

## <span data-ttu-id="b7492-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7492-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7492-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="b7492-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="b7492-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7492-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
