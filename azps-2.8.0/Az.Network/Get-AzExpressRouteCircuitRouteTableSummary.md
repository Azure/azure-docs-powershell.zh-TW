---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: bca0dde2947b214d13032b54681f2fc179c26af1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411530"
---
# <span data-ttu-id="8dd44-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8dd44-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="8dd44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8dd44-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd44-103">獲得 ExpressRoute 回路的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="8dd44-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8dd44-104">語法</span><span class="sxs-lookup"><span data-stu-id="8dd44-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd44-105">描述</span><span class="sxs-lookup"><span data-stu-id="8dd44-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd44-106">**Get-AzExpressRouteRouteCircuitRouteTableSummary Cmdlet** 會針對特定路由上下文，取得 BGP 相鄰資訊的摘要。</span><span class="sxs-lookup"><span data-stu-id="8dd44-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="8dd44-107">此資訊很適合用於判斷路由上下文的建立時間，以及對等路由器所宣告的路由首碼數目。</span><span class="sxs-lookup"><span data-stu-id="8dd44-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="8dd44-108">例子</span><span class="sxs-lookup"><span data-stu-id="8dd44-108">EXAMPLES</span></span>

### <span data-ttu-id="8dd44-109">範例 1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="8dd44-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="8dd44-110">參數</span><span class="sxs-lookup"><span data-stu-id="8dd44-110">PARAMETERS</span></span>

### <span data-ttu-id="8dd44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd44-111">-DefaultProfile</span></span>
<span data-ttu-id="8dd44-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8dd44-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd44-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8dd44-113">-DevicePath</span></span>
<span data-ttu-id="8dd44-114">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8dd44-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8dd44-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="8dd44-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="8dd44-116">要檢查的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="8dd44-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="8dd44-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8dd44-117">-PeeringType</span></span>
<span data-ttu-id="8dd44-118">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8dd44-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8dd44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd44-119">-ResourceGroupName</span></span>
<span data-ttu-id="8dd44-120">包含 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8dd44-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="8dd44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd44-121">CommonParameters</span></span>
<span data-ttu-id="8dd44-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8dd44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd44-123">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dd44-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd44-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8dd44-124">INPUTS</span></span>

### <span data-ttu-id="8dd44-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8dd44-125">System.String</span></span>

## <span data-ttu-id="8dd44-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8dd44-126">OUTPUTS</span></span>

### <span data-ttu-id="8dd44-127">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="8dd44-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="8dd44-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8dd44-128">NOTES</span></span>

## <span data-ttu-id="8dd44-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dd44-129">RELATED LINKS</span></span>

[<span data-ttu-id="8dd44-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8dd44-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="8dd44-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8dd44-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="8dd44-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="8dd44-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
