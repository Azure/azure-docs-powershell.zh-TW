---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 43bf5a0a551840d03ac19e9ea78b26135dde5493
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794440"
---
# <span data-ttu-id="97149-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="97149-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="97149-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97149-102">SYNOPSIS</span></span>
<span data-ttu-id="97149-103">從 ExpressRoute 回路取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="97149-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="97149-104">句法</span><span class="sxs-lookup"><span data-stu-id="97149-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97149-105">說明</span><span class="sxs-lookup"><span data-stu-id="97149-105">DESCRIPTION</span></span>
<span data-ttu-id="97149-106">**AzExpressRouteCircuitARPTable** Cmdlet 會從 ExpressRoute 回路的兩個介面中檢索 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="97149-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="97149-107">ARP 表格提供特定對等的 IPv4 位址到 MAC 位址的對應。</span><span class="sxs-lookup"><span data-stu-id="97149-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="97149-108">您可以使用 ARP 資料表來驗證第2層設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="97149-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="97149-109">示例</span><span class="sxs-lookup"><span data-stu-id="97149-109">EXAMPLES</span></span>

### <span data-ttu-id="97149-110">範例1：顯示 ExpressRoute 對等的 ARP 資料表</span><span class="sxs-lookup"><span data-stu-id="97149-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="97149-111">參數</span><span class="sxs-lookup"><span data-stu-id="97149-111">PARAMETERS</span></span>

### <span data-ttu-id="97149-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97149-112">-DefaultProfile</span></span>
<span data-ttu-id="97149-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97149-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97149-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="97149-114">-DevicePath</span></span>
<span data-ttu-id="97149-115">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="97149-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="97149-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="97149-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="97149-117">所檢查的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="97149-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="97149-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="97149-118">-PeeringType</span></span>
<span data-ttu-id="97149-119">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="97149-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="97149-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97149-120">-ResourceGroupName</span></span>
<span data-ttu-id="97149-121">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97149-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="97149-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97149-122">CommonParameters</span></span>
<span data-ttu-id="97149-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97149-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97149-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97149-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97149-125">輸入</span><span class="sxs-lookup"><span data-stu-id="97149-125">INPUTS</span></span>

## <span data-ttu-id="97149-126">輸出</span><span class="sxs-lookup"><span data-stu-id="97149-126">OUTPUTS</span></span>

### <span data-ttu-id="97149-127">PSExpressRouteCircuitArpTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97149-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="97149-128">筆記</span><span class="sxs-lookup"><span data-stu-id="97149-128">NOTES</span></span>

## <span data-ttu-id="97149-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="97149-129">RELATED LINKS</span></span>

[<span data-ttu-id="97149-130">AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="97149-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="97149-131">AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="97149-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="97149-132">AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="97149-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
