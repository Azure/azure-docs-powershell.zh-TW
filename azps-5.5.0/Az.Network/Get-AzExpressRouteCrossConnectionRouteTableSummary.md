---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132603"
---
# <span data-ttu-id="a06a9-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a06a9-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="a06a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a06a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a06a9-103">取得 ExpressRoute 交叉連線的路由資料表摘要。</span><span class="sxs-lookup"><span data-stu-id="a06a9-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="a06a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a06a9-104">SYNTAX</span></span>

### <span data-ttu-id="a06a9-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="a06a9-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a06a9-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="a06a9-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a06a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="a06a9-107">DESCRIPTION</span></span>
<span data-ttu-id="a06a9-108">AzExpressRouteCrossConnectionRouteTableSummary Cmdlet 會針對特定路由內容， **取得** BGP 鄰居資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="a06a9-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="a06a9-109">此資訊對判斷路由內容已建立的時間，以及對等路由器宣告的路由首碼數量很有用。</span><span class="sxs-lookup"><span data-stu-id="a06a9-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="a06a9-110">示例</span><span class="sxs-lookup"><span data-stu-id="a06a9-110">EXAMPLES</span></span>

### <span data-ttu-id="a06a9-111">範例1：顯示主要路徑的路由摘要</span><span class="sxs-lookup"><span data-stu-id="a06a9-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="a06a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="a06a9-112">PARAMETERS</span></span>

### <span data-ttu-id="a06a9-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="a06a9-113">-CrossConnectionName</span></span>
<span data-ttu-id="a06a9-114">快速路由的名稱交叉連接</span><span class="sxs-lookup"><span data-stu-id="a06a9-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="a06a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06a9-115">-DefaultProfile</span></span>
<span data-ttu-id="a06a9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a06a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a06a9-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a06a9-117">-DevicePath</span></span>
<span data-ttu-id="a06a9-118">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a06a9-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a06a9-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a06a9-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a06a9-120">快速路由的交叉連接</span><span class="sxs-lookup"><span data-stu-id="a06a9-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="a06a9-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a06a9-121">-PeeringType</span></span>
<span data-ttu-id="a06a9-122">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a06a9-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a06a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a06a9-124">包含 ExpressRoute 交叉連線的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a06a9-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="a06a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06a9-125">CommonParameters</span></span>
<span data-ttu-id="a06a9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a06a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06a9-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a06a9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06a9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a06a9-128">INPUTS</span></span>

### <span data-ttu-id="a06a9-129">所有</span><span class="sxs-lookup"><span data-stu-id="a06a9-129">None</span></span>
<span data-ttu-id="a06a9-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a06a9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a06a9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a06a9-131">OUTPUTS</span></span>

### <span data-ttu-id="a06a9-132">PSExpressRouteCrossConnectionRoutesTableSummary 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a06a9-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="a06a9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a06a9-133">NOTES</span></span>

## <span data-ttu-id="a06a9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a06a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="a06a9-135">AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="a06a9-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="a06a9-136">AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a06a9-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
