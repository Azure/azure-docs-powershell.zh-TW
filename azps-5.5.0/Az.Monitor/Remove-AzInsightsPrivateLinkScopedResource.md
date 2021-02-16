---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129070"
---
# <span data-ttu-id="a4e48-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a4e48-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a4e48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4e48-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e48-103">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="a4e48-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="a4e48-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4e48-104">SYNTAX</span></span>

### <span data-ttu-id="a4e48-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4e48-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4e48-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4e48-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4e48-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4e48-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4e48-108">說明</span><span class="sxs-lookup"><span data-stu-id="a4e48-108">DESCRIPTION</span></span>
<span data-ttu-id="a4e48-109">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="a4e48-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="a4e48-110">示例</span><span class="sxs-lookup"><span data-stu-id="a4e48-110">EXAMPLES</span></span>

### <span data-ttu-id="a4e48-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a4e48-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="a4e48-112">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="a4e48-112">delete private link scoped resource</span></span>

## <span data-ttu-id="a4e48-113">參數</span><span class="sxs-lookup"><span data-stu-id="a4e48-113">PARAMETERS</span></span>

### <span data-ttu-id="a4e48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e48-114">-DefaultProfile</span></span>
<span data-ttu-id="a4e48-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4e48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4e48-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4e48-116">-InputObject</span></span>
<span data-ttu-id="a4e48-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a4e48-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="a4e48-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4e48-118">-Name</span></span>
<span data-ttu-id="a4e48-119">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="a4e48-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="a4e48-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e48-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4e48-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a4e48-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a4e48-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4e48-122">-ResourceId</span></span>
<span data-ttu-id="a4e48-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a4e48-123">Resource Id</span></span>

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

### <span data-ttu-id="a4e48-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="a4e48-124">-ScopeName</span></span>
<span data-ttu-id="a4e48-125">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="a4e48-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a4e48-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a4e48-126">-Confirm</span></span>
<span data-ttu-id="a4e48-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4e48-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e48-128">-WhatIf</span></span>
<span data-ttu-id="a4e48-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4e48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4e48-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4e48-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e48-131">CommonParameters</span></span>
<span data-ttu-id="a4e48-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4e48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e48-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4e48-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e48-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a4e48-134">INPUTS</span></span>

### <span data-ttu-id="a4e48-135">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a4e48-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="a4e48-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a4e48-136">System.String</span></span>

## <span data-ttu-id="a4e48-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a4e48-137">OUTPUTS</span></span>

### <span data-ttu-id="a4e48-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a4e48-138">System.Boolean</span></span>

## <span data-ttu-id="a4e48-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a4e48-139">NOTES</span></span>

## <span data-ttu-id="a4e48-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4e48-140">RELATED LINKS</span></span>
