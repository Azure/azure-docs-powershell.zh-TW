---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: f990e2bb408fc9bb76c992d7de3e01b5eb88311b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448632"
---
# <span data-ttu-id="acd52-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="acd52-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="acd52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acd52-102">SYNOPSIS</span></span>
<span data-ttu-id="acd52-103">移除現有的 ExpressRoute 配置授權。</span><span class="sxs-lookup"><span data-stu-id="acd52-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acd52-104">句法</span><span class="sxs-lookup"><span data-stu-id="acd52-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd52-105">說明</span><span class="sxs-lookup"><span data-stu-id="acd52-105">DESCRIPTION</span></span>
<span data-ttu-id="acd52-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet 會移除指派給 ExpressRoute 回路的授權。</span><span class="sxs-lookup"><span data-stu-id="acd52-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="acd52-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="acd52-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="acd52-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至線路。</span><span class="sxs-lookup"><span data-stu-id="acd52-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="acd52-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="acd52-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="acd52-110">不過，線路擁有者可以隨時使用 **移除 AzureRmExpressRouteCircuitAuthorization** 來移除指派給虛擬網路的授權。</span><span class="sxs-lookup"><span data-stu-id="acd52-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="acd52-111">在這種情況下，對應的虛擬網路將無法再使用 ExpressRoute 線路連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="acd52-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="acd52-112">示例</span><span class="sxs-lookup"><span data-stu-id="acd52-112">EXAMPLES</span></span>

### <span data-ttu-id="acd52-113">範例1：從 ExpressRoute 回路移除線路授權</span><span class="sxs-lookup"><span data-stu-id="acd52-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="acd52-114">這個範例會從 ExpressRoute 回路中移除線路授權。</span><span class="sxs-lookup"><span data-stu-id="acd52-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="acd52-115">第一個命令使用 **AzureRmExpressRouteCircuit** Cmdlet 來建立名為 ContosoCircuit 的 ExpressRoute 回路的物件參照，並將結果儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="acd52-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="acd52-116">第二個命令會標示要移除的線路授權 ContosoCircuitAuthorization。</span><span class="sxs-lookup"><span data-stu-id="acd52-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="acd52-117">第三個命令使用 Set-AzureRmExpressRouteCircuit Cmdlet 來確認移除儲存在 $Circuit 變數中的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="acd52-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="acd52-118">參數</span><span class="sxs-lookup"><span data-stu-id="acd52-118">PARAMETERS</span></span>

### <span data-ttu-id="acd52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd52-119">-DefaultProfile</span></span>
<span data-ttu-id="acd52-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acd52-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acd52-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acd52-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="acd52-122">指定此 Cmdlet 移除的 ExpressRouteCircuit 物件。</span><span class="sxs-lookup"><span data-stu-id="acd52-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acd52-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="acd52-123">-Name</span></span>
<span data-ttu-id="acd52-124">指定此 Cmdlet 移除之線路授權的名稱。</span><span class="sxs-lookup"><span data-stu-id="acd52-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd52-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd52-125">CommonParameters</span></span>
<span data-ttu-id="acd52-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acd52-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd52-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acd52-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd52-128">輸入</span><span class="sxs-lookup"><span data-stu-id="acd52-128">INPUTS</span></span>

### <span data-ttu-id="acd52-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acd52-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="acd52-130">這個 Cmdlet 會接受 PSExpressRouteCircuit 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** 物件）。</span><span class="sxs-lookup"><span data-stu-id="acd52-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="acd52-131">輸出</span><span class="sxs-lookup"><span data-stu-id="acd52-131">OUTPUTS</span></span>

### <span data-ttu-id="acd52-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acd52-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="acd52-133">這個 Cmdlet 會修改 PSExpressRouteCircuit 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** 物件）。</span><span class="sxs-lookup"><span data-stu-id="acd52-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="acd52-134">筆記</span><span class="sxs-lookup"><span data-stu-id="acd52-134">NOTES</span></span>

## <span data-ttu-id="acd52-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="acd52-135">RELATED LINKS</span></span>

[<span data-ttu-id="acd52-136">附加 AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="acd52-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="acd52-137">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acd52-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="acd52-138">AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="acd52-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="acd52-139">新-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="acd52-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="acd52-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acd52-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
