---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 1b4b5b8a56089d7461d92918f5956675390781f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449309"
---
# <span data-ttu-id="5e8ca-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5e8ca-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="5e8ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8ca-103">新增 ExpressRoute 線路驗證。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e8ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e8ca-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e8ca-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8ca-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet 會將授權新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="5e8ca-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5e8ca-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生一個授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至 (每個虛擬網路) 一個授權的線路。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="5e8ca-109">[ **載入 AzureRmExpressRouteCircuitAuthorization** ] 會將新的授權新增至電路，同時也會產生對應的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="5e8ca-110">您可以隨時執行 Get-AzureRmExpressRouteCircuitAuthorization Cmdlet 並視需要來查看這些金鑰，然後將其複製並轉寄給適當的網路擁有者。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="5e8ca-111">請注意，執行 **附加 AzureRmExpressRouteCircuitAuthorization** 之後，您必須呼叫 Set-AzureRmExpressRouteCircuit Cmdlet 才能啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="5e8ca-112">如果您不撥打電話給 **AzureRmExpressRouteCircuit** ，授權將會新增至電路，但不會啟用使用。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="5e8ca-113">示例</span><span class="sxs-lookup"><span data-stu-id="5e8ca-113">EXAMPLES</span></span>

### <span data-ttu-id="5e8ca-114">範例1：將授權新增至指定的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="5e8ca-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="5e8ca-115">這個範例中的命令會將新的授權新增到現有的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="5e8ca-116">第一個命令使用 **AzureRmExpressRouteCircuit** ，建立名為 ContosoCircuit 的電路的物件參照。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="5e8ca-117">該物件參照會儲存在名為 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="5e8ca-118">在第二個命令中， **AzureRmExpressRouteCircuitAuthorization** Cmdlet 是用來將新的授權 (ContosoCircuitAuthorization) 新增至 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="5e8ca-119">這個命令會新增授權，但不會啟動該授權。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="5e8ca-120">若要啟用授權，您需要在範例中的最後一個命令中顯示 **設定 AzureRmExpressRouteCircuit** 。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="5e8ca-121">參數</span><span class="sxs-lookup"><span data-stu-id="5e8ca-121">PARAMETERS</span></span>

### <span data-ttu-id="5e8ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8ca-122">-DefaultProfile</span></span>
<span data-ttu-id="5e8ca-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e8ca-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e8ca-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5e8ca-125">指定此 Cmdlet 新增授權的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="5e8ca-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e8ca-126">-Name</span></span>
<span data-ttu-id="5e8ca-127">指定要新增的線路授權名稱。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8ca-128">CommonParameters</span></span>
<span data-ttu-id="5e8ca-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8ca-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8ca-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5e8ca-131">INPUTS</span></span>

### <span data-ttu-id="5e8ca-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e8ca-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5e8ca-133">**AzureRmExpressRouteCircuitAuthorization** 會接受 PSExpressRouteCircuit 物件的流水線式實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** 物件）。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5e8ca-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5e8ca-134">OUTPUTS</span></span>

### <span data-ttu-id="5e8ca-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e8ca-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5e8ca-136">[ **載入 AzureRmExpressRouteCircuitAuthorization** ] 會修改 PSExpressRouteCircuit 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** 物件）。</span><span class="sxs-lookup"><span data-stu-id="5e8ca-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5e8ca-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5e8ca-137">NOTES</span></span>

## <span data-ttu-id="5e8ca-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e8ca-138">RELATED LINKS</span></span>

[<span data-ttu-id="5e8ca-139">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e8ca-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e8ca-140">AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5e8ca-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5e8ca-141">新-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5e8ca-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5e8ca-142">移除-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5e8ca-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5e8ca-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e8ca-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
