---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 6813d1e1abf8e1f1b978c3cbcdf5a52fed92f96f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790513"
---
# <span data-ttu-id="12177-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="12177-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12177-102">SYNOPSIS</span></span>
<span data-ttu-id="12177-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="12177-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="12177-104">句法</span><span class="sxs-lookup"><span data-stu-id="12177-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12177-105">說明</span><span class="sxs-lookup"><span data-stu-id="12177-105">DESCRIPTION</span></span>
<span data-ttu-id="12177-106">**AzExpressRouteCircuit** Cmdlet 會將已修改的 ExpressRoute 電路儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="12177-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="12177-107">示例</span><span class="sxs-lookup"><span data-stu-id="12177-107">EXAMPLES</span></span>

### <span data-ttu-id="12177-108">範例1：變更 ExpressRoute 電路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="12177-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="12177-109">參數</span><span class="sxs-lookup"><span data-stu-id="12177-109">PARAMETERS</span></span>

### <span data-ttu-id="12177-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12177-110">-AsJob</span></span>
<span data-ttu-id="12177-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12177-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12177-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12177-112">-DefaultProfile</span></span>
<span data-ttu-id="12177-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12177-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12177-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="12177-115">指定此 Cmdlet 修改的 **ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="12177-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="12177-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12177-116">CommonParameters</span></span>
<span data-ttu-id="12177-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12177-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12177-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12177-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12177-119">輸入</span><span class="sxs-lookup"><span data-stu-id="12177-119">INPUTS</span></span>

### <span data-ttu-id="12177-120">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12177-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="12177-121">輸出</span><span class="sxs-lookup"><span data-stu-id="12177-121">OUTPUTS</span></span>

### <span data-ttu-id="12177-122">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="12177-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="12177-123">筆記</span><span class="sxs-lookup"><span data-stu-id="12177-123">NOTES</span></span>

## <span data-ttu-id="12177-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="12177-124">RELATED LINKS</span></span>

[<span data-ttu-id="12177-125">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="12177-126">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="12177-127">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="12177-128">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12177-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
