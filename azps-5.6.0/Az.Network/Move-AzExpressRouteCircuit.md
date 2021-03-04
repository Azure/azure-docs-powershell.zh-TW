---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901973"
---
# <span data-ttu-id="7a711-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7a711-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a711-102">SYNOPSIS</span></span>
<span data-ttu-id="7a711-103">將 ExpressRoute 回路從傳統部署模型移至 Resource Manager 部署模型。</span><span class="sxs-lookup"><span data-stu-id="7a711-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="7a711-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a711-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a711-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a711-105">DESCRIPTION</span></span>
<span data-ttu-id="7a711-106">**Move-AzExpressRouteCircuit** Cmdlet 會將 ExpressRoute 回路從傳統部署模型移至 Resource Manager 部署模型。</span><span class="sxs-lookup"><span data-stu-id="7a711-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="7a711-107">移動之後，ExpressRoute 回路的行為及執行方式會與在 Resource Manager 部署模型中建立的其他 ExpressRoute 回路類似。</span><span class="sxs-lookup"><span data-stu-id="7a711-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="7a711-108">此作業不會移動回路連結、虛擬網路和 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="7a711-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="7a711-109">移動之後，必須重新配置這些資源。</span><span class="sxs-lookup"><span data-stu-id="7a711-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="7a711-110">例子</span><span class="sxs-lookup"><span data-stu-id="7a711-110">EXAMPLES</span></span>

### <span data-ttu-id="7a711-111">範例 1：將 ExpressRoute 回路移至 Resource Manager 部署模型</span><span class="sxs-lookup"><span data-stu-id="7a711-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="7a711-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a711-112">PARAMETERS</span></span>

### <span data-ttu-id="7a711-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a711-113">-AsJob</span></span>
<span data-ttu-id="7a711-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a711-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a711-115">-DefaultProfile</span></span>
<span data-ttu-id="7a711-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a711-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a711-117">-強制</span><span class="sxs-lookup"><span data-stu-id="7a711-117">-Force</span></span>
<span data-ttu-id="7a711-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7a711-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a711-119">-位置</span><span class="sxs-lookup"><span data-stu-id="7a711-119">-Location</span></span>
<span data-ttu-id="7a711-120">ExpressRoute 回路所在的 Azure 位置名稱。</span><span class="sxs-lookup"><span data-stu-id="7a711-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a711-121">-Name</span></span>
<span data-ttu-id="7a711-122">要移動的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="7a711-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a711-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a711-124">將包含要移動 ExpressRoute 回路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7a711-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="7a711-125">-ServiceKey</span></span>
<span data-ttu-id="7a711-126">ExpressRoute 回路在傳統部署模型中使用的服務金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a711-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-127">-標記</span><span class="sxs-lookup"><span data-stu-id="7a711-127">-Tag</span></span>
<span data-ttu-id="7a711-128">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="7a711-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7a711-129">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7a711-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-130">-確認</span><span class="sxs-lookup"><span data-stu-id="7a711-130">-Confirm</span></span>
<span data-ttu-id="7a711-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7a711-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a711-132">-WhatIf</span></span>
<span data-ttu-id="7a711-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a711-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a711-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a711-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a711-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a711-135">CommonParameters</span></span>
<span data-ttu-id="7a711-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a711-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a711-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7a711-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a711-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7a711-138">INPUTS</span></span>

### <span data-ttu-id="7a711-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7a711-139">System.String</span></span>

### <span data-ttu-id="7a711-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a711-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7a711-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7a711-141">OUTPUTS</span></span>

### <span data-ttu-id="7a711-142">Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7a711-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7a711-143">NOTES</span></span>

## <span data-ttu-id="7a711-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a711-144">RELATED LINKS</span></span>

[<span data-ttu-id="7a711-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7a711-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7a711-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="7a711-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7a711-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
