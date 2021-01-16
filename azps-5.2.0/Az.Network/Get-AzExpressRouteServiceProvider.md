---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279276"
---
# <span data-ttu-id="5af23-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="5af23-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="5af23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5af23-102">SYNOPSIS</span></span>
<span data-ttu-id="5af23-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="5af23-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="5af23-104">句法</span><span class="sxs-lookup"><span data-stu-id="5af23-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5af23-105">說明</span><span class="sxs-lookup"><span data-stu-id="5af23-105">DESCRIPTION</span></span>
<span data-ttu-id="5af23-106">**AzExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="5af23-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="5af23-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="5af23-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="5af23-108">示例</span><span class="sxs-lookup"><span data-stu-id="5af23-108">EXAMPLES</span></span>

### <span data-ttu-id="5af23-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="5af23-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="5af23-110">參數</span><span class="sxs-lookup"><span data-stu-id="5af23-110">PARAMETERS</span></span>

### <span data-ttu-id="5af23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af23-111">-DefaultProfile</span></span>
<span data-ttu-id="5af23-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5af23-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5af23-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af23-113">CommonParameters</span></span>
<span data-ttu-id="5af23-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5af23-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af23-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5af23-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af23-116">輸入</span><span class="sxs-lookup"><span data-stu-id="5af23-116">INPUTS</span></span>

### <span data-ttu-id="5af23-117">所有</span><span class="sxs-lookup"><span data-stu-id="5af23-117">None</span></span>

## <span data-ttu-id="5af23-118">輸出</span><span class="sxs-lookup"><span data-stu-id="5af23-118">OUTPUTS</span></span>

### <span data-ttu-id="5af23-119">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5af23-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="5af23-120">筆記</span><span class="sxs-lookup"><span data-stu-id="5af23-120">NOTES</span></span>

## <span data-ttu-id="5af23-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="5af23-121">RELATED LINKS</span></span>

[<span data-ttu-id="5af23-122">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5af23-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5af23-123">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5af23-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="5af23-124">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5af23-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5af23-125">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="5af23-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
