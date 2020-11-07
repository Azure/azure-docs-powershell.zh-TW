---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 969d7c5f55d210cdff74066d08af50bbcc47181e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624373"
---
# <span data-ttu-id="70e89-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70e89-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="70e89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70e89-102">SYNOPSIS</span></span>
<span data-ttu-id="70e89-103">從 Azure 取得 Azure ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="70e89-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70e89-104">句法</span><span class="sxs-lookup"><span data-stu-id="70e89-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e89-105">說明</span><span class="sxs-lookup"><span data-stu-id="70e89-105">DESCRIPTION</span></span>
<span data-ttu-id="70e89-106">**AzureRmExpressRouteCircuit** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 回路物件。</span><span class="sxs-lookup"><span data-stu-id="70e89-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="70e89-107">傳回的電路物件可以用來做為其他 Cmdlet 的輸入，以在 ExpressRoute 回路上運作。</span><span class="sxs-lookup"><span data-stu-id="70e89-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="70e89-108">示例</span><span class="sxs-lookup"><span data-stu-id="70e89-108">EXAMPLES</span></span>

### <span data-ttu-id="70e89-109">範例1：取得要刪除的 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="70e89-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="70e89-110">參數</span><span class="sxs-lookup"><span data-stu-id="70e89-110">PARAMETERS</span></span>

### <span data-ttu-id="70e89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e89-111">-DefaultProfile</span></span>
<span data-ttu-id="70e89-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70e89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70e89-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="70e89-113">-Name</span></span>
<span data-ttu-id="70e89-114">ExpressRoute 回路的名稱。</span><span class="sxs-lookup"><span data-stu-id="70e89-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e89-115">-ResourceGroupName</span></span>
<span data-ttu-id="70e89-116">包含 ExpressRoute 回路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70e89-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70e89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e89-117">CommonParameters</span></span>
<span data-ttu-id="70e89-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70e89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e89-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70e89-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e89-120">輸入</span><span class="sxs-lookup"><span data-stu-id="70e89-120">INPUTS</span></span>

### <span data-ttu-id="70e89-121">System.object</span><span class="sxs-lookup"><span data-stu-id="70e89-121">System.String</span></span>

## <span data-ttu-id="70e89-122">輸出</span><span class="sxs-lookup"><span data-stu-id="70e89-122">OUTPUTS</span></span>

### <span data-ttu-id="70e89-123">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70e89-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="70e89-124">筆記</span><span class="sxs-lookup"><span data-stu-id="70e89-124">NOTES</span></span>

## <span data-ttu-id="70e89-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="70e89-125">RELATED LINKS</span></span>

[<span data-ttu-id="70e89-126">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70e89-126">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="70e89-127">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70e89-127">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="70e89-128">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70e89-128">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="70e89-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70e89-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
