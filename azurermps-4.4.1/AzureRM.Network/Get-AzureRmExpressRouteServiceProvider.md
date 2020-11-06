---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: b321e55160d3a88c04e3a0587efb845c70028a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448140"
---
# <span data-ttu-id="59bd2-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="59bd2-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="59bd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="59bd2-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="59bd2-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="59bd2-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59bd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="59bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="59bd2-106">**AzureRmExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="59bd2-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="59bd2-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="59bd2-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="59bd2-108">示例</span><span class="sxs-lookup"><span data-stu-id="59bd2-108">EXAMPLES</span></span>

### <span data-ttu-id="59bd2-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="59bd2-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="59bd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="59bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="59bd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bd2-111">-DefaultProfile</span></span>
<span data-ttu-id="59bd2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59bd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59bd2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bd2-113">CommonParameters</span></span>
<span data-ttu-id="59bd2-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59bd2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bd2-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59bd2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bd2-116">輸入</span><span class="sxs-lookup"><span data-stu-id="59bd2-116">INPUTS</span></span>

## <span data-ttu-id="59bd2-117">輸出</span><span class="sxs-lookup"><span data-stu-id="59bd2-117">OUTPUTS</span></span>

### <span data-ttu-id="59bd2-118">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59bd2-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="59bd2-119">筆記</span><span class="sxs-lookup"><span data-stu-id="59bd2-119">NOTES</span></span>

## <span data-ttu-id="59bd2-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="59bd2-120">RELATED LINKS</span></span>

[<span data-ttu-id="59bd2-121">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="59bd2-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="59bd2-122">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="59bd2-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="59bd2-123">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59bd2-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="59bd2-124">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="59bd2-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
