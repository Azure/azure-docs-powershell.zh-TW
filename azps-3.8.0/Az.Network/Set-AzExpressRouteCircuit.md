---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959045"
---
# <span data-ttu-id="cd631-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="cd631-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd631-102">SYNOPSIS</span></span>
<span data-ttu-id="cd631-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="cd631-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="cd631-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd631-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd631-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd631-105">DESCRIPTION</span></span>
<span data-ttu-id="cd631-106">**AzExpressRouteCircuit** Cmdlet 會將已修改的 ExpressRoute 電路儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="cd631-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="cd631-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd631-107">EXAMPLES</span></span>

### <span data-ttu-id="cd631-108">範例1：變更 ExpressRoute 電路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="cd631-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="cd631-109">參數</span><span class="sxs-lookup"><span data-stu-id="cd631-109">PARAMETERS</span></span>

### <span data-ttu-id="cd631-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd631-110">-AsJob</span></span>
<span data-ttu-id="cd631-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd631-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd631-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd631-112">-DefaultProfile</span></span>
<span data-ttu-id="cd631-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd631-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd631-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cd631-115">指定此 Cmdlet 修改的 **ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="cd631-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd631-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd631-116">CommonParameters</span></span>
<span data-ttu-id="cd631-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd631-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd631-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd631-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd631-119">輸入</span><span class="sxs-lookup"><span data-stu-id="cd631-119">INPUTS</span></span>

### <span data-ttu-id="cd631-120">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cd631-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cd631-121">輸出</span><span class="sxs-lookup"><span data-stu-id="cd631-121">OUTPUTS</span></span>

### <span data-ttu-id="cd631-122">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cd631-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cd631-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cd631-123">NOTES</span></span>

## <span data-ttu-id="cd631-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd631-124">RELATED LINKS</span></span>

[<span data-ttu-id="cd631-125">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="cd631-126">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="cd631-127">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="cd631-128">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cd631-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
