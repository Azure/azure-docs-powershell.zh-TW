---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 83f4fae326920b24d272ae87341c20702a2bf8fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915390"
---
# <span data-ttu-id="d1927-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d1927-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="d1927-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1927-102">SYNOPSIS</span></span>
<span data-ttu-id="d1927-103">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="d1927-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="d1927-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1927-104">SYNTAX</span></span>

### <span data-ttu-id="d1927-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d1927-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1927-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1927-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1927-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1927-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1927-108">描述</span><span class="sxs-lookup"><span data-stu-id="d1927-108">DESCRIPTION</span></span>
<span data-ttu-id="d1927-109">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="d1927-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="d1927-110">例子</span><span class="sxs-lookup"><span data-stu-id="d1927-110">EXAMPLES</span></span>

### <span data-ttu-id="d1927-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d1927-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="d1927-112">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="d1927-112">delete private link scoped resource</span></span>

## <span data-ttu-id="d1927-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1927-113">PARAMETERS</span></span>

### <span data-ttu-id="d1927-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1927-114">-DefaultProfile</span></span>
<span data-ttu-id="d1927-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1927-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1927-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1927-116">-InputObject</span></span>
<span data-ttu-id="d1927-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d1927-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d1927-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1927-118">-Name</span></span>
<span data-ttu-id="d1927-119">範圍資源名稱</span><span class="sxs-lookup"><span data-stu-id="d1927-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1927-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1927-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1927-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="d1927-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1927-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1927-122">-ResourceId</span></span>
<span data-ttu-id="d1927-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d1927-123">Resource Id</span></span>

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

### <span data-ttu-id="d1927-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="d1927-124">-ScopeName</span></span>
<span data-ttu-id="d1927-125">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="d1927-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1927-126">-確認</span><span class="sxs-lookup"><span data-stu-id="d1927-126">-Confirm</span></span>
<span data-ttu-id="d1927-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1927-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1927-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1927-128">-WhatIf</span></span>
<span data-ttu-id="d1927-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1927-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1927-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1927-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1927-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1927-131">CommonParameters</span></span>
<span data-ttu-id="d1927-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1927-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1927-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1927-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1927-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d1927-134">INPUTS</span></span>

### <span data-ttu-id="d1927-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d1927-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="d1927-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d1927-136">System.String</span></span>

## <span data-ttu-id="d1927-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d1927-137">OUTPUTS</span></span>

### <span data-ttu-id="d1927-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1927-138">System.Boolean</span></span>

## <span data-ttu-id="d1927-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d1927-139">NOTES</span></span>

## <span data-ttu-id="d1927-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1927-140">RELATED LINKS</span></span>
