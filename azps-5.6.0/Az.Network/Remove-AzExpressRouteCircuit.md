---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 94730c362ae9854179525212971dda5c2ad1feae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913461"
---
# <span data-ttu-id="55828-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55828-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="55828-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55828-102">SYNOPSIS</span></span>
<span data-ttu-id="55828-103">移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="55828-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="55828-104">語法</span><span class="sxs-lookup"><span data-stu-id="55828-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55828-105">描述</span><span class="sxs-lookup"><span data-stu-id="55828-105">DESCRIPTION</span></span>
<span data-ttu-id="55828-106">**Remove-AzExpressRouteCircuit Cmdlet** 會移除 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="55828-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="55828-107">例子</span><span class="sxs-lookup"><span data-stu-id="55828-107">EXAMPLES</span></span>

### <span data-ttu-id="55828-108">範例 1：刪除 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="55828-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="55828-109">範例 2：使用管線刪除 ExpressRoute 回路</span><span class="sxs-lookup"><span data-stu-id="55828-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="55828-110">參數</span><span class="sxs-lookup"><span data-stu-id="55828-110">PARAMETERS</span></span>

### <span data-ttu-id="55828-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55828-111">-AsJob</span></span>
<span data-ttu-id="55828-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55828-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55828-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55828-113">-DefaultProfile</span></span>
<span data-ttu-id="55828-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55828-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55828-115">-強制</span><span class="sxs-lookup"><span data-stu-id="55828-115">-Force</span></span>
<span data-ttu-id="55828-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="55828-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55828-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="55828-117">-Name</span></span>
<span data-ttu-id="55828-118">要移除的 ExpressRoute 回路名稱。</span><span class="sxs-lookup"><span data-stu-id="55828-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="55828-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55828-119">-PassThru</span></span>
<span data-ttu-id="55828-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="55828-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="55828-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="55828-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55828-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55828-122">-ResourceGroupName</span></span>
<span data-ttu-id="55828-123">指定此 ExpressRoute 回路所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="55828-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="55828-124">-確認</span><span class="sxs-lookup"><span data-stu-id="55828-124">-Confirm</span></span>
<span data-ttu-id="55828-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55828-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55828-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55828-126">-WhatIf</span></span>
<span data-ttu-id="55828-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55828-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55828-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55828-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55828-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55828-129">CommonParameters</span></span>
<span data-ttu-id="55828-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55828-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55828-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55828-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55828-132">輸入</span><span class="sxs-lookup"><span data-stu-id="55828-132">INPUTS</span></span>

### <span data-ttu-id="55828-133">System.String</span><span class="sxs-lookup"><span data-stu-id="55828-133">System.String</span></span>

## <span data-ttu-id="55828-134">輸出</span><span class="sxs-lookup"><span data-stu-id="55828-134">OUTPUTS</span></span>

### <span data-ttu-id="55828-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55828-135">System.Boolean</span></span>

## <span data-ttu-id="55828-136">筆記</span><span class="sxs-lookup"><span data-stu-id="55828-136">NOTES</span></span>

## <span data-ttu-id="55828-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="55828-137">RELATED LINKS</span></span>

[<span data-ttu-id="55828-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55828-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="55828-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55828-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="55828-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55828-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="55828-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="55828-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
