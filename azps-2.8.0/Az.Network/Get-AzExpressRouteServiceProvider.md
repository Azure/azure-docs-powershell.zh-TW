---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790117"
---
# <span data-ttu-id="23364-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="23364-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="23364-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23364-102">SYNOPSIS</span></span>
<span data-ttu-id="23364-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="23364-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="23364-104">句法</span><span class="sxs-lookup"><span data-stu-id="23364-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23364-105">說明</span><span class="sxs-lookup"><span data-stu-id="23364-105">DESCRIPTION</span></span>
<span data-ttu-id="23364-106">**AzExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="23364-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="23364-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="23364-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="23364-108">示例</span><span class="sxs-lookup"><span data-stu-id="23364-108">EXAMPLES</span></span>

### <span data-ttu-id="23364-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="23364-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="23364-110">參數</span><span class="sxs-lookup"><span data-stu-id="23364-110">PARAMETERS</span></span>

### <span data-ttu-id="23364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23364-111">-DefaultProfile</span></span>
<span data-ttu-id="23364-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23364-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23364-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23364-113">CommonParameters</span></span>
<span data-ttu-id="23364-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23364-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23364-115">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23364-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23364-116">輸入</span><span class="sxs-lookup"><span data-stu-id="23364-116">INPUTS</span></span>

### <span data-ttu-id="23364-117">所有</span><span class="sxs-lookup"><span data-stu-id="23364-117">None</span></span>

## <span data-ttu-id="23364-118">輸出</span><span class="sxs-lookup"><span data-stu-id="23364-118">OUTPUTS</span></span>

### <span data-ttu-id="23364-119">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23364-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="23364-120">筆記</span><span class="sxs-lookup"><span data-stu-id="23364-120">NOTES</span></span>

## <span data-ttu-id="23364-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="23364-121">RELATED LINKS</span></span>

[<span data-ttu-id="23364-122">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="23364-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="23364-123">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="23364-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="23364-124">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="23364-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="23364-125">AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="23364-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
