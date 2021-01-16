---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275148"
---
# <span data-ttu-id="a3ee8-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="a3ee8-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="a3ee8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ee8-103">取得 ExpressRoute 回路的使用方式統計資料。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3ee8-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3ee8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ee8-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3ee8-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ee8-106">**AzExpressRouteCircuitStat** Cmdlet 會為 ExpressRoute 回路檢索流量統計資料。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="a3ee8-107">統計資料包括在主要和次要路由上傳送和接收的位元組數。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="a3ee8-108">示例</span><span class="sxs-lookup"><span data-stu-id="a3ee8-108">EXAMPLES</span></span>

### <span data-ttu-id="a3ee8-109">範例1：顯示 ExpressRoute 對等的流量統計資料</span><span class="sxs-lookup"><span data-stu-id="a3ee8-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="a3ee8-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3ee8-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ee8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ee8-111">-DefaultProfile</span></span>
<span data-ttu-id="a3ee8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ee8-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a3ee8-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a3ee8-114">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a3ee8-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a3ee8-115">-PeeringType</span></span>
<span data-ttu-id="a3ee8-116">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a3ee8-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a3ee8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ee8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3ee8-118">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a3ee8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ee8-119">CommonParameters</span></span>
<span data-ttu-id="a3ee8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ee8-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3ee8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ee8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a3ee8-122">INPUTS</span></span>

### <span data-ttu-id="a3ee8-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a3ee8-123">System.String</span></span>

## <span data-ttu-id="a3ee8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a3ee8-124">OUTPUTS</span></span>

### <span data-ttu-id="a3ee8-125">PSExpressRouteCircuitStats 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3ee8-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="a3ee8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a3ee8-126">NOTES</span></span>

## <span data-ttu-id="a3ee8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3ee8-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3ee8-128">AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a3ee8-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a3ee8-129">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3ee8-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a3ee8-130">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a3ee8-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
