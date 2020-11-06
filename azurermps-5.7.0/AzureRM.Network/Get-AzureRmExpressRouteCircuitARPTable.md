---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e007f220b827db144a4c10b1adb5732e110ddf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449864"
---
# <span data-ttu-id="c6795-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c6795-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="c6795-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6795-102">SYNOPSIS</span></span>
<span data-ttu-id="c6795-103">從 ExpressRoute 回路取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="c6795-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6795-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6795-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6795-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6795-105">DESCRIPTION</span></span>
<span data-ttu-id="c6795-106">**AzureRmExpressRouteCircuitARPTable** Cmdlet 會從 ExpressRoute 回路的兩個介面中檢索 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="c6795-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="c6795-107">ARP 表格提供特定對等的 IPv4 位址到 MAC 位址的對應。</span><span class="sxs-lookup"><span data-stu-id="c6795-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="c6795-108">您可以使用 ARP 資料表來驗證第2層設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="c6795-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="c6795-109">示例</span><span class="sxs-lookup"><span data-stu-id="c6795-109">EXAMPLES</span></span>

### <span data-ttu-id="c6795-110">範例1：顯示 ExpressRoute 對等的 ARP 資料表</span><span class="sxs-lookup"><span data-stu-id="c6795-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="c6795-111">參數</span><span class="sxs-lookup"><span data-stu-id="c6795-111">PARAMETERS</span></span>

### <span data-ttu-id="c6795-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6795-112">-DefaultProfile</span></span>
<span data-ttu-id="c6795-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6795-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6795-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c6795-114">-DevicePath</span></span>
<span data-ttu-id="c6795-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c6795-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6795-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c6795-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c6795-117">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="c6795-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6795-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c6795-118">-PeeringType</span></span>
<span data-ttu-id="c6795-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c6795-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6795-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6795-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6795-121">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6795-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6795-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6795-122">CommonParameters</span></span>
<span data-ttu-id="c6795-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6795-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6795-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6795-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6795-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c6795-125">INPUTS</span></span>

### <span data-ttu-id="c6795-126">所有</span><span class="sxs-lookup"><span data-stu-id="c6795-126">None</span></span>
<span data-ttu-id="c6795-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c6795-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6795-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c6795-128">OUTPUTS</span></span>

### <span data-ttu-id="c6795-129">PSExpressRouteCircuitArpTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6795-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="c6795-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c6795-130">NOTES</span></span>

## <span data-ttu-id="c6795-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6795-131">RELATED LINKS</span></span>

[<span data-ttu-id="c6795-132">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6795-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c6795-133">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c6795-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c6795-134">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c6795-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
