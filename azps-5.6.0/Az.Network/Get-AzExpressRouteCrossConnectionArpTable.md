---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
ms.openlocfilehash: 4e23e96906874d8f19931005919ef088f9bc5ec1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901989"
---
# <span data-ttu-id="ef32f-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ef32f-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="ef32f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef32f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef32f-103">從 ExpressRoute 交叉連接獲得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="ef32f-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ef32f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef32f-104">SYNTAX</span></span>

### <span data-ttu-id="ef32f-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="ef32f-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef32f-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="ef32f-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef32f-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef32f-107">DESCRIPTION</span></span>
<span data-ttu-id="ef32f-108">**Get-AzExpressRouteCrossConnectionARPTable** Cmdlet 會從 ExpressRoute 交互連接的兩個介面中，取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="ef32f-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="ef32f-109">ARP 資料表提供特定對等的 IPv4 位址與 MAC 位址的映射。</span><span class="sxs-lookup"><span data-stu-id="ef32f-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="ef32f-110">您可以使用 ARP 資料表驗證第 2 層組配置和連接。</span><span class="sxs-lookup"><span data-stu-id="ef32f-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="ef32f-111">例子</span><span class="sxs-lookup"><span data-stu-id="ef32f-111">EXAMPLES</span></span>

### <span data-ttu-id="ef32f-112">範例 1：顯示 ExpressRoute 對等的 ARP 表格</span><span class="sxs-lookup"><span data-stu-id="ef32f-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="ef32f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef32f-113">PARAMETERS</span></span>

### <span data-ttu-id="ef32f-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="ef32f-114">-CrossConnectionName</span></span>
<span data-ttu-id="ef32f-115">Express Route 交叉連接的名稱</span><span class="sxs-lookup"><span data-stu-id="ef32f-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef32f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef32f-116">-DefaultProfile</span></span>
<span data-ttu-id="ef32f-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef32f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef32f-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ef32f-118">-DevicePath</span></span>
<span data-ttu-id="ef32f-119">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ef32f-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ef32f-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ef32f-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ef32f-121">Express Route 交叉連接</span><span class="sxs-lookup"><span data-stu-id="ef32f-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef32f-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ef32f-122">-PeeringType</span></span>
<span data-ttu-id="ef32f-123">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ef32f-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ef32f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef32f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef32f-125">包含 ExpressRoute 交叉連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ef32f-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef32f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef32f-126">CommonParameters</span></span>
<span data-ttu-id="ef32f-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef32f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef32f-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef32f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef32f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ef32f-129">INPUTS</span></span>

### <span data-ttu-id="ef32f-130">沒有</span><span class="sxs-lookup"><span data-stu-id="ef32f-130">None</span></span>
<span data-ttu-id="ef32f-131">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ef32f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef32f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ef32f-132">OUTPUTS</span></span>

### <span data-ttu-id="ef32f-133">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="ef32f-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="ef32f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ef32f-134">NOTES</span></span>

## <span data-ttu-id="ef32f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef32f-135">RELATED LINKS</span></span>

[<span data-ttu-id="ef32f-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ef32f-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="ef32f-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ef32f-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
