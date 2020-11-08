---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127736"
---
# <span data-ttu-id="e4d20-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e4d20-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="e4d20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4d20-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d20-103">刪除私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="e4d20-103">delete private link scope</span></span>

## <span data-ttu-id="e4d20-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4d20-104">SYNTAX</span></span>

### <span data-ttu-id="e4d20-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e4d20-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d20-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d20-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d20-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d20-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d20-108">說明</span><span class="sxs-lookup"><span data-stu-id="e4d20-108">DESCRIPTION</span></span>
<span data-ttu-id="e4d20-109">刪除私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="e4d20-109">delete private link scope</span></span>

## <span data-ttu-id="e4d20-110">示例</span><span class="sxs-lookup"><span data-stu-id="e4d20-110">EXAMPLES</span></span>

### <span data-ttu-id="e4d20-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e4d20-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="e4d20-112">在資源群組 "rg_name" 下，刪除名稱為 "scope_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="e4d20-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="e4d20-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e4d20-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="e4d20-114">刪除含資源識別碼的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="e4d20-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="e4d20-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e4d20-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="e4d20-116">刪除含輸入私人連結範圍物件的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="e4d20-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="e4d20-117">參數</span><span class="sxs-lookup"><span data-stu-id="e4d20-117">PARAMETERS</span></span>

### <span data-ttu-id="e4d20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d20-118">-DefaultProfile</span></span>
<span data-ttu-id="e4d20-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4d20-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d20-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4d20-120">-InputObject</span></span>
<span data-ttu-id="e4d20-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e4d20-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4d20-122">-Name</span></span>
<span data-ttu-id="e4d20-123">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="e4d20-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d20-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4d20-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e4d20-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4d20-126">-ResourceId</span></span>
<span data-ttu-id="e4d20-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e4d20-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e4d20-128">-Confirm</span></span>
<span data-ttu-id="e4d20-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4d20-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d20-130">-WhatIf</span></span>
<span data-ttu-id="e4d20-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4d20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d20-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4d20-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d20-133">CommonParameters</span></span>
<span data-ttu-id="e4d20-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4d20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d20-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e4d20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d20-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e4d20-136">INPUTS</span></span>

### <span data-ttu-id="e4d20-137">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e4d20-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e4d20-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e4d20-138">System.String</span></span>

## <span data-ttu-id="e4d20-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e4d20-139">OUTPUTS</span></span>

### <span data-ttu-id="e4d20-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e4d20-140">System.Boolean</span></span>

## <span data-ttu-id="e4d20-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e4d20-141">NOTES</span></span>

## <span data-ttu-id="e4d20-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4d20-142">RELATED LINKS</span></span>