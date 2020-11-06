---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456019"
---
# <span data-ttu-id="15d8c-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="15d8c-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="15d8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="15d8c-103">取得與 ExpressRouteCircuit 的私有對等相關聯的 ExpressRoute 線路連線設定。</span><span class="sxs-lookup"><span data-stu-id="15d8c-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="15d8c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="15d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="15d8c-106">AzureRmExpressRouteCircuitConnectionConfig Cmdlet 會為與 ExpressRoute 回路的私人對等相關聯的線路連線 **取得** 配置。</span><span class="sxs-lookup"><span data-stu-id="15d8c-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="15d8c-107">示例</span><span class="sxs-lookup"><span data-stu-id="15d8c-107">EXAMPLES</span></span>

### <span data-ttu-id="15d8c-108">範例1：顯示 ExpressRoute 線路的線路連線設定</span><span class="sxs-lookup"><span data-stu-id="15d8c-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="15d8c-109">範例2：使用管道取得與 ExpressRoute 電路相關聯的線路連線資源</span><span class="sxs-lookup"><span data-stu-id="15d8c-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="15d8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="15d8c-110">PARAMETERS</span></span>

### <span data-ttu-id="15d8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d8c-111">-DefaultProfile</span></span>
<span data-ttu-id="15d8c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15d8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d8c-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15d8c-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="15d8c-114">包含線路連接設定的 ExpressRoute 電路物件。</span><span class="sxs-lookup"><span data-stu-id="15d8c-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="15d8c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="15d8c-115">-Name</span></span>
<span data-ttu-id="15d8c-116">要檢索之線路連接設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="15d8c-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d8c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d8c-117">CommonParameters</span></span>
<span data-ttu-id="15d8c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15d8c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d8c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15d8c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d8c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="15d8c-120">INPUTS</span></span>

### <span data-ttu-id="15d8c-121">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15d8c-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="15d8c-122">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="15d8c-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="15d8c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="15d8c-123">OUTPUTS</span></span>

### <span data-ttu-id="15d8c-124">PSExpressRouteCircuitConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15d8c-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="15d8c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="15d8c-125">NOTES</span></span>

## <span data-ttu-id="15d8c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="15d8c-126">RELATED LINKS</span></span>

[<span data-ttu-id="15d8c-127">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15d8c-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15d8c-128">附加 AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="15d8c-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="15d8c-129">移除-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="15d8c-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="15d8c-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="15d8c-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="15d8c-131">新-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="15d8c-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
