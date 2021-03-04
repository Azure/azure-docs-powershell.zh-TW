---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2adb971d2e44f844fe52bb83a9ce834bbebe1897
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913457"
---
# <span data-ttu-id="37697-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="37697-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="37697-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37697-102">SYNOPSIS</span></span>
<span data-ttu-id="37697-103">移除現有的 ExpressRoute 組組授權。</span><span class="sxs-lookup"><span data-stu-id="37697-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="37697-104">語法</span><span class="sxs-lookup"><span data-stu-id="37697-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37697-105">描述</span><span class="sxs-lookup"><span data-stu-id="37697-105">DESCRIPTION</span></span>
<span data-ttu-id="37697-106">**Remove-AzExpressRouteRouteCircuitAuthorization** Cmdlet 會移除指派給 ExpressRoute 回路的授權。</span><span class="sxs-lookup"><span data-stu-id="37697-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="37697-107">ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Azure。</span><span class="sxs-lookup"><span data-stu-id="37697-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="37697-108">ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，由虛擬網路擁有者用來將其網路連接至回路。</span><span class="sxs-lookup"><span data-stu-id="37697-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="37697-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="37697-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="37697-110">不過，回路擁有者隨時都可以使用 **Remove-AzExpressRouteCircuitAuthorization** 來移除指派給虛擬網路的授權。</span><span class="sxs-lookup"><span data-stu-id="37697-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="37697-111">發生這種情況時，對應的虛擬網路無法再使用 ExpressRoute 回路連接到 Azure。</span><span class="sxs-lookup"><span data-stu-id="37697-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="37697-112">例子</span><span class="sxs-lookup"><span data-stu-id="37697-112">EXAMPLES</span></span>

### <span data-ttu-id="37697-113">範例 1：從 ExpressRoute 回路移除回路授權</span><span class="sxs-lookup"><span data-stu-id="37697-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="37697-114">此範例會從 ExpressRoute 回路移除回路授權。</span><span class="sxs-lookup"><span data-stu-id="37697-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="37697-115">第一個命令使用 **Get-AzExpressRouteCircuit** Cmdlet 來建立名為 ContosoCircuit 的 ExpressRoute 回路物件參照，並儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="37697-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="37697-116">第二個命令會標記要移除的回路授權 ContosoCircuitAuthorization。</span><span class="sxs-lookup"><span data-stu-id="37697-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="37697-117">第三個命令使用 Set-AzExpressRouteCircuit Cmdlet 以確認移除儲存在 $Circuit 變數中的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="37697-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="37697-118">參數</span><span class="sxs-lookup"><span data-stu-id="37697-118">PARAMETERS</span></span>

### <span data-ttu-id="37697-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37697-119">-DefaultProfile</span></span>
<span data-ttu-id="37697-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37697-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37697-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37697-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="37697-122">指定此 Cmdlet 移除的 ExpressRouteCircuit 物件。</span><span class="sxs-lookup"><span data-stu-id="37697-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37697-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="37697-123">-Name</span></span>
<span data-ttu-id="37697-124">指定此 Cmdlet 移除的回路授權名稱。</span><span class="sxs-lookup"><span data-stu-id="37697-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37697-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37697-125">CommonParameters</span></span>
<span data-ttu-id="37697-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37697-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37697-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37697-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37697-128">輸入</span><span class="sxs-lookup"><span data-stu-id="37697-128">INPUTS</span></span>

### <span data-ttu-id="37697-129">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37697-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="37697-130">輸出</span><span class="sxs-lookup"><span data-stu-id="37697-130">OUTPUTS</span></span>

### <span data-ttu-id="37697-131">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37697-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="37697-132">筆記</span><span class="sxs-lookup"><span data-stu-id="37697-132">NOTES</span></span>

## <span data-ttu-id="37697-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="37697-133">RELATED LINKS</span></span>

[<span data-ttu-id="37697-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="37697-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="37697-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37697-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="37697-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="37697-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="37697-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="37697-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="37697-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37697-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
