---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801985"
---
# <span data-ttu-id="5e097-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="5e097-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e097-102">SYNOPSIS</span></span>
<span data-ttu-id="5e097-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="5e097-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e097-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e097-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e097-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e097-105">DESCRIPTION</span></span>
<span data-ttu-id="5e097-106">**AzureRmExpressRouteCircuit** Cmdlet 會將已修改的 ExpressRoute 電路儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="5e097-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="5e097-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e097-107">EXAMPLES</span></span>

### <span data-ttu-id="5e097-108">範例1：變更 ExpressRoute 電路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="5e097-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="5e097-109">參數</span><span class="sxs-lookup"><span data-stu-id="5e097-109">PARAMETERS</span></span>

### <span data-ttu-id="5e097-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e097-110">-AsJob</span></span>
<span data-ttu-id="5e097-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5e097-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e097-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e097-112">-DefaultProfile</span></span>
<span data-ttu-id="5e097-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e097-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e097-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5e097-115">指定此 Cmdlet 修改的 **ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e097-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e097-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e097-116">CommonParameters</span></span>
<span data-ttu-id="5e097-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e097-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e097-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e097-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e097-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5e097-119">INPUTS</span></span>

### <span data-ttu-id="5e097-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5e097-121">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5e097-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="5e097-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5e097-122">OUTPUTS</span></span>

### <span data-ttu-id="5e097-123">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e097-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5e097-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5e097-124">NOTES</span></span>

## <span data-ttu-id="5e097-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e097-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e097-126">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e097-127">移動流覽 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e097-128">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e097-129">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e097-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
