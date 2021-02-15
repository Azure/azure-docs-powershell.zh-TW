---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136003"
---
# <span data-ttu-id="08d5b-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="08d5b-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="08d5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="08d5b-103">新增 ExpressRoute 線路驗證。</span><span class="sxs-lookup"><span data-stu-id="08d5b-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="08d5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="08d5b-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08d5b-105">說明</span><span class="sxs-lookup"><span data-stu-id="08d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="08d5b-106">**AzExpressRouteCircuitAuthorization** Cmdlet 會將授權新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="08d5b-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="08d5b-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="08d5b-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="08d5b-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生一個授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至 (每個虛擬網路) 一個授權的線路。</span><span class="sxs-lookup"><span data-stu-id="08d5b-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="08d5b-109">[**載入 AzExpressRouteCircuitAuthorization** ] 會將新的授權新增至電路，同時也會產生對應的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="08d5b-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="08d5b-110">您可以隨時執行 Get-AzExpressRouteCircuitAuthorization Cmdlet 並視需要來查看這些金鑰，然後將其複製並轉寄給適當的網路擁有者。</span><span class="sxs-lookup"><span data-stu-id="08d5b-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="08d5b-111">請注意，執行 **附加 AzExpressRouteCircuitAuthorization** 之後，您必須呼叫 Set-AzExpressRouteCircuit Cmdlet 才能啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="08d5b-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="08d5b-112">如果您不撥打電話給 **AzExpressRouteCircuit** ，授權將會新增至電路，但不會啟用使用。</span><span class="sxs-lookup"><span data-stu-id="08d5b-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="08d5b-113">示例</span><span class="sxs-lookup"><span data-stu-id="08d5b-113">EXAMPLES</span></span>

### <span data-ttu-id="08d5b-114">範例1：將授權新增至指定的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="08d5b-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="08d5b-115">這個範例中的命令會將新的授權新增到現有的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="08d5b-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="08d5b-116">第一個命令使用 **AzExpressRouteCircuit** ，建立名為 ContosoCircuit 的電路的物件參照。</span><span class="sxs-lookup"><span data-stu-id="08d5b-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="08d5b-117">該物件參照會儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="08d5b-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="08d5b-118">在第二個命令中， **AzExpressRouteCircuitAuthorization** Cmdlet 是用來將新的授權 (ContosoCircuitAuthorization) 新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="08d5b-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="08d5b-119">這個命令會新增授權，但不會啟動該授權。</span><span class="sxs-lookup"><span data-stu-id="08d5b-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="08d5b-120">若要啟用授權，您需要在範例中的最後一個命令中顯示 **設定 AzExpressRouteCircuit** 。</span><span class="sxs-lookup"><span data-stu-id="08d5b-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="08d5b-121">參數</span><span class="sxs-lookup"><span data-stu-id="08d5b-121">PARAMETERS</span></span>

### <span data-ttu-id="08d5b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d5b-122">-DefaultProfile</span></span>
<span data-ttu-id="08d5b-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08d5b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08d5b-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08d5b-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="08d5b-125">指定此 Cmdlet 新增授權的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="08d5b-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="08d5b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="08d5b-126">-Name</span></span>
<span data-ttu-id="08d5b-127">指定要新增的線路授權名稱。</span><span class="sxs-lookup"><span data-stu-id="08d5b-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="08d5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d5b-128">CommonParameters</span></span>
<span data-ttu-id="08d5b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08d5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d5b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08d5b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d5b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="08d5b-131">INPUTS</span></span>

### <span data-ttu-id="08d5b-132">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="08d5b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="08d5b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="08d5b-133">OUTPUTS</span></span>

### <span data-ttu-id="08d5b-134">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="08d5b-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="08d5b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="08d5b-135">NOTES</span></span>

## <span data-ttu-id="08d5b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="08d5b-136">RELATED LINKS</span></span>

[<span data-ttu-id="08d5b-137">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08d5b-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="08d5b-138">AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="08d5b-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="08d5b-139">新-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="08d5b-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="08d5b-140">移除-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="08d5b-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="08d5b-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08d5b-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
