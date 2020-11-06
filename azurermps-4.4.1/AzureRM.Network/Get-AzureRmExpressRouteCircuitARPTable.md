---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e306faae861b8f35bff3695dc4235394764621a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446741"
---
# <span data-ttu-id="262a5-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="262a5-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="262a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="262a5-102">SYNOPSIS</span></span>
<span data-ttu-id="262a5-103">從 ExpressRoute 回路取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="262a5-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="262a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="262a5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="262a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="262a5-105">DESCRIPTION</span></span>
<span data-ttu-id="262a5-106">**AzureRmExpressRouteCircuitARPTable** Cmdlet 會從 ExpressRoute 回路的兩個介面中檢索 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="262a5-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="262a5-107">ARP 表格提供特定對等的 IPv4 位址到 MAC 位址的對應。</span><span class="sxs-lookup"><span data-stu-id="262a5-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="262a5-108">您可以使用 ARP 資料表來驗證第2層設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="262a5-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="262a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="262a5-109">EXAMPLES</span></span>

### <span data-ttu-id="262a5-110">範例1：顯示 ExpressRoute 對等的 ARP 資料表</span><span class="sxs-lookup"><span data-stu-id="262a5-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="262a5-111">參數</span><span class="sxs-lookup"><span data-stu-id="262a5-111">PARAMETERS</span></span>

### <span data-ttu-id="262a5-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="262a5-112">-DevicePath</span></span>
<span data-ttu-id="262a5-113">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="262a5-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="262a5-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="262a5-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="262a5-115">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="262a5-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="262a5-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="262a5-116">-PeeringType</span></span>
<span data-ttu-id="262a5-117">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="262a5-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="262a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="262a5-119">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="262a5-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="262a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262a5-120">-DefaultProfile</span></span>
<span data-ttu-id="262a5-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="262a5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262a5-122">CommonParameters</span></span>
<span data-ttu-id="262a5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="262a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262a5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="262a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262a5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="262a5-125">INPUTS</span></span>

## <span data-ttu-id="262a5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="262a5-126">OUTPUTS</span></span>

### <span data-ttu-id="262a5-127">PSExpressRouteCircuitArpTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="262a5-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="262a5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="262a5-128">NOTES</span></span>

## <span data-ttu-id="262a5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="262a5-129">RELATED LINKS</span></span>

[<span data-ttu-id="262a5-130">AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="262a5-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="262a5-131">AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="262a5-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="262a5-132">AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="262a5-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
