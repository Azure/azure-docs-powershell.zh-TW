---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: b4e93b89a11d4341b6a04de1b5625084e9348c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452460"
---
# <span data-ttu-id="a6dd5-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a6dd5-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="a6dd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dd5-103">取得 ExpressRoute 回路的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6dd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6dd5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6dd5-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="a6dd5-106">AzureRmExpressRouteCircuitRouteTableSummary Cmdlet 會針對特定路由內容， **取得** BGP 鄰居資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="a6dd5-107">此資訊對判斷路由內容已建立的時間，以及對等路由器宣告的路由首碼數量很有用。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="a6dd5-108">示例</span><span class="sxs-lookup"><span data-stu-id="a6dd5-108">EXAMPLES</span></span>

### <span data-ttu-id="a6dd5-109">範例1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="a6dd5-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a6dd5-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6dd5-110">PARAMETERS</span></span>

### <span data-ttu-id="a6dd5-111">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a6dd5-111">-DevicePath</span></span>
<span data-ttu-id="a6dd5-112">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a6dd5-112">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a6dd5-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a6dd5-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a6dd5-114">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a6dd5-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a6dd5-115">-PeeringType</span></span>
<span data-ttu-id="a6dd5-116">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a6dd5-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a6dd5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6dd5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6dd5-118">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a6dd5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dd5-119">-DefaultProfile</span></span>
<span data-ttu-id="a6dd5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6dd5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dd5-121">CommonParameters</span></span>
<span data-ttu-id="a6dd5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6dd5-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6dd5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dd5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a6dd5-124">INPUTS</span></span>

## <span data-ttu-id="a6dd5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a6dd5-125">OUTPUTS</span></span>

### <span data-ttu-id="a6dd5-126">PSExpressRouteCircuitRoutesTableSummary 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6dd5-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="a6dd5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a6dd5-127">NOTES</span></span>

## <span data-ttu-id="a6dd5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6dd5-128">RELATED LINKS</span></span>

[<span data-ttu-id="a6dd5-129">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a6dd5-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a6dd5-130">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6dd5-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a6dd5-131">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a6dd5-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
