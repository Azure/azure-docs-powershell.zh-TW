---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451612"
---
# <span data-ttu-id="4afa7-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4afa7-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4afa7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4afa7-102">SYNOPSIS</span></span>
<span data-ttu-id="4afa7-103">將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="4afa7-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4afa7-104">句法</span><span class="sxs-lookup"><span data-stu-id="4afa7-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afa7-105">說明</span><span class="sxs-lookup"><span data-stu-id="4afa7-105">DESCRIPTION</span></span>
<span data-ttu-id="4afa7-106">**AzureRmExpressRouteCircuit** Cmdlet 會將 ExpressRoute 回路從傳統部署模型移至資源管理器部署模型。</span><span class="sxs-lookup"><span data-stu-id="4afa7-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="4afa7-107">移動之後，ExpressRoute 電路的行為和執行方式就像是在資源管理器部署模型中建立的任何其他 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="4afa7-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="4afa7-108">不會在此操作中移動線路連結、虛擬網路及 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="4afa7-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="4afa7-109">在移動之後，必須重新配置那些資源。</span><span class="sxs-lookup"><span data-stu-id="4afa7-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="4afa7-110">示例</span><span class="sxs-lookup"><span data-stu-id="4afa7-110">EXAMPLES</span></span>

### <span data-ttu-id="4afa7-111">範例1：將 ExpressRoute 線路移至資源管理器部署模型</span><span class="sxs-lookup"><span data-stu-id="4afa7-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="4afa7-112">參數</span><span class="sxs-lookup"><span data-stu-id="4afa7-112">PARAMETERS</span></span>

### <span data-ttu-id="4afa7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4afa7-113">-Force</span></span>
<span data-ttu-id="4afa7-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4afa7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4afa7-115">-位置</span><span class="sxs-lookup"><span data-stu-id="4afa7-115">-Location</span></span>
<span data-ttu-id="4afa7-116">ExpressRoute 電路所在之 Azure 位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4afa7-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="4afa7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4afa7-117">-Name</span></span>
<span data-ttu-id="4afa7-118">要移動之 ExpressRoute 電路的名稱。</span><span class="sxs-lookup"><span data-stu-id="4afa7-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="4afa7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afa7-119">-ResourceGroupName</span></span>
<span data-ttu-id="4afa7-120">包含要移動 ExpressRoute 電路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4afa7-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="4afa7-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="4afa7-121">-ServiceKey</span></span>
<span data-ttu-id="4afa7-122">在傳統部署模型中，ExpressRoute 回路所使用的服務金鑰。</span><span class="sxs-lookup"><span data-stu-id="4afa7-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="4afa7-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4afa7-123">-Tag</span></span>
<span data-ttu-id="4afa7-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="4afa7-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4afa7-125">例如：</span><span class="sxs-lookup"><span data-stu-id="4afa7-125">For example:</span></span>

<span data-ttu-id="4afa7-126">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4afa7-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4afa7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4afa7-127">-Confirm</span></span>
<span data-ttu-id="4afa7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4afa7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afa7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afa7-129">-WhatIf</span></span>
<span data-ttu-id="4afa7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4afa7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afa7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4afa7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afa7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afa7-132">-DefaultProfile</span></span>
<span data-ttu-id="4afa7-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4afa7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4afa7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afa7-134">CommonParameters</span></span>
<span data-ttu-id="4afa7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4afa7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afa7-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4afa7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afa7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4afa7-137">INPUTS</span></span>

## <span data-ttu-id="4afa7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4afa7-138">OUTPUTS</span></span>

### <span data-ttu-id="4afa7-139">PSExpressRouteCircuit 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4afa7-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4afa7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4afa7-140">NOTES</span></span>

## <span data-ttu-id="4afa7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4afa7-141">RELATED LINKS</span></span>

[<span data-ttu-id="4afa7-142">AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4afa7-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4afa7-143">新-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4afa7-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4afa7-144">移除-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4afa7-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4afa7-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4afa7-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
