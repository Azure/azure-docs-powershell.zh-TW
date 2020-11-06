---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456943"
---
# <span data-ttu-id="b55b0-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="b55b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b55b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b55b0-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="b55b0-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b55b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b55b0-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b55b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="b55b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b55b0-106">**AzureRmExpressRouteCircuit** Cmdlet 會將已修改的 ExpressRoute 電路儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="b55b0-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="b55b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="b55b0-107">EXAMPLES</span></span>

### <span data-ttu-id="b55b0-108">範例1：變更 ExpressRoute 電路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="b55b0-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="b55b0-109">參數</span><span class="sxs-lookup"><span data-stu-id="b55b0-109">PARAMETERS</span></span>

### <span data-ttu-id="b55b0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b55b0-110">-AsJob</span></span>
<span data-ttu-id="b55b0-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b55b0-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55b0-112">-DefaultProfile</span></span>
<span data-ttu-id="b55b0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b55b0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b55b0-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b55b0-115">指定此 Cmdlet 修改的 **ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="b55b0-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b55b0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55b0-116">CommonParameters</span></span>
<span data-ttu-id="b55b0-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b55b0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55b0-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b55b0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55b0-119">輸入</span><span class="sxs-lookup"><span data-stu-id="b55b0-119">INPUTS</span></span>

### <span data-ttu-id="b55b0-120">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b55b0-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="b55b0-121">參數： ExpressRouteCircuit (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b55b0-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="b55b0-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b55b0-122">OUTPUTS</span></span>

### <span data-ttu-id="b55b0-123">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b55b0-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b55b0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b55b0-124">NOTES</span></span>

## <span data-ttu-id="b55b0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b55b0-125">RELATED LINKS</span></span>

[<span data-ttu-id="b55b0-126">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b55b0-127">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b55b0-128">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b55b0-129">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b55b0-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
