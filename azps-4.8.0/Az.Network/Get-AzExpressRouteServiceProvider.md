---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135596"
---
# <span data-ttu-id="b70bd-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b70bd-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b70bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b70bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b70bd-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="b70bd-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="b70bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b70bd-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="b70bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b70bd-106">**AzExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="b70bd-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="b70bd-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="b70bd-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="b70bd-108">示例</span><span class="sxs-lookup"><span data-stu-id="b70bd-108">EXAMPLES</span></span>

### <span data-ttu-id="b70bd-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="b70bd-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="b70bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="b70bd-110">PARAMETERS</span></span>

### <span data-ttu-id="b70bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70bd-111">-DefaultProfile</span></span>
<span data-ttu-id="b70bd-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b70bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70bd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70bd-113">CommonParameters</span></span>
<span data-ttu-id="b70bd-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b70bd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70bd-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b70bd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70bd-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b70bd-116">INPUTS</span></span>

### <span data-ttu-id="b70bd-117">所有</span><span class="sxs-lookup"><span data-stu-id="b70bd-117">None</span></span>

## <span data-ttu-id="b70bd-118">輸出</span><span class="sxs-lookup"><span data-stu-id="b70bd-118">OUTPUTS</span></span>

### <span data-ttu-id="b70bd-119">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b70bd-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b70bd-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b70bd-120">NOTES</span></span>

## <span data-ttu-id="b70bd-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b70bd-121">RELATED LINKS</span></span>

[<span data-ttu-id="b70bd-122">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b70bd-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b70bd-123">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b70bd-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b70bd-124">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b70bd-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b70bd-125">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="b70bd-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
