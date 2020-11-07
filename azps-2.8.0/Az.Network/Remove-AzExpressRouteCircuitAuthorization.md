---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 62cfc4fc3555b9eb798a1d64c53b0b25e9abc14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790677"
---
# <span data-ttu-id="e5456-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e5456-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e5456-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5456-102">SYNOPSIS</span></span>
<span data-ttu-id="e5456-103">移除現有的 ExpressRoute 配置授權。</span><span class="sxs-lookup"><span data-stu-id="e5456-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="e5456-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5456-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5456-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5456-105">DESCRIPTION</span></span>
<span data-ttu-id="e5456-106">**AzExpressRouteCircuitAuthorization** Cmdlet 會移除指派給 ExpressRoute 回路的授權。</span><span class="sxs-lookup"><span data-stu-id="e5456-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="e5456-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="e5456-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e5456-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至線路。</span><span class="sxs-lookup"><span data-stu-id="e5456-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="e5456-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="e5456-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="e5456-110">不過，線路擁有者可以隨時使用 **移除 AzExpressRouteCircuitAuthorization** 來移除指派給虛擬網路的授權。</span><span class="sxs-lookup"><span data-stu-id="e5456-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="e5456-111">在這種情況下，對應的虛擬網路將無法再使用 ExpressRoute 線路連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="e5456-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="e5456-112">示例</span><span class="sxs-lookup"><span data-stu-id="e5456-112">EXAMPLES</span></span>

### <span data-ttu-id="e5456-113">範例1：從 ExpressRoute 回路移除線路授權</span><span class="sxs-lookup"><span data-stu-id="e5456-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="e5456-114">這個範例會從 ExpressRoute 回路中移除線路授權。</span><span class="sxs-lookup"><span data-stu-id="e5456-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="e5456-115">第一個命令使用 **AzExpressRouteCircuit** Cmdlet 來建立名為 ContosoCircuit 的 ExpressRoute 回路的物件參照，並將結果儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e5456-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="e5456-116">第二個命令會標示要移除的線路授權 ContosoCircuitAuthorization。</span><span class="sxs-lookup"><span data-stu-id="e5456-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="e5456-117">第三個命令使用 Set-AzExpressRouteCircuit Cmdlet 來確認移除儲存在 $Circuit 變數中的 ExpressRoute 電路。</span><span class="sxs-lookup"><span data-stu-id="e5456-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="e5456-118">參數</span><span class="sxs-lookup"><span data-stu-id="e5456-118">PARAMETERS</span></span>

### <span data-ttu-id="e5456-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5456-119">-DefaultProfile</span></span>
<span data-ttu-id="e5456-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5456-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5456-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5456-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e5456-122">指定此 Cmdlet 移除的 ExpressRouteCircuit 物件。</span><span class="sxs-lookup"><span data-stu-id="e5456-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5456-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5456-123">-Name</span></span>
<span data-ttu-id="e5456-124">指定此 Cmdlet 移除之線路授權的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5456-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5456-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5456-125">CommonParameters</span></span>
<span data-ttu-id="e5456-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5456-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5456-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5456-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5456-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e5456-128">INPUTS</span></span>

### <span data-ttu-id="e5456-129">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5456-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e5456-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e5456-130">OUTPUTS</span></span>

### <span data-ttu-id="e5456-131">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5456-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e5456-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e5456-132">NOTES</span></span>

## <span data-ttu-id="e5456-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5456-133">RELATED LINKS</span></span>

[<span data-ttu-id="e5456-134">附加 AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e5456-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e5456-135">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5456-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5456-136">AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e5456-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e5456-137">新-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e5456-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e5456-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5456-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
