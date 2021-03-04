---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910054"
---
# <span data-ttu-id="0aa20-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0aa20-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0aa20-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0aa20-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa20-103">刪除私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0aa20-103">delete private link scope</span></span>

## <span data-ttu-id="0aa20-104">語法</span><span class="sxs-lookup"><span data-stu-id="0aa20-104">SYNTAX</span></span>

### <span data-ttu-id="0aa20-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0aa20-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa20-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aa20-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa20-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aa20-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa20-108">描述</span><span class="sxs-lookup"><span data-stu-id="0aa20-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa20-109">刪除私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0aa20-109">delete private link scope</span></span>

## <span data-ttu-id="0aa20-110">例子</span><span class="sxs-lookup"><span data-stu-id="0aa20-110">EXAMPLES</span></span>

### <span data-ttu-id="0aa20-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0aa20-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0aa20-112">刪除資源群組 "scope_name" 下名稱為 "rg_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0aa20-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="0aa20-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="0aa20-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="0aa20-114">使用資源識別碼刪除私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0aa20-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="0aa20-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="0aa20-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="0aa20-116">刪除包含輸入私人連結範圍物件的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0aa20-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="0aa20-117">參數</span><span class="sxs-lookup"><span data-stu-id="0aa20-117">PARAMETERS</span></span>

### <span data-ttu-id="0aa20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa20-118">-DefaultProfile</span></span>
<span data-ttu-id="0aa20-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aa20-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa20-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aa20-120">-InputObject</span></span>
<span data-ttu-id="0aa20-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0aa20-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="0aa20-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0aa20-122">-Name</span></span>
<span data-ttu-id="0aa20-123">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="0aa20-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0aa20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa20-124">-ResourceGroupName</span></span>
<span data-ttu-id="0aa20-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="0aa20-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0aa20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa20-126">-ResourceId</span></span>
<span data-ttu-id="0aa20-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0aa20-127">Resource Id</span></span>

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

### <span data-ttu-id="0aa20-128">-確認</span><span class="sxs-lookup"><span data-stu-id="0aa20-128">-Confirm</span></span>
<span data-ttu-id="0aa20-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0aa20-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa20-130">-WhatIf</span></span>
<span data-ttu-id="0aa20-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0aa20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa20-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0aa20-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa20-133">CommonParameters</span></span>
<span data-ttu-id="0aa20-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0aa20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa20-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aa20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa20-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0aa20-136">INPUTS</span></span>

### <span data-ttu-id="0aa20-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0aa20-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="0aa20-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0aa20-138">System.String</span></span>

## <span data-ttu-id="0aa20-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0aa20-139">OUTPUTS</span></span>

### <span data-ttu-id="0aa20-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa20-140">System.Boolean</span></span>

## <span data-ttu-id="0aa20-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0aa20-141">NOTES</span></span>

## <span data-ttu-id="0aa20-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aa20-142">RELATED LINKS</span></span>
