---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 3230a9e9d8bb70cc80125258cca7d2eaef973e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452459"
---
# <span data-ttu-id="b4fc1-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="b4fc1-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="b4fc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fc1-103">取得 ExpressRoute 回路的使用方式統計資料。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4fc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4fc1-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4fc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fc1-106">**AzureRmExpressRouteCircuitStats** Cmdlet 會為 ExpressRoute 回路檢索流量統計資料。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="b4fc1-107">統計資料包括在主要和次要路由上傳送和接收的位元組數。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="b4fc1-108">示例</span><span class="sxs-lookup"><span data-stu-id="b4fc1-108">EXAMPLES</span></span>

### <span data-ttu-id="b4fc1-109">範例1：顯示 ExpressRoute 對等的流量統計資料</span><span class="sxs-lookup"><span data-stu-id="b4fc1-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="b4fc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="b4fc1-111">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="b4fc1-111">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b4fc1-112">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-112">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="b4fc1-113">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b4fc1-113">-PeeringType</span></span>
<span data-ttu-id="b4fc1-114">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b4fc1-114">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b4fc1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4fc1-115">-ResourceGroupName</span></span>
<span data-ttu-id="b4fc1-116">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-116">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b4fc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fc1-117">-DefaultProfile</span></span>
<span data-ttu-id="b4fc1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4fc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fc1-119">CommonParameters</span></span>
<span data-ttu-id="b4fc1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fc1-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4fc1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fc1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b4fc1-122">INPUTS</span></span>

## <span data-ttu-id="b4fc1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b4fc1-123">OUTPUTS</span></span>

### <span data-ttu-id="b4fc1-124">PSExpressRouteCircuitStats 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b4fc1-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="b4fc1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b4fc1-125">NOTES</span></span>

## <span data-ttu-id="b4fc1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4fc1-126">RELATED LINKS</span></span>

[<span data-ttu-id="b4fc1-127">AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b4fc1-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b4fc1-128">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4fc1-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b4fc1-129">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b4fc1-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
