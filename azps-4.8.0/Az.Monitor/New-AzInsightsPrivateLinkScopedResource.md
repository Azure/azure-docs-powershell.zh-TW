---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135873"
---
# <span data-ttu-id="98e7d-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="98e7d-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="98e7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="98e7d-103">針對私人連結範圍資源建立</span><span class="sxs-lookup"><span data-stu-id="98e7d-103">create for private link scoped resource</span></span>

## <span data-ttu-id="98e7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="98e7d-104">SYNTAX</span></span>

### <span data-ttu-id="98e7d-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="98e7d-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98e7d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e7d-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98e7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="98e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="98e7d-108">針對私人連結範圍資源建立，範圍資源可以是 Log Analytics 工作區或 Application Insights 元件</span><span class="sxs-lookup"><span data-stu-id="98e7d-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="98e7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="98e7d-109">EXAMPLES</span></span>

### <span data-ttu-id="98e7d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="98e7d-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="98e7d-111">建立連結至 application insights 元件 "ai_name" 的範圍資源 "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="98e7d-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="98e7d-112">參數</span><span class="sxs-lookup"><span data-stu-id="98e7d-112">PARAMETERS</span></span>

### <span data-ttu-id="98e7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e7d-113">-DefaultProfile</span></span>
<span data-ttu-id="98e7d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98e7d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e7d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98e7d-115">-InputObject</span></span>
<span data-ttu-id="98e7d-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="98e7d-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="98e7d-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="98e7d-117">-LinkedResourceId</span></span>
<span data-ttu-id="98e7d-118">要連結的 LA/AI 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="98e7d-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="98e7d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="98e7d-119">-Name</span></span>
<span data-ttu-id="98e7d-120">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="98e7d-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="98e7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="98e7d-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="98e7d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="98e7d-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="98e7d-123">-ScopeName</span></span>
<span data-ttu-id="98e7d-124">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="98e7d-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="98e7d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="98e7d-125">-Confirm</span></span>
<span data-ttu-id="98e7d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98e7d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e7d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e7d-127">-WhatIf</span></span>
<span data-ttu-id="98e7d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98e7d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e7d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98e7d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e7d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e7d-130">CommonParameters</span></span>
<span data-ttu-id="98e7d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98e7d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e7d-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98e7d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e7d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98e7d-133">INPUTS</span></span>

### <span data-ttu-id="98e7d-134">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="98e7d-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="98e7d-135">System.object</span><span class="sxs-lookup"><span data-stu-id="98e7d-135">System.String</span></span>

## <span data-ttu-id="98e7d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="98e7d-136">OUTPUTS</span></span>

### <span data-ttu-id="98e7d-137">PSMonitorPrivateLinkScopedResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="98e7d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="98e7d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="98e7d-138">NOTES</span></span>

## <span data-ttu-id="98e7d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="98e7d-139">RELATED LINKS</span></span>
