---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913833"
---
# <span data-ttu-id="d9700-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d9700-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="d9700-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9700-102">SYNOPSIS</span></span>
<span data-ttu-id="d9700-103">獲得 ExpressRoute 回路的使用統計資料。</span><span class="sxs-lookup"><span data-stu-id="d9700-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d9700-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9700-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9700-105">描述</span><span class="sxs-lookup"><span data-stu-id="d9700-105">DESCRIPTION</span></span>
<span data-ttu-id="d9700-106">**Get-AzExpressRouteCircuitStat** Cmdlet 會檢索 ExpressRoute 回路的流量統計資料。</span><span class="sxs-lookup"><span data-stu-id="d9700-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="d9700-107">統計資料包括主要和次要路由上所送出及接收的位元組數。</span><span class="sxs-lookup"><span data-stu-id="d9700-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="d9700-108">例子</span><span class="sxs-lookup"><span data-stu-id="d9700-108">EXAMPLES</span></span>

### <span data-ttu-id="d9700-109">範例 1：顯示 ExpressRoute 對等程式的流量統計資料</span><span class="sxs-lookup"><span data-stu-id="d9700-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="d9700-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9700-110">PARAMETERS</span></span>

### <span data-ttu-id="d9700-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9700-111">-DefaultProfile</span></span>
<span data-ttu-id="d9700-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9700-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9700-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d9700-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d9700-114">要檢查的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="d9700-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d9700-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d9700-115">-PeeringType</span></span>
<span data-ttu-id="d9700-116">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d9700-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d9700-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9700-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9700-118">包含 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d9700-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d9700-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9700-119">CommonParameters</span></span>
<span data-ttu-id="d9700-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9700-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9700-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9700-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9700-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d9700-122">INPUTS</span></span>

### <span data-ttu-id="d9700-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d9700-123">System.String</span></span>

## <span data-ttu-id="d9700-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d9700-124">OUTPUTS</span></span>

### <span data-ttu-id="d9700-125">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="d9700-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="d9700-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d9700-126">NOTES</span></span>

## <span data-ttu-id="d9700-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9700-127">RELATED LINKS</span></span>

[<span data-ttu-id="d9700-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d9700-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d9700-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d9700-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="d9700-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d9700-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
