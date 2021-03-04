---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913154"
---
# <span data-ttu-id="78af1-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="78af1-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="78af1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78af1-102">SYNOPSIS</span></span>
<span data-ttu-id="78af1-103">建立 ExpressRoute 回路授權。</span><span class="sxs-lookup"><span data-stu-id="78af1-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="78af1-104">語法</span><span class="sxs-lookup"><span data-stu-id="78af1-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78af1-105">描述</span><span class="sxs-lookup"><span data-stu-id="78af1-105">DESCRIPTION</span></span>
<span data-ttu-id="78af1-106">**New-AzExpressRouteRouteCircuitAuthorization** Cmdlet 會建立一個可以新加入 ExpressRoute 回路的回路授權。</span><span class="sxs-lookup"><span data-stu-id="78af1-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="78af1-107">ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="78af1-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="78af1-108">ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，由虛擬網路擁有者用來將網路連接至回路。</span><span class="sxs-lookup"><span data-stu-id="78af1-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="78af1-109">每個虛擬網路只能有一個授權。</span><span class="sxs-lookup"><span data-stu-id="78af1-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="78af1-110">建立 ExpressRoute 回路之後，您可以使用 **Add-AzExpressRouteCircuitAuthorization** 來新增該回路的授權。</span><span class="sxs-lookup"><span data-stu-id="78af1-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="78af1-111">或者，您可以使用 **New-AzExpressRouteRouteCircuitAuthorization** 來建立可在建立回路時新回路中新增的授權。</span><span class="sxs-lookup"><span data-stu-id="78af1-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="78af1-112">例子</span><span class="sxs-lookup"><span data-stu-id="78af1-112">EXAMPLES</span></span>

### <span data-ttu-id="78af1-113">範例 1：建立新回路授權</span><span class="sxs-lookup"><span data-stu-id="78af1-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="78af1-114">此命令會建立名為 ContosoCircuitAuthorization 的新回路授權，然後將該物件儲存在名為 contosoCircuitAuthorization 的$Authorization。</span><span class="sxs-lookup"><span data-stu-id="78af1-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="78af1-115">將物件另存到變數很重要：雖然 **New-AzExpressRouteCircuitAuthorization** 可以建立回路授權，但無法將該授權新加到回路路由。</span><span class="sxs-lookup"><span data-stu-id="78af1-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="78af1-116">相反地，在$Authorization ExpressRoute 回路New-AzExpressRouteCircuit使用變數變數。</span><span class="sxs-lookup"><span data-stu-id="78af1-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="78af1-117">詳細資訊請參閱 Cmdlet New-AzExpressRouteCircuit檔。</span><span class="sxs-lookup"><span data-stu-id="78af1-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="78af1-118">參數</span><span class="sxs-lookup"><span data-stu-id="78af1-118">PARAMETERS</span></span>

### <span data-ttu-id="78af1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78af1-119">-DefaultProfile</span></span>
<span data-ttu-id="78af1-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78af1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78af1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="78af1-121">-Name</span></span>
<span data-ttu-id="78af1-122">指定新 ExpressRoute 回路授權的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="78af1-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="78af1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78af1-123">CommonParameters</span></span>
<span data-ttu-id="78af1-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78af1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78af1-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="78af1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78af1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="78af1-126">INPUTS</span></span>

### <span data-ttu-id="78af1-127">沒有</span><span class="sxs-lookup"><span data-stu-id="78af1-127">None</span></span>

## <span data-ttu-id="78af1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="78af1-128">OUTPUTS</span></span>

### <span data-ttu-id="78af1-129">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="78af1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="78af1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="78af1-130">NOTES</span></span>

## <span data-ttu-id="78af1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="78af1-131">RELATED LINKS</span></span>

[<span data-ttu-id="78af1-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="78af1-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="78af1-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="78af1-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="78af1-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="78af1-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

