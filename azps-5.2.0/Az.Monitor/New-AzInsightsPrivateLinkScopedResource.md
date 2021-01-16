---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280334"
---
# <span data-ttu-id="cff04-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cff04-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="cff04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cff04-102">SYNOPSIS</span></span>
<span data-ttu-id="cff04-103">針對私人連結範圍資源建立</span><span class="sxs-lookup"><span data-stu-id="cff04-103">create for private link scoped resource</span></span>

## <span data-ttu-id="cff04-104">句法</span><span class="sxs-lookup"><span data-stu-id="cff04-104">SYNTAX</span></span>

### <span data-ttu-id="cff04-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cff04-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cff04-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cff04-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cff04-107">說明</span><span class="sxs-lookup"><span data-stu-id="cff04-107">DESCRIPTION</span></span>
<span data-ttu-id="cff04-108">針對私人連結範圍資源建立，範圍資源可以是 Log Analytics 工作區或 Application Insights 元件</span><span class="sxs-lookup"><span data-stu-id="cff04-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="cff04-109">示例</span><span class="sxs-lookup"><span data-stu-id="cff04-109">EXAMPLES</span></span>

### <span data-ttu-id="cff04-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cff04-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="cff04-111">建立連結至 application insights 元件 "ai_name" 的範圍資源 "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="cff04-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="cff04-112">參數</span><span class="sxs-lookup"><span data-stu-id="cff04-112">PARAMETERS</span></span>

### <span data-ttu-id="cff04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff04-113">-DefaultProfile</span></span>
<span data-ttu-id="cff04-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cff04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff04-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cff04-115">-InputObject</span></span>
<span data-ttu-id="cff04-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cff04-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="cff04-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="cff04-117">-LinkedResourceId</span></span>
<span data-ttu-id="cff04-118">要連結的 LA/AI 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cff04-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="cff04-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cff04-119">-Name</span></span>
<span data-ttu-id="cff04-120">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="cff04-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="cff04-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff04-121">-ResourceGroupName</span></span>
<span data-ttu-id="cff04-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cff04-122">Resource Group Name</span></span>

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

### <span data-ttu-id="cff04-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="cff04-123">-ScopeName</span></span>
<span data-ttu-id="cff04-124">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="cff04-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="cff04-125">-確認</span><span class="sxs-lookup"><span data-stu-id="cff04-125">-Confirm</span></span>
<span data-ttu-id="cff04-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cff04-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff04-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff04-127">-WhatIf</span></span>
<span data-ttu-id="cff04-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cff04-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cff04-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cff04-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff04-130">CommonParameters</span></span>
<span data-ttu-id="cff04-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cff04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff04-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cff04-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff04-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cff04-133">INPUTS</span></span>

### <span data-ttu-id="cff04-134">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="cff04-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="cff04-135">System.object</span><span class="sxs-lookup"><span data-stu-id="cff04-135">System.String</span></span>

## <span data-ttu-id="cff04-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cff04-136">OUTPUTS</span></span>

### <span data-ttu-id="cff04-137">PSMonitorPrivateLinkScopedResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="cff04-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="cff04-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cff04-138">NOTES</span></span>

## <span data-ttu-id="cff04-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cff04-139">RELATED LINKS</span></span>
