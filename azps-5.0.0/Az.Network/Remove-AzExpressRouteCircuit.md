---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141090"
---
# <span data-ttu-id="0f51b-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f51b-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="0f51b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f51b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f51b-103">移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="0f51b-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0f51b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f51b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f51b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f51b-105">DESCRIPTION</span></span>
<span data-ttu-id="0f51b-106">**AzExpressRouteCircuit** Cmdlet 會移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="0f51b-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0f51b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f51b-107">EXAMPLES</span></span>

### <span data-ttu-id="0f51b-108">範例1：刪除 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="0f51b-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="0f51b-109">範例2：使用管線刪除 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="0f51b-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="0f51b-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f51b-110">PARAMETERS</span></span>

### <span data-ttu-id="0f51b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f51b-111">-AsJob</span></span>
<span data-ttu-id="0f51b-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0f51b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f51b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f51b-113">-DefaultProfile</span></span>
<span data-ttu-id="0f51b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f51b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f51b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0f51b-115">-Force</span></span>
<span data-ttu-id="0f51b-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0f51b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f51b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f51b-117">-Name</span></span>
<span data-ttu-id="0f51b-118">要移除的 ExpressRoute 電路名稱。</span><span class="sxs-lookup"><span data-stu-id="0f51b-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="0f51b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f51b-119">-PassThru</span></span>
<span data-ttu-id="0f51b-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="0f51b-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0f51b-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="0f51b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f51b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f51b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f51b-123">指定此 ExpressRoute 線路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f51b-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="0f51b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="0f51b-124">-Confirm</span></span>
<span data-ttu-id="0f51b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f51b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f51b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f51b-126">-WhatIf</span></span>
<span data-ttu-id="0f51b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f51b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f51b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f51b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f51b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f51b-129">CommonParameters</span></span>
<span data-ttu-id="0f51b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f51b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f51b-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f51b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f51b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0f51b-132">INPUTS</span></span>

### <span data-ttu-id="0f51b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="0f51b-133">System.String</span></span>

## <span data-ttu-id="0f51b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0f51b-134">OUTPUTS</span></span>

### <span data-ttu-id="0f51b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0f51b-135">System.Boolean</span></span>

## <span data-ttu-id="0f51b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0f51b-136">NOTES</span></span>

## <span data-ttu-id="0f51b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f51b-137">RELATED LINKS</span></span>

[<span data-ttu-id="0f51b-138">AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f51b-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f51b-139">移動流覽 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f51b-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f51b-140">新-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f51b-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f51b-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f51b-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
