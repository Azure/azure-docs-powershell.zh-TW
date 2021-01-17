---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435226"
---
# <span data-ttu-id="c1e78-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1e78-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c1e78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1e78-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e78-103">取得與 ExpressRouteCircuit 的私有對等相關聯的 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="c1e78-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="c1e78-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1e78-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1e78-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1e78-105">DESCRIPTION</span></span>
<span data-ttu-id="c1e78-106">AzExpressRouteCircuitConnectionConfig Cmdlet 會為與 ExpressRoute 回路的私人對等相關聯的線路連線 **取得** 配置。</span><span class="sxs-lookup"><span data-stu-id="c1e78-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c1e78-107">示例</span><span class="sxs-lookup"><span data-stu-id="c1e78-107">EXAMPLES</span></span>

### <span data-ttu-id="c1e78-108">範例1：顯示 ExpressRoute 線路的線路連線設定</span><span class="sxs-lookup"><span data-stu-id="c1e78-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c1e78-109">範例2：使用管道取得與 ExpressRoute 電路相關聯的線路連線資源</span><span class="sxs-lookup"><span data-stu-id="c1e78-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="c1e78-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1e78-110">PARAMETERS</span></span>

### <span data-ttu-id="c1e78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e78-111">-DefaultProfile</span></span>
<span data-ttu-id="c1e78-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1e78-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e78-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1e78-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c1e78-114">包含線路連接設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="c1e78-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="c1e78-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1e78-115">-Name</span></span>
<span data-ttu-id="c1e78-116">要檢索之線路連接設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1e78-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="c1e78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e78-117">CommonParameters</span></span>
<span data-ttu-id="c1e78-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1e78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e78-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c1e78-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e78-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c1e78-120">INPUTS</span></span>

### <span data-ttu-id="c1e78-121">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c1e78-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c1e78-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c1e78-122">OUTPUTS</span></span>

### <span data-ttu-id="c1e78-123">PSExpressRouteCircuitConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c1e78-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="c1e78-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c1e78-124">NOTES</span></span>

## <span data-ttu-id="c1e78-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1e78-125">RELATED LINKS</span></span>

[<span data-ttu-id="c1e78-126">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c1e78-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c1e78-127">附加 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1e78-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1e78-128">移除-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1e78-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1e78-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1e78-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c1e78-130">新-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c1e78-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)