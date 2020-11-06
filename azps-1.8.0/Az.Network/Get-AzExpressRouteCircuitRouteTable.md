---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: bb6ffb1537a5beb6a845bbad742b864360da55d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622043"
---
# <span data-ttu-id="a3c7a-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c7a-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="a3c7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c7a-103">從 ExpressRoute 回路取得路由表。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3c7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3c7a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3c7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="a3c7a-106">**AzExpressRouteCircuitRouteTable** Cmdlet 會檢索 ExpressRoute 回路的詳細路由表。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="a3c7a-107">[路由] 表格會顯示所有路由，或可以篩選，以顯示特定對等類型的路線。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="a3c7a-108">您可以使用路由表來驗證對等設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="a3c7a-109">示例</span><span class="sxs-lookup"><span data-stu-id="a3c7a-109">EXAMPLES</span></span>

### <span data-ttu-id="a3c7a-110">範例1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="a3c7a-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a3c7a-111">參數</span><span class="sxs-lookup"><span data-stu-id="a3c7a-111">PARAMETERS</span></span>

### <span data-ttu-id="a3c7a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c7a-112">-DefaultProfile</span></span>
<span data-ttu-id="a3c7a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3c7a-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a3c7a-114">-DevicePath</span></span>
<span data-ttu-id="a3c7a-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a3c7a-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a3c7a-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a3c7a-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a3c7a-117">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a3c7a-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a3c7a-118">-PeeringType</span></span>
<span data-ttu-id="a3c7a-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a3c7a-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a3c7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3c7a-121">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a3c7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c7a-122">CommonParameters</span></span>
<span data-ttu-id="a3c7a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c7a-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3c7a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c7a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a3c7a-125">INPUTS</span></span>

### <span data-ttu-id="a3c7a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="a3c7a-126">System.String</span></span>

## <span data-ttu-id="a3c7a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a3c7a-127">OUTPUTS</span></span>

### <span data-ttu-id="a3c7a-128">PSExpressRouteCircuitRoutesTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3c7a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="a3c7a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a3c7a-129">NOTES</span></span>

## <span data-ttu-id="a3c7a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3c7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="a3c7a-131">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a3c7a-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a3c7a-132">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a3c7a-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a3c7a-133">AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a3c7a-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
