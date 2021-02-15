---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131387"
---
# <span data-ttu-id="bdf75-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bdf75-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="bdf75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdf75-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf75-103">取得 ExpressRoute 線路授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf75-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="bdf75-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdf75-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdf75-105">說明</span><span class="sxs-lookup"><span data-stu-id="bdf75-105">DESCRIPTION</span></span>
<span data-ttu-id="bdf75-106">**AzExpressRouteCircuitAuthorization** Cmdlet 會取得指派給 ExpressRoute 回路之授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf75-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="bdf75-107">ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。</span><span class="sxs-lookup"><span data-stu-id="bdf75-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="bdf75-108">ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生一個授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至 (每個虛擬網路) 一個授權的線路。</span><span class="sxs-lookup"><span data-stu-id="bdf75-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="bdf75-109">您可以隨時執行 **AzExpressRouteCircuitAuthorization**，隨時查看授權金鑰以及授權的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf75-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="bdf75-110">示例</span><span class="sxs-lookup"><span data-stu-id="bdf75-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf75-111">範例1：取得所有 ExpressRoute 授權</span><span class="sxs-lookup"><span data-stu-id="bdf75-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="bdf75-112">這些命令會傳回與 ExpressRoute 回路相關聯之所有 ExpressRoute 授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf75-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="bdf75-113">第一個命令使用 **AzExpressRouteCircuit** Cmdlet 來建立物件參照名為 ContosoCircuit 的電路;該物件參照會儲存在 $Circuit 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bdf75-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="bdf75-114">然後，第二個命令會使用該物件參照及 **AzExpressRouteCircuitAuthorization** Cmdlet，傳回與 ContosoCircuit 相關的授權資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf75-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="bdf75-115">範例2：使用 Where-Object Cmdlet 取得所有 ExpressRoute 授權</span><span class="sxs-lookup"><span data-stu-id="bdf75-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="bdf75-116">這些命令代表範例1中所用命令的變化。</span><span class="sxs-lookup"><span data-stu-id="bdf75-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="bdf75-117">不過，在此情況下，只會針對那些可使用 (的授權傳回信息，也就是對於尚未指派給虛擬網路) 的授權。</span><span class="sxs-lookup"><span data-stu-id="bdf75-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="bdf75-118">若要這樣做，請在命令2中傳回線路授權資訊，並以管道 **方式** 傳送到物件 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdf75-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="bdf75-119">**在其中，物件** 只會挑選 *AuthorizationUseStatus* 屬性設定為 [可用] 的授權。</span><span class="sxs-lookup"><span data-stu-id="bdf75-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="bdf75-120">若要只列出那些無法使用的授權，請使用此語法做為 Where 子句： `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="bdf75-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="bdf75-121">參數</span><span class="sxs-lookup"><span data-stu-id="bdf75-121">PARAMETERS</span></span>

### <span data-ttu-id="bdf75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf75-122">-DefaultProfile</span></span>
<span data-ttu-id="bdf75-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdf75-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf75-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bdf75-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bdf75-125">指定 ExpressRoute 線路驗證。</span><span class="sxs-lookup"><span data-stu-id="bdf75-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="bdf75-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdf75-126">-Name</span></span>
<span data-ttu-id="bdf75-127">指定此 Cmdlet 取得的 ExpressRoute 線路授權名稱。</span><span class="sxs-lookup"><span data-stu-id="bdf75-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="bdf75-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="bdf75-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="bdf75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf75-129">CommonParameters</span></span>
<span data-ttu-id="bdf75-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdf75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf75-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bdf75-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf75-132">輸入</span><span class="sxs-lookup"><span data-stu-id="bdf75-132">INPUTS</span></span>

### <span data-ttu-id="bdf75-133">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bdf75-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bdf75-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bdf75-134">OUTPUTS</span></span>

### <span data-ttu-id="bdf75-135">PSExpressRouteCircuitAuthorization 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bdf75-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="bdf75-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bdf75-136">NOTES</span></span>

## <span data-ttu-id="bdf75-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdf75-137">RELATED LINKS</span></span>

[<span data-ttu-id="bdf75-138">附加 AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bdf75-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bdf75-139">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bdf75-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bdf75-140">新-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bdf75-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bdf75-141">移除-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bdf75-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
