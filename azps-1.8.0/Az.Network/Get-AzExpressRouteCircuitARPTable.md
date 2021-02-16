---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 04c4355caaa76776a96e2619a0080b9c32d8e98a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402077"
---
# <span data-ttu-id="e1904-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e1904-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="e1904-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1904-102">SYNOPSIS</span></span>
<span data-ttu-id="e1904-103">從 ExpressRoute 回路中獲得 ARP 表格。</span><span class="sxs-lookup"><span data-stu-id="e1904-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e1904-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1904-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1904-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1904-105">DESCRIPTION</span></span>
<span data-ttu-id="e1904-106">**Get-AzExpressRouteRouteCircuitARPTable** Cmdlet 會從 ExpressRoute 回路的兩個介面中，取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="e1904-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="e1904-107">ARP 資料表提供特定對等的 IPv4 位址與 MAC 位址的映射。</span><span class="sxs-lookup"><span data-stu-id="e1904-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="e1904-108">您可以使用 ARP 資料表驗證第 2 層組配置和連接。</span><span class="sxs-lookup"><span data-stu-id="e1904-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="e1904-109">例子</span><span class="sxs-lookup"><span data-stu-id="e1904-109">EXAMPLES</span></span>

### <span data-ttu-id="e1904-110">範例 1：顯示 ExpressRoute 對等的 ARP 表格</span><span class="sxs-lookup"><span data-stu-id="e1904-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="e1904-111">參數</span><span class="sxs-lookup"><span data-stu-id="e1904-111">PARAMETERS</span></span>

### <span data-ttu-id="e1904-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1904-112">-DefaultProfile</span></span>
<span data-ttu-id="e1904-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1904-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1904-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="e1904-114">-DevicePath</span></span>
<span data-ttu-id="e1904-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="e1904-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1904-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="e1904-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="e1904-117">要檢查的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="e1904-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="e1904-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e1904-118">-PeeringType</span></span>
<span data-ttu-id="e1904-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e1904-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1904-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1904-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1904-121">包含 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e1904-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e1904-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1904-122">CommonParameters</span></span>
<span data-ttu-id="e1904-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1904-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1904-124">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1904-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1904-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e1904-125">INPUTS</span></span>

### <span data-ttu-id="e1904-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e1904-126">System.String</span></span>

## <span data-ttu-id="e1904-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e1904-127">OUTPUTS</span></span>

### <span data-ttu-id="e1904-128">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="e1904-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="e1904-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e1904-129">NOTES</span></span>

## <span data-ttu-id="e1904-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1904-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1904-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1904-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e1904-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e1904-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="e1904-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="e1904-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
