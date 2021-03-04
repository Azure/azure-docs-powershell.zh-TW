---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905362"
---
# <span data-ttu-id="68431-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="68431-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="68431-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68431-102">SYNOPSIS</span></span>
<span data-ttu-id="68431-103">私人連結範圍的更新</span><span class="sxs-lookup"><span data-stu-id="68431-103">Update for private link scope</span></span>

## <span data-ttu-id="68431-104">語法</span><span class="sxs-lookup"><span data-stu-id="68431-104">SYNTAX</span></span>

### <span data-ttu-id="68431-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68431-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68431-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68431-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68431-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68431-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68431-108">描述</span><span class="sxs-lookup"><span data-stu-id="68431-108">DESCRIPTION</span></span>
<span data-ttu-id="68431-109">私人連結範圍的更新</span><span class="sxs-lookup"><span data-stu-id="68431-109">Update for private link scope</span></span>

## <span data-ttu-id="68431-110">例子</span><span class="sxs-lookup"><span data-stu-id="68431-110">EXAMPLES</span></span>

### <span data-ttu-id="68431-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="68431-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="68431-112">在資源群組 "scope_name" 下更新名稱為 "rg_name" 的私人連結範圍，以使用標記 "key：value"</span><span class="sxs-lookup"><span data-stu-id="68431-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="68431-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="68431-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="68431-114">使用資源識別碼更新私人連結範圍，以使用標記 "key：value"</span><span class="sxs-lookup"><span data-stu-id="68431-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="68431-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="68431-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="68431-116">使用輸入私人連結範圍物件更新私人連結範圍，以使用標記 "key：value"</span><span class="sxs-lookup"><span data-stu-id="68431-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="68431-117">參數</span><span class="sxs-lookup"><span data-stu-id="68431-117">PARAMETERS</span></span>

### <span data-ttu-id="68431-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68431-118">-DefaultProfile</span></span>
<span data-ttu-id="68431-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68431-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68431-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68431-120">-InputObject</span></span>
<span data-ttu-id="68431-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="68431-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="68431-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="68431-122">-Name</span></span>
<span data-ttu-id="68431-123">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="68431-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="68431-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68431-124">-ResourceGroupName</span></span>
<span data-ttu-id="68431-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="68431-125">Resource Group Name</span></span>

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

### <span data-ttu-id="68431-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68431-126">-ResourceId</span></span>
<span data-ttu-id="68431-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="68431-127">Resource Id</span></span>

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

### <span data-ttu-id="68431-128">-標記</span><span class="sxs-lookup"><span data-stu-id="68431-128">-Tags</span></span>
<span data-ttu-id="68431-129">標籤</span><span class="sxs-lookup"><span data-stu-id="68431-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68431-130">-確認</span><span class="sxs-lookup"><span data-stu-id="68431-130">-Confirm</span></span>
<span data-ttu-id="68431-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="68431-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68431-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68431-132">-WhatIf</span></span>
<span data-ttu-id="68431-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68431-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68431-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68431-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68431-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68431-135">CommonParameters</span></span>
<span data-ttu-id="68431-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68431-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68431-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68431-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68431-138">輸入</span><span class="sxs-lookup"><span data-stu-id="68431-138">INPUTS</span></span>

### <span data-ttu-id="68431-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="68431-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="68431-140">System.String</span><span class="sxs-lookup"><span data-stu-id="68431-140">System.String</span></span>

## <span data-ttu-id="68431-141">輸出</span><span class="sxs-lookup"><span data-stu-id="68431-141">OUTPUTS</span></span>

### <span data-ttu-id="68431-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="68431-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="68431-143">筆記</span><span class="sxs-lookup"><span data-stu-id="68431-143">NOTES</span></span>

## <span data-ttu-id="68431-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="68431-144">RELATED LINKS</span></span>
