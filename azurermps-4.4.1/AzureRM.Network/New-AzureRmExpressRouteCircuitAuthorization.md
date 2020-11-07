---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625489"
---
# <span data-ttu-id="74e4d-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="74e4d-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="74e4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="74e4d-103">建立 ExpressRoute 線路驗證。</span><span class="sxs-lookup"><span data-stu-id="74e4d-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74e4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="74e4d-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74e4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="74e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="74e4d-106">**新的 AzureRmExpressRouteCircuitAuthorization** Cmdlet 會建立可新增至 ExpressRoute 回路的線路驗證。</span><span class="sxs-lookup"><span data-stu-id="74e4d-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="74e4d-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="74e4d-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="74e4d-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生可供虛擬網路擁有者用來將網路連接至電路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="74e4d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="74e4d-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="74e4d-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="74e4d-110">在您建立 ExpressRoute 電路之後，您可以使用 [ **載入 AzureRmExpressRouteCircuitAuthorization** ] 來新增該線路的授權。</span><span class="sxs-lookup"><span data-stu-id="74e4d-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="74e4d-111">或者，您也可以使用 [ **新-AzureRmExpressRouteCircuitAuthorization** ] 建立授權，在建立該電路時，可以將該授權新增到新的電路中。</span><span class="sxs-lookup"><span data-stu-id="74e4d-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="74e4d-112">示例</span><span class="sxs-lookup"><span data-stu-id="74e4d-112">EXAMPLES</span></span>

### <span data-ttu-id="74e4d-113">範例1：建立新的線路驗證</span><span class="sxs-lookup"><span data-stu-id="74e4d-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="74e4d-114">這個命令會建立一個名為 ContosoCircuitAuthorization 的新線路授權，然後將該物件儲存在名為 $Authorization 的變數中。</span><span class="sxs-lookup"><span data-stu-id="74e4d-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="74e4d-115">將物件儲存到變數是重要的：雖然 **新的 AzureRmExpressRouteCircuitAuthorization** 可以建立線路驗證，但它無法將該授權新增至線路路線。</span><span class="sxs-lookup"><span data-stu-id="74e4d-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="74e4d-116">相反地，在建立全新的 ExpressRoute 電路時，會使用變數 $Authorization New-AzureRmExpressRouteCircuit。</span><span class="sxs-lookup"><span data-stu-id="74e4d-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="74e4d-117">如需詳細資訊，請參閱 New-AzureRmExpressRouteCircuit Cmdlet 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="74e4d-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="74e4d-118">參數</span><span class="sxs-lookup"><span data-stu-id="74e4d-118">PARAMETERS</span></span>

### <span data-ttu-id="74e4d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="74e4d-119">-Name</span></span>
<span data-ttu-id="74e4d-120">為新的 ExpressRoute 線路驗證指定唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="74e4d-120">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="74e4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e4d-121">-DefaultProfile</span></span>
<span data-ttu-id="74e4d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74e4d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74e4d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e4d-123">CommonParameters</span></span>
<span data-ttu-id="74e4d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74e4d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e4d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74e4d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e4d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="74e4d-126">INPUTS</span></span>

### <span data-ttu-id="74e4d-127">所有</span><span class="sxs-lookup"><span data-stu-id="74e4d-127">None</span></span>
<span data-ttu-id="74e4d-128">這個 Cmdlet 不接受流水線輸入。</span><span class="sxs-lookup"><span data-stu-id="74e4d-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="74e4d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="74e4d-129">OUTPUTS</span></span>

### <span data-ttu-id="74e4d-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="74e4d-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="74e4d-131">這個 Cmdlet 會建立 PSExpressRouteCircuitAuthorization 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** 物件）。</span><span class="sxs-lookup"><span data-stu-id="74e4d-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="74e4d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="74e4d-132">NOTES</span></span>

## <span data-ttu-id="74e4d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="74e4d-133">RELATED LINKS</span></span>

[<span data-ttu-id="74e4d-134">附加 AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="74e4d-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="74e4d-135">AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="74e4d-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="74e4d-136">移除-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="74e4d-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

