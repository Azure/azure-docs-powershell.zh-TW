---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 5042f7055c9d74dcabc01aa81169c9290816953c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794426"
---
# <span data-ttu-id="24990-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="24990-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="24990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24990-102">SYNOPSIS</span></span>
<span data-ttu-id="24990-103">取得 ExpressRoute 回路的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="24990-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="24990-104">句法</span><span class="sxs-lookup"><span data-stu-id="24990-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24990-105">說明</span><span class="sxs-lookup"><span data-stu-id="24990-105">DESCRIPTION</span></span>
<span data-ttu-id="24990-106">AzExpressRouteCircuitRouteTableSummary Cmdlet 會針對特定路由內容， **取得** BGP 鄰居資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="24990-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="24990-107">此資訊對判斷路由內容已建立的時間，以及對等路由器宣告的路由首碼數量很有用。</span><span class="sxs-lookup"><span data-stu-id="24990-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="24990-108">示例</span><span class="sxs-lookup"><span data-stu-id="24990-108">EXAMPLES</span></span>

### <span data-ttu-id="24990-109">範例1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="24990-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="24990-110">參數</span><span class="sxs-lookup"><span data-stu-id="24990-110">PARAMETERS</span></span>

### <span data-ttu-id="24990-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24990-111">-DefaultProfile</span></span>
<span data-ttu-id="24990-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24990-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24990-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="24990-113">-DevicePath</span></span>
<span data-ttu-id="24990-114">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="24990-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="24990-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="24990-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="24990-116">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="24990-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="24990-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="24990-117">-PeeringType</span></span>
<span data-ttu-id="24990-118">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="24990-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="24990-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24990-119">-ResourceGroupName</span></span>
<span data-ttu-id="24990-120">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24990-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="24990-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24990-121">CommonParameters</span></span>
<span data-ttu-id="24990-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24990-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24990-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24990-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24990-124">輸入</span><span class="sxs-lookup"><span data-stu-id="24990-124">INPUTS</span></span>

## <span data-ttu-id="24990-125">輸出</span><span class="sxs-lookup"><span data-stu-id="24990-125">OUTPUTS</span></span>

### <span data-ttu-id="24990-126">PSExpressRouteCircuitRoutesTableSummary 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24990-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="24990-127">筆記</span><span class="sxs-lookup"><span data-stu-id="24990-127">NOTES</span></span>

## <span data-ttu-id="24990-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="24990-128">RELATED LINKS</span></span>

[<span data-ttu-id="24990-129">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="24990-129">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="24990-130">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="24990-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="24990-131">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="24990-131">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
