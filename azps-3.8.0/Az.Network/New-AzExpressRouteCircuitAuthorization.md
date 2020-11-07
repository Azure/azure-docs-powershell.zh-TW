---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966194"
---
# <span data-ttu-id="69074-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="69074-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="69074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69074-102">SYNOPSIS</span></span>
<span data-ttu-id="69074-103">建立 ExpressRoute 線路驗證。</span><span class="sxs-lookup"><span data-stu-id="69074-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="69074-104">句法</span><span class="sxs-lookup"><span data-stu-id="69074-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69074-105">說明</span><span class="sxs-lookup"><span data-stu-id="69074-105">DESCRIPTION</span></span>
<span data-ttu-id="69074-106">**新的 AzExpressRouteCircuitAuthorization** Cmdlet 會建立可新增至 ExpressRoute 回路的線路驗證。</span><span class="sxs-lookup"><span data-stu-id="69074-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="69074-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="69074-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="69074-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生可供虛擬網路擁有者用來將網路連接至電路的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="69074-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="69074-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="69074-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="69074-110">在您建立 ExpressRoute 電路之後，您可以使用 [ **載入 AzExpressRouteCircuitAuthorization** ] 來新增該線路的授權。</span><span class="sxs-lookup"><span data-stu-id="69074-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="69074-111">或者，您也可以使用 [ **新-AzExpressRouteCircuitAuthorization** ] 建立授權，在建立該電路時，可以將該授權新增到新的電路中。</span><span class="sxs-lookup"><span data-stu-id="69074-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="69074-112">示例</span><span class="sxs-lookup"><span data-stu-id="69074-112">EXAMPLES</span></span>

### <span data-ttu-id="69074-113">範例1：建立新的線路驗證</span><span class="sxs-lookup"><span data-stu-id="69074-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="69074-114">這個命令會建立一個名為 ContosoCircuitAuthorization 的新線路授權，然後將該物件儲存在名為 $Authorization 的變數中。</span><span class="sxs-lookup"><span data-stu-id="69074-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="69074-115">將物件儲存到變數是重要的：雖然 **新的 AzExpressRouteCircuitAuthorization** 可以建立線路驗證，但它無法將該授權新增至線路路線。</span><span class="sxs-lookup"><span data-stu-id="69074-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="69074-116">相反地，在建立全新的 ExpressRoute 電路時，會使用變數 $Authorization New-AzExpressRouteCircuit。</span><span class="sxs-lookup"><span data-stu-id="69074-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="69074-117">如需詳細資訊，請參閱 New-AzExpressRouteCircuit Cmdlet 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="69074-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="69074-118">參數</span><span class="sxs-lookup"><span data-stu-id="69074-118">PARAMETERS</span></span>

### <span data-ttu-id="69074-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69074-119">-DefaultProfile</span></span>
<span data-ttu-id="69074-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69074-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69074-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="69074-121">-Name</span></span>
<span data-ttu-id="69074-122">為新的 ExpressRoute 線路驗證指定唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="69074-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="69074-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69074-123">CommonParameters</span></span>
<span data-ttu-id="69074-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69074-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69074-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69074-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69074-126">輸入</span><span class="sxs-lookup"><span data-stu-id="69074-126">INPUTS</span></span>

### <span data-ttu-id="69074-127">所有</span><span class="sxs-lookup"><span data-stu-id="69074-127">None</span></span>

## <span data-ttu-id="69074-128">輸出</span><span class="sxs-lookup"><span data-stu-id="69074-128">OUTPUTS</span></span>

### <span data-ttu-id="69074-129">PSExpressRouteCircuitAuthorization 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="69074-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="69074-130">筆記</span><span class="sxs-lookup"><span data-stu-id="69074-130">NOTES</span></span>

## <span data-ttu-id="69074-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="69074-131">RELATED LINKS</span></span>

[<span data-ttu-id="69074-132">附加 AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="69074-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="69074-133">AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="69074-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="69074-134">移除-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="69074-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

