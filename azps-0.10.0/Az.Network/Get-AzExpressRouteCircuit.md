---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794441"
---
# <span data-ttu-id="9fde0-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fde0-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="9fde0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fde0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fde0-103">從 Azure 取得 Azure ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="9fde0-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="9fde0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fde0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fde0-105">說明</span><span class="sxs-lookup"><span data-stu-id="9fde0-105">DESCRIPTION</span></span>
<span data-ttu-id="9fde0-106">**AzExpressRouteCircuit** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="9fde0-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="9fde0-107">傳回的電路物件可以用來做為其他 Cmdlet 的輸入，以在 ExpressRoute 回路上運作。</span><span class="sxs-lookup"><span data-stu-id="9fde0-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="9fde0-108">示例</span><span class="sxs-lookup"><span data-stu-id="9fde0-108">EXAMPLES</span></span>

### <span data-ttu-id="9fde0-109">範例1：取得要刪除的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="9fde0-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="9fde0-110">參數</span><span class="sxs-lookup"><span data-stu-id="9fde0-110">PARAMETERS</span></span>

### <span data-ttu-id="9fde0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fde0-111">-DefaultProfile</span></span>
<span data-ttu-id="9fde0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fde0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fde0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fde0-113">-Name</span></span>
<span data-ttu-id="9fde0-114">ExpressRoute 回路的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fde0-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fde0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fde0-115">-ResourceGroupName</span></span>
<span data-ttu-id="9fde0-116">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fde0-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fde0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fde0-117">CommonParameters</span></span>
<span data-ttu-id="9fde0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fde0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fde0-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fde0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fde0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9fde0-120">INPUTS</span></span>

## <span data-ttu-id="9fde0-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9fde0-121">OUTPUTS</span></span>

### <span data-ttu-id="9fde0-122">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9fde0-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9fde0-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9fde0-123">NOTES</span></span>

## <span data-ttu-id="9fde0-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fde0-124">RELATED LINKS</span></span>

[<span data-ttu-id="9fde0-125">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fde0-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="9fde0-126">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fde0-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="9fde0-127">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fde0-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="9fde0-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9fde0-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
