---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0ef2870592411ce64847f8a4a58dabdebcc8235f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414708"
---
# <span data-ttu-id="4ec65-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ec65-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="4ec65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ec65-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec65-103">獲得與 ExpressRouteCircuit 的專用對等關聯的 ExpressRoute 回路連接組。</span><span class="sxs-lookup"><span data-stu-id="4ec65-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="4ec65-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ec65-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec65-105">描述</span><span class="sxs-lookup"><span data-stu-id="4ec65-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec65-106">**Get-AzExpressRouteRouteCircuitConnectionConfig** Cmdlet 會針對 ExpressRoute 回路，取得與私人對等關聯的回路連接組式。</span><span class="sxs-lookup"><span data-stu-id="4ec65-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4ec65-107">例子</span><span class="sxs-lookup"><span data-stu-id="4ec65-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec65-108">範例 1：顯示 ExpressRoute 回路的回路連接組</span><span class="sxs-lookup"><span data-stu-id="4ec65-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="4ec65-109">範例 2：使用管道取得與 ExpressRoute 回路相關聯的回路連接資源</span><span class="sxs-lookup"><span data-stu-id="4ec65-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="4ec65-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ec65-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec65-111">-DefaultProfile</span></span>
<span data-ttu-id="4ec65-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ec65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec65-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ec65-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4ec65-114">包含回路連接配置的 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="4ec65-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec65-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ec65-115">-Name</span></span>
<span data-ttu-id="4ec65-116">要取回的回路連接組名。</span><span class="sxs-lookup"><span data-stu-id="4ec65-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec65-117">CommonParameters</span></span>
<span data-ttu-id="4ec65-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ec65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec65-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ec65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec65-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4ec65-120">INPUTS</span></span>

### <span data-ttu-id="4ec65-121">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ec65-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4ec65-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4ec65-122">OUTPUTS</span></span>

### <span data-ttu-id="4ec65-123">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="4ec65-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="4ec65-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4ec65-124">NOTES</span></span>

## <span data-ttu-id="4ec65-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ec65-125">RELATED LINKS</span></span>

[<span data-ttu-id="4ec65-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ec65-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4ec65-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ec65-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4ec65-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ec65-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4ec65-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ec65-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)


