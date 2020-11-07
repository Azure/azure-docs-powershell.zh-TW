---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795428"
---
# <span data-ttu-id="72bdc-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="72bdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="72bdc-103">修改 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="72bdc-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="72bdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="72bdc-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72bdc-105">說明</span><span class="sxs-lookup"><span data-stu-id="72bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="72bdc-106">**AzExpressRouteCircuit** Cmdlet 會將已修改的 ExpressRoute 電路儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="72bdc-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="72bdc-107">示例</span><span class="sxs-lookup"><span data-stu-id="72bdc-107">EXAMPLES</span></span>

### <span data-ttu-id="72bdc-108">範例1：變更 ExpressRoute 電路的 ServiceKey</span><span class="sxs-lookup"><span data-stu-id="72bdc-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="72bdc-109">參數</span><span class="sxs-lookup"><span data-stu-id="72bdc-109">PARAMETERS</span></span>

### <span data-ttu-id="72bdc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72bdc-110">-AsJob</span></span>
<span data-ttu-id="72bdc-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="72bdc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72bdc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bdc-112">-DefaultProfile</span></span>
<span data-ttu-id="72bdc-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72bdc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bdc-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="72bdc-115">指定此 Cmdlet 修改的 **ExpressRouteCircuit** 物件。</span><span class="sxs-lookup"><span data-stu-id="72bdc-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="72bdc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bdc-116">CommonParameters</span></span>
<span data-ttu-id="72bdc-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72bdc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bdc-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72bdc-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bdc-119">輸入</span><span class="sxs-lookup"><span data-stu-id="72bdc-119">INPUTS</span></span>

### <span data-ttu-id="72bdc-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="72bdc-121">形參 "ExpressRouteCircuit" 接受管線中 "PSExpressRouteCircuit" 類型的值</span><span class="sxs-lookup"><span data-stu-id="72bdc-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="72bdc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="72bdc-122">OUTPUTS</span></span>

### <span data-ttu-id="72bdc-123">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="72bdc-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="72bdc-124">筆記</span><span class="sxs-lookup"><span data-stu-id="72bdc-124">NOTES</span></span>

## <span data-ttu-id="72bdc-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="72bdc-125">RELATED LINKS</span></span>

[<span data-ttu-id="72bdc-126">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="72bdc-127">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="72bdc-128">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="72bdc-129">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72bdc-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
