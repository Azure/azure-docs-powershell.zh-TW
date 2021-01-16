---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277063"
---
# <span data-ttu-id="55e64-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55e64-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="55e64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55e64-102">SYNOPSIS</span></span>
<span data-ttu-id="55e64-103">將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="55e64-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="55e64-104">句法</span><span class="sxs-lookup"><span data-stu-id="55e64-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55e64-105">說明</span><span class="sxs-lookup"><span data-stu-id="55e64-105">DESCRIPTION</span></span>
<span data-ttu-id="55e64-106">**AzExpressRouteCircuit** Cmdlet 會將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="55e64-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="55e64-107">移動之後，ExpressRoute 電路的行為和執行方式就像是在資源管理器部署模型中建立的任何其他 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="55e64-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="55e64-108">不會在此操作中移動線路連結、虛擬網路及 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="55e64-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="55e64-109">在移動之後，必須重新配置那些資源。</span><span class="sxs-lookup"><span data-stu-id="55e64-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="55e64-110">示例</span><span class="sxs-lookup"><span data-stu-id="55e64-110">EXAMPLES</span></span>

### <span data-ttu-id="55e64-111">範例1：將 ExpressRoute 線路移至資源管理器部署模型</span><span class="sxs-lookup"><span data-stu-id="55e64-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="55e64-112">參數</span><span class="sxs-lookup"><span data-stu-id="55e64-112">PARAMETERS</span></span>

### <span data-ttu-id="55e64-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55e64-113">-AsJob</span></span>
<span data-ttu-id="55e64-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55e64-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55e64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e64-115">-DefaultProfile</span></span>
<span data-ttu-id="55e64-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55e64-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e64-117">-Force</span><span class="sxs-lookup"><span data-stu-id="55e64-117">-Force</span></span>
<span data-ttu-id="55e64-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="55e64-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55e64-119">-位置</span><span class="sxs-lookup"><span data-stu-id="55e64-119">-Location</span></span>
<span data-ttu-id="55e64-120">ExpressRoute 電路所在之 Azure 位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e64-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="55e64-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="55e64-121">-Name</span></span>
<span data-ttu-id="55e64-122">要移動之 ExpressRoute 電路的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e64-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="55e64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e64-123">-ResourceGroupName</span></span>
<span data-ttu-id="55e64-124">包含要移動 ExpressRoute 電路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e64-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="55e64-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="55e64-125">-ServiceKey</span></span>
<span data-ttu-id="55e64-126">在傳統部署模型中，ExpressRoute 回路所使用的服務金鑰。</span><span class="sxs-lookup"><span data-stu-id="55e64-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="55e64-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="55e64-127">-Tag</span></span>
<span data-ttu-id="55e64-128">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="55e64-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55e64-129">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="55e64-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55e64-130">-確認</span><span class="sxs-lookup"><span data-stu-id="55e64-130">-Confirm</span></span>
<span data-ttu-id="55e64-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55e64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e64-132">-WhatIf</span></span>
<span data-ttu-id="55e64-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55e64-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55e64-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55e64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e64-135">CommonParameters</span></span>
<span data-ttu-id="55e64-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55e64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e64-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55e64-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e64-138">輸入</span><span class="sxs-lookup"><span data-stu-id="55e64-138">INPUTS</span></span>

### <span data-ttu-id="55e64-139">System.object</span><span class="sxs-lookup"><span data-stu-id="55e64-139">System.String</span></span>

### <span data-ttu-id="55e64-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55e64-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55e64-141">輸出</span><span class="sxs-lookup"><span data-stu-id="55e64-141">OUTPUTS</span></span>

### <span data-ttu-id="55e64-142">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55e64-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="55e64-143">筆記</span><span class="sxs-lookup"><span data-stu-id="55e64-143">NOTES</span></span>

## <span data-ttu-id="55e64-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="55e64-144">RELATED LINKS</span></span>

[<span data-ttu-id="55e64-145">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55e64-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="55e64-146">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55e64-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="55e64-147">移除-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55e64-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="55e64-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55e64-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
