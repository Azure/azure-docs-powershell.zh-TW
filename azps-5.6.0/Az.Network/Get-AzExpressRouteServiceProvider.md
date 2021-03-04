---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: c27ac0c2a56000465b70810ca1e957b882fa3357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903162"
---
# <span data-ttu-id="96100-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="96100-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="96100-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96100-102">SYNOPSIS</span></span>
<span data-ttu-id="96100-103">獲得 ExpressRoute 服務提供者及其屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="96100-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="96100-104">語法</span><span class="sxs-lookup"><span data-stu-id="96100-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96100-105">描述</span><span class="sxs-lookup"><span data-stu-id="96100-105">DESCRIPTION</span></span>
<span data-ttu-id="96100-106">**Get-AzExpressRouteServiceProvider Cmdlet** 會取得 ExpressRoute 服務提供者及其屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="96100-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="96100-107">屬性包括位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="96100-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="96100-108">例子</span><span class="sxs-lookup"><span data-stu-id="96100-108">EXAMPLES</span></span>

### <span data-ttu-id="96100-109">範例 1：在「矽谷」中取得具有位置的服務提供者清單</span><span class="sxs-lookup"><span data-stu-id="96100-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="96100-110">參數</span><span class="sxs-lookup"><span data-stu-id="96100-110">PARAMETERS</span></span>

### <span data-ttu-id="96100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96100-111">-DefaultProfile</span></span>
<span data-ttu-id="96100-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96100-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96100-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96100-113">CommonParameters</span></span>
<span data-ttu-id="96100-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96100-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96100-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96100-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96100-116">輸入</span><span class="sxs-lookup"><span data-stu-id="96100-116">INPUTS</span></span>

### <span data-ttu-id="96100-117">沒有</span><span class="sxs-lookup"><span data-stu-id="96100-117">None</span></span>

## <span data-ttu-id="96100-118">輸出</span><span class="sxs-lookup"><span data-stu-id="96100-118">OUTPUTS</span></span>

### <span data-ttu-id="96100-119">Microsoft.Azure.Commands.Network.models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="96100-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="96100-120">筆記</span><span class="sxs-lookup"><span data-stu-id="96100-120">NOTES</span></span>

## <span data-ttu-id="96100-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="96100-121">RELATED LINKS</span></span>

[<span data-ttu-id="96100-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="96100-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="96100-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="96100-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="96100-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="96100-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="96100-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="96100-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
