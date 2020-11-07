---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: ce3d4e42c6644cd3181ec9389a7b571c7f6ca51a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794424"
---
# <span data-ttu-id="1f500-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="1f500-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1f500-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f500-102">SYNOPSIS</span></span>
<span data-ttu-id="1f500-103">取得清單 ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="1f500-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="1f500-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f500-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f500-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f500-105">DESCRIPTION</span></span>
<span data-ttu-id="1f500-106">**AzExpressRouteServiceProvider** Cmdlet 會檢索 list ExpressRoute 服務提供者及其屬性。</span><span class="sxs-lookup"><span data-stu-id="1f500-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="1f500-107">[屬性] 包含位置和頻寬選項。</span><span class="sxs-lookup"><span data-stu-id="1f500-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="1f500-108">示例</span><span class="sxs-lookup"><span data-stu-id="1f500-108">EXAMPLES</span></span>

### <span data-ttu-id="1f500-109">範例1：取得服務提供者清單，其中包含「矽谷」的位置</span><span class="sxs-lookup"><span data-stu-id="1f500-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="1f500-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f500-110">PARAMETERS</span></span>

### <span data-ttu-id="1f500-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f500-111">-DefaultProfile</span></span>
<span data-ttu-id="1f500-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f500-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f500-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f500-113">CommonParameters</span></span>
<span data-ttu-id="1f500-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f500-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f500-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f500-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f500-116">輸入</span><span class="sxs-lookup"><span data-stu-id="1f500-116">INPUTS</span></span>

## <span data-ttu-id="1f500-117">輸出</span><span class="sxs-lookup"><span data-stu-id="1f500-117">OUTPUTS</span></span>

### <span data-ttu-id="1f500-118">PSExpressRouteServiceProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f500-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1f500-119">筆記</span><span class="sxs-lookup"><span data-stu-id="1f500-119">NOTES</span></span>

## <span data-ttu-id="1f500-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f500-120">RELATED LINKS</span></span>

[<span data-ttu-id="1f500-121">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1f500-121">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1f500-122">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f500-122">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1f500-123">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1f500-123">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="1f500-124">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="1f500-124">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
