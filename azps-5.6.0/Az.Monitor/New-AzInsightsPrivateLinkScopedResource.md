---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916614"
---
# <span data-ttu-id="c153d-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="c153d-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="c153d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c153d-102">SYNOPSIS</span></span>
<span data-ttu-id="c153d-103">建立私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="c153d-103">create for private link scoped resource</span></span>

## <span data-ttu-id="c153d-104">語法</span><span class="sxs-lookup"><span data-stu-id="c153d-104">SYNTAX</span></span>

### <span data-ttu-id="c153d-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c153d-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c153d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c153d-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c153d-107">描述</span><span class="sxs-lookup"><span data-stu-id="c153d-107">DESCRIPTION</span></span>
<span data-ttu-id="c153d-108">建立私人連結範圍資源，範圍資源可以是 Log Analytics 工作區或應用程式深入解析元件</span><span class="sxs-lookup"><span data-stu-id="c153d-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="c153d-109">例子</span><span class="sxs-lookup"><span data-stu-id="c153d-109">EXAMPLES</span></span>

### <span data-ttu-id="c153d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c153d-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="c153d-111">建立範圍資源 "scoped_resource_name" 連結至應用程式深入資訊元件 "ai_name"</span><span class="sxs-lookup"><span data-stu-id="c153d-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="c153d-112">參數</span><span class="sxs-lookup"><span data-stu-id="c153d-112">PARAMETERS</span></span>

### <span data-ttu-id="c153d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c153d-113">-DefaultProfile</span></span>
<span data-ttu-id="c153d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c153d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c153d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c153d-115">-InputObject</span></span>
<span data-ttu-id="c153d-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c153d-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="c153d-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="c153d-117">-LinkedResourceId</span></span>
<span data-ttu-id="c153d-118">LA/AI 資源識別碼連結</span><span class="sxs-lookup"><span data-stu-id="c153d-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c153d-119">-Name</span></span>
<span data-ttu-id="c153d-120">範圍資源名稱</span><span class="sxs-lookup"><span data-stu-id="c153d-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c153d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c153d-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="c153d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="c153d-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="c153d-123">-ScopeName</span></span>
<span data-ttu-id="c153d-124">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="c153d-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="c153d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c153d-125">-Confirm</span></span>
<span data-ttu-id="c153d-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c153d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c153d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c153d-127">-WhatIf</span></span>
<span data-ttu-id="c153d-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c153d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c153d-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c153d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c153d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c153d-130">CommonParameters</span></span>
<span data-ttu-id="c153d-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c153d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c153d-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c153d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c153d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c153d-133">INPUTS</span></span>

### <span data-ttu-id="c153d-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c153d-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="c153d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c153d-135">System.String</span></span>

## <span data-ttu-id="c153d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c153d-136">OUTPUTS</span></span>

### <span data-ttu-id="c153d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="c153d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="c153d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c153d-138">NOTES</span></span>

## <span data-ttu-id="c153d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c153d-139">RELATED LINKS</span></span>
