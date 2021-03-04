---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 71571d9fe6eccee73efda01015a877014c67c9ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901937"
---
# <span data-ttu-id="e410c-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="e410c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e410c-102">SYNOPSIS</span></span>
<span data-ttu-id="e410c-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="e410c-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e410c-104">語法</span><span class="sxs-lookup"><span data-stu-id="e410c-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e410c-105">描述</span><span class="sxs-lookup"><span data-stu-id="e410c-105">DESCRIPTION</span></span>
<span data-ttu-id="e410c-106">**Set-AzExpressRouteCircuit** Cmdlet 會將修改後的 ExpressRoute 回路存到 Azure。</span><span class="sxs-lookup"><span data-stu-id="e410c-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="e410c-107">例子</span><span class="sxs-lookup"><span data-stu-id="e410c-107">EXAMPLES</span></span>

### <span data-ttu-id="e410c-108">範例 1：變更 ExpressRoute 回路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="e410c-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="e410c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e410c-109">PARAMETERS</span></span>

### <span data-ttu-id="e410c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e410c-110">-AsJob</span></span>
<span data-ttu-id="e410c-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e410c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e410c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e410c-112">-DefaultProfile</span></span>
<span data-ttu-id="e410c-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e410c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e410c-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e410c-115">指定此 **Cmdlet 修改的 ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="e410c-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e410c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e410c-116">CommonParameters</span></span>
<span data-ttu-id="e410c-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e410c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e410c-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e410c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e410c-119">輸入</span><span class="sxs-lookup"><span data-stu-id="e410c-119">INPUTS</span></span>

### <span data-ttu-id="e410c-120">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e410c-121">輸出</span><span class="sxs-lookup"><span data-stu-id="e410c-121">OUTPUTS</span></span>

### <span data-ttu-id="e410c-122">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e410c-123">筆記</span><span class="sxs-lookup"><span data-stu-id="e410c-123">NOTES</span></span>

## <span data-ttu-id="e410c-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="e410c-124">RELATED LINKS</span></span>

[<span data-ttu-id="e410c-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e410c-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="e410c-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="e410c-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e410c-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
