---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901998"
---
# <span data-ttu-id="f4efe-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="f4efe-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="f4efe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4efe-102">SYNOPSIS</span></span>
<span data-ttu-id="f4efe-103">新增 ExpressRoute 回路授權。</span><span class="sxs-lookup"><span data-stu-id="f4efe-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="f4efe-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4efe-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4efe-105">描述</span><span class="sxs-lookup"><span data-stu-id="f4efe-105">DESCRIPTION</span></span>
<span data-ttu-id="f4efe-106">**Add-AzExpressRouteRouteCircuitAuthorization** Cmdlet 會新增 ExpressRoute 回路的授權。</span><span class="sxs-lookup"><span data-stu-id="f4efe-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="f4efe-107">ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="f4efe-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="f4efe-108">ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用該金鑰將其網路連接至回路， (每個虛擬網路) 。</span><span class="sxs-lookup"><span data-stu-id="f4efe-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="f4efe-109">**Add-AzExpressRouteCircteCircuitAuthorization** 會為回路新增新的授權，並同時產生對應的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="f4efe-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="f4efe-110">您隨時都可以執行 Get-AzExpressRouteCircuitAuthorization Cmdlet 來查看這些金鑰，然後視需要複製並轉寄到適當的網路擁有者。</span><span class="sxs-lookup"><span data-stu-id="f4efe-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="f4efe-111">請注意，執行 **Add-AzExpressRouteRouteCircuitAuthorization** 之後，您必須撥打 Set-AzExpressRouteCircuit Cmdlet 以啟用金鑰。</span><span class="sxs-lookup"><span data-stu-id="f4efe-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="f4efe-112">如果您未撥打 **Set-AzExpressRouteCircuit，** 則授權會新增到回路中，但無法啟用。</span><span class="sxs-lookup"><span data-stu-id="f4efe-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="f4efe-113">例子</span><span class="sxs-lookup"><span data-stu-id="f4efe-113">EXAMPLES</span></span>

### <span data-ttu-id="f4efe-114">範例 1：新增授權至指定的 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="f4efe-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="f4efe-115">此範例中的命令會新增授權至現有的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="f4efe-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="f4efe-116">第一個命令使用 **Get-AzExpressRouteCircuit** 來建立名為 ContosoCircuit 之回路的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f4efe-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="f4efe-117">該物件參照會儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f4efe-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="f4efe-118">第二個命令是使用 **Add-AzExpressRouteRouteCircuitAuthorization** Cmdlet 在 ExpressRoute 回路中 (ContosoCircuitAuthorization) 新授權。</span><span class="sxs-lookup"><span data-stu-id="f4efe-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="f4efe-119">此命令會新增授權，但無法啟用該授權。</span><span class="sxs-lookup"><span data-stu-id="f4efe-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="f4efe-120">啟用授權需要範例最後一個命令中顯示的 **Set-AzExpressRouteCircuit。**</span><span class="sxs-lookup"><span data-stu-id="f4efe-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="f4efe-121">參數</span><span class="sxs-lookup"><span data-stu-id="f4efe-121">PARAMETERS</span></span>

### <span data-ttu-id="f4efe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4efe-122">-DefaultProfile</span></span>
<span data-ttu-id="f4efe-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4efe-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4efe-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f4efe-125">指定此 Cmdlet 新增授權的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="f4efe-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="f4efe-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4efe-126">-Name</span></span>
<span data-ttu-id="f4efe-127">指定要新增的回路授權名稱。</span><span class="sxs-lookup"><span data-stu-id="f4efe-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4efe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4efe-128">CommonParameters</span></span>
<span data-ttu-id="f4efe-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4efe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4efe-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f4efe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4efe-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f4efe-131">INPUTS</span></span>

### <span data-ttu-id="f4efe-132">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4efe-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f4efe-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f4efe-133">OUTPUTS</span></span>

### <span data-ttu-id="f4efe-134">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4efe-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f4efe-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f4efe-135">NOTES</span></span>

## <span data-ttu-id="f4efe-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4efe-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4efe-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4efe-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f4efe-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="f4efe-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="f4efe-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="f4efe-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="f4efe-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="f4efe-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="f4efe-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4efe-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
