---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137676"
---
# <span data-ttu-id="76ef5-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76ef5-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="76ef5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="76ef5-103">取得 ExpressRoute 回路的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="76ef5-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="76ef5-104">句法</span><span class="sxs-lookup"><span data-stu-id="76ef5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76ef5-105">說明</span><span class="sxs-lookup"><span data-stu-id="76ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="76ef5-106">AzExpressRouteCircuitRouteTableSummary Cmdlet 會針對特定路由內容， **取得** BGP 鄰居資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="76ef5-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="76ef5-107">此資訊對判斷路由內容已建立的時間，以及對等路由器宣告的路由首碼數量很有用。</span><span class="sxs-lookup"><span data-stu-id="76ef5-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="76ef5-108">示例</span><span class="sxs-lookup"><span data-stu-id="76ef5-108">EXAMPLES</span></span>

### <span data-ttu-id="76ef5-109">範例1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="76ef5-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="76ef5-110">參數</span><span class="sxs-lookup"><span data-stu-id="76ef5-110">PARAMETERS</span></span>

### <span data-ttu-id="76ef5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ef5-111">-DefaultProfile</span></span>
<span data-ttu-id="76ef5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76ef5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ef5-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="76ef5-113">-DevicePath</span></span>
<span data-ttu-id="76ef5-114">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="76ef5-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="76ef5-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="76ef5-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="76ef5-116">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="76ef5-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="76ef5-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="76ef5-117">-PeeringType</span></span>
<span data-ttu-id="76ef5-118">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="76ef5-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="76ef5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ef5-119">-ResourceGroupName</span></span>
<span data-ttu-id="76ef5-120">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76ef5-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="76ef5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ef5-121">CommonParameters</span></span>
<span data-ttu-id="76ef5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76ef5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ef5-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="76ef5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ef5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="76ef5-124">INPUTS</span></span>

### <span data-ttu-id="76ef5-125">System.object</span><span class="sxs-lookup"><span data-stu-id="76ef5-125">System.String</span></span>

## <span data-ttu-id="76ef5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="76ef5-126">OUTPUTS</span></span>

### <span data-ttu-id="76ef5-127">PSExpressRouteCircuitRoutesTableSummary 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76ef5-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="76ef5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="76ef5-128">NOTES</span></span>

## <span data-ttu-id="76ef5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="76ef5-129">RELATED LINKS</span></span>

[<span data-ttu-id="76ef5-130">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="76ef5-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="76ef5-131">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="76ef5-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="76ef5-132">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="76ef5-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
