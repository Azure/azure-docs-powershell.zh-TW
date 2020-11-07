---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800817"
---
# <span data-ttu-id="49fac-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="49fac-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="49fac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49fac-102">SYNOPSIS</span></span>
<span data-ttu-id="49fac-103">將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="49fac-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49fac-104">句法</span><span class="sxs-lookup"><span data-stu-id="49fac-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49fac-105">說明</span><span class="sxs-lookup"><span data-stu-id="49fac-105">DESCRIPTION</span></span>
<span data-ttu-id="49fac-106">**AzureRmExpressRouteCircuit** Cmdlet 會將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="49fac-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="49fac-107">移動之後，ExpressRoute 電路的行為和執行方式就像是在資源管理器部署模型中建立的任何其他 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="49fac-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="49fac-108">不會在此操作中移動線路連結、虛擬網路及 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="49fac-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="49fac-109">在移動之後，必須重新配置那些資源。</span><span class="sxs-lookup"><span data-stu-id="49fac-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="49fac-110">示例</span><span class="sxs-lookup"><span data-stu-id="49fac-110">EXAMPLES</span></span>

### <span data-ttu-id="49fac-111">範例1：將 ExpressRoute 線路移至資源管理器部署模型</span><span class="sxs-lookup"><span data-stu-id="49fac-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="49fac-112">參數</span><span class="sxs-lookup"><span data-stu-id="49fac-112">PARAMETERS</span></span>

### <span data-ttu-id="49fac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49fac-113">-AsJob</span></span>
<span data-ttu-id="49fac-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="49fac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49fac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fac-115">-DefaultProfile</span></span>
<span data-ttu-id="49fac-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49fac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49fac-117">-Force</span><span class="sxs-lookup"><span data-stu-id="49fac-117">-Force</span></span>
<span data-ttu-id="49fac-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="49fac-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49fac-119">-位置</span><span class="sxs-lookup"><span data-stu-id="49fac-119">-Location</span></span>
<span data-ttu-id="49fac-120">ExpressRoute 電路所在之 Azure 位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="49fac-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="49fac-121">-Name</span></span>
<span data-ttu-id="49fac-122">要移動之 ExpressRoute 電路的名稱。</span><span class="sxs-lookup"><span data-stu-id="49fac-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49fac-123">-ResourceGroupName</span></span>
<span data-ttu-id="49fac-124">包含要移動 ExpressRoute 電路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49fac-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="49fac-125">-ServiceKey</span></span>
<span data-ttu-id="49fac-126">在傳統部署模型中，ExpressRoute 回路所使用的服務金鑰。</span><span class="sxs-lookup"><span data-stu-id="49fac-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="49fac-127">-Tag</span></span>
<span data-ttu-id="49fac-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="49fac-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49fac-129">例如：</span><span class="sxs-lookup"><span data-stu-id="49fac-129">For example:</span></span>

<span data-ttu-id="49fac-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="49fac-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-131">-確認</span><span class="sxs-lookup"><span data-stu-id="49fac-131">-Confirm</span></span>
<span data-ttu-id="49fac-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49fac-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fac-133">-WhatIf</span></span>
<span data-ttu-id="49fac-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49fac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49fac-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49fac-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fac-136">CommonParameters</span></span>
<span data-ttu-id="49fac-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49fac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fac-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49fac-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fac-139">輸入</span><span class="sxs-lookup"><span data-stu-id="49fac-139">INPUTS</span></span>

## <span data-ttu-id="49fac-140">輸出</span><span class="sxs-lookup"><span data-stu-id="49fac-140">OUTPUTS</span></span>

### <span data-ttu-id="49fac-141">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49fac-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="49fac-142">筆記</span><span class="sxs-lookup"><span data-stu-id="49fac-142">NOTES</span></span>

## <span data-ttu-id="49fac-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="49fac-143">RELATED LINKS</span></span>

[<span data-ttu-id="49fac-144">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="49fac-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="49fac-145">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="49fac-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="49fac-146">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="49fac-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="49fac-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="49fac-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
