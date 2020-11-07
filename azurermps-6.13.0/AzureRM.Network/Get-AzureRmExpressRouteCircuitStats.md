---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: d9978c50186b520d8e956dc20581d1ceb615b673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626071"
---
# <span data-ttu-id="1dc94-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="1dc94-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="1dc94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dc94-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc94-103">取得 ExpressRoute 回路的使用方式統計資料。</span><span class="sxs-lookup"><span data-stu-id="1dc94-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc94-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dc94-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc94-105">說明</span><span class="sxs-lookup"><span data-stu-id="1dc94-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc94-106">**AzureRmExpressRouteCircuitStats** Cmdlet 會為 ExpressRoute 回路檢索流量統計資料。</span><span class="sxs-lookup"><span data-stu-id="1dc94-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="1dc94-107">統計資料包括在主要和次要路由上傳送和接收的位元組數。</span><span class="sxs-lookup"><span data-stu-id="1dc94-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="1dc94-108">示例</span><span class="sxs-lookup"><span data-stu-id="1dc94-108">EXAMPLES</span></span>

### <span data-ttu-id="1dc94-109">範例1：顯示 ExpressRoute 對等的流量統計資料</span><span class="sxs-lookup"><span data-stu-id="1dc94-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="1dc94-110">參數</span><span class="sxs-lookup"><span data-stu-id="1dc94-110">PARAMETERS</span></span>

### <span data-ttu-id="1dc94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc94-111">-DefaultProfile</span></span>
<span data-ttu-id="1dc94-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dc94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc94-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="1dc94-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="1dc94-114">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc94-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="1dc94-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1dc94-115">-PeeringType</span></span>
<span data-ttu-id="1dc94-116">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1dc94-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1dc94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc94-117">-ResourceGroupName</span></span>
<span data-ttu-id="1dc94-118">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc94-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="1dc94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc94-119">CommonParameters</span></span>
<span data-ttu-id="1dc94-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dc94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc94-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dc94-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc94-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc94-122">INPUTS</span></span>

### <span data-ttu-id="1dc94-123">System.object</span><span class="sxs-lookup"><span data-stu-id="1dc94-123">System.String</span></span>

## <span data-ttu-id="1dc94-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc94-124">OUTPUTS</span></span>

### <span data-ttu-id="1dc94-125">PSExpressRouteCircuitStats 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dc94-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="1dc94-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc94-126">NOTES</span></span>

## <span data-ttu-id="1dc94-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc94-127">RELATED LINKS</span></span>

[<span data-ttu-id="1dc94-128">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1dc94-128">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1dc94-129">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1dc94-129">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1dc94-130">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1dc94-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
