---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127559"
---
# <span data-ttu-id="c2a3f-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="c2a3f-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="c2a3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a3f-103">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="c2a3f-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="c2a3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2a3f-104">SYNTAX</span></span>

### <span data-ttu-id="c2a3f-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2a3f-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2a3f-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a3f-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2a3f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a3f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a3f-108">說明</span><span class="sxs-lookup"><span data-stu-id="c2a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="c2a3f-109">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="c2a3f-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="c2a3f-110">示例</span><span class="sxs-lookup"><span data-stu-id="c2a3f-110">EXAMPLES</span></span>

### <span data-ttu-id="c2a3f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c2a3f-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="c2a3f-112">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="c2a3f-112">delete private link scoped resource</span></span>

## <span data-ttu-id="c2a3f-113">參數</span><span class="sxs-lookup"><span data-stu-id="c2a3f-113">PARAMETERS</span></span>

### <span data-ttu-id="c2a3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a3f-114">-DefaultProfile</span></span>
<span data-ttu-id="c2a3f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a3f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2a3f-116">-InputObject</span></span>
<span data-ttu-id="c2a3f-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c2a3f-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="c2a3f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2a3f-118">-Name</span></span>
<span data-ttu-id="c2a3f-119">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="c2a3f-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="c2a3f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a3f-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2a3f-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c2a3f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c2a3f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a3f-122">-ResourceId</span></span>
<span data-ttu-id="c2a3f-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2a3f-123">Resource Id</span></span>

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

### <span data-ttu-id="c2a3f-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="c2a3f-124">-ScopeName</span></span>
<span data-ttu-id="c2a3f-125">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="c2a3f-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="c2a3f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c2a3f-126">-Confirm</span></span>
<span data-ttu-id="c2a3f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a3f-128">-WhatIf</span></span>
<span data-ttu-id="c2a3f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a3f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a3f-131">CommonParameters</span></span>
<span data-ttu-id="c2a3f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a3f-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a3f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c2a3f-134">INPUTS</span></span>

### <span data-ttu-id="c2a3f-135">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="c2a3f-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="c2a3f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c2a3f-136">System.String</span></span>

## <span data-ttu-id="c2a3f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c2a3f-137">OUTPUTS</span></span>

### <span data-ttu-id="c2a3f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c2a3f-138">System.Boolean</span></span>

## <span data-ttu-id="c2a3f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c2a3f-139">NOTES</span></span>

## <span data-ttu-id="c2a3f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2a3f-140">RELATED LINKS</span></span>