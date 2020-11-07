---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800465"
---
# <span data-ttu-id="d5d8b-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5d8b-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d5d8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d8b-103">從 Azure 取得 Azure ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5d8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5d8b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d8b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d8b-106">**AzureRmExpressRouteCircuit** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="d5d8b-107">傳回的電路物件可以用來做為其他 Cmdlet 的輸入，以在 ExpressRoute 回路上運作。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="d5d8b-108">示例</span><span class="sxs-lookup"><span data-stu-id="d5d8b-108">EXAMPLES</span></span>

### <span data-ttu-id="d5d8b-109">範例1：取得要刪除的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="d5d8b-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="d5d8b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="d5d8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d8b-111">-DefaultProfile</span></span>
<span data-ttu-id="d5d8b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d8b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5d8b-113">-Name</span></span>
<span data-ttu-id="d5d8b-114">ExpressRoute 回路的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d5d8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5d8b-116">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d5d8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d8b-117">CommonParameters</span></span>
<span data-ttu-id="d5d8b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d8b-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5d8b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d8b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d8b-120">INPUTS</span></span>

## <span data-ttu-id="d5d8b-121">輸出</span><span class="sxs-lookup"><span data-stu-id="d5d8b-121">OUTPUTS</span></span>

### <span data-ttu-id="d5d8b-122">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d5d8b-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d5d8b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="d5d8b-123">NOTES</span></span>

## <span data-ttu-id="d5d8b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5d8b-124">RELATED LINKS</span></span>

[<span data-ttu-id="d5d8b-125">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5d8b-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5d8b-126">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5d8b-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5d8b-127">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5d8b-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5d8b-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5d8b-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
