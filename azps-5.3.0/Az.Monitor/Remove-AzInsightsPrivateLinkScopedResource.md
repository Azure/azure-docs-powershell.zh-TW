---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436944"
---
# <span data-ttu-id="9443a-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="9443a-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="9443a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9443a-102">SYNOPSIS</span></span>
<span data-ttu-id="9443a-103">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="9443a-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="9443a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9443a-104">SYNTAX</span></span>

### <span data-ttu-id="9443a-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9443a-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9443a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9443a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9443a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9443a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9443a-108">說明</span><span class="sxs-lookup"><span data-stu-id="9443a-108">DESCRIPTION</span></span>
<span data-ttu-id="9443a-109">針對私人連結範圍資源刪除</span><span class="sxs-lookup"><span data-stu-id="9443a-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="9443a-110">示例</span><span class="sxs-lookup"><span data-stu-id="9443a-110">EXAMPLES</span></span>

### <span data-ttu-id="9443a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9443a-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="9443a-112">刪除私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="9443a-112">delete private link scoped resource</span></span>

## <span data-ttu-id="9443a-113">參數</span><span class="sxs-lookup"><span data-stu-id="9443a-113">PARAMETERS</span></span>

### <span data-ttu-id="9443a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9443a-114">-DefaultProfile</span></span>
<span data-ttu-id="9443a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9443a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9443a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9443a-116">-InputObject</span></span>
<span data-ttu-id="9443a-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9443a-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="9443a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9443a-118">-Name</span></span>
<span data-ttu-id="9443a-119">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="9443a-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="9443a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9443a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9443a-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9443a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9443a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9443a-122">-ResourceId</span></span>
<span data-ttu-id="9443a-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9443a-123">Resource Id</span></span>

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

### <span data-ttu-id="9443a-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="9443a-124">-ScopeName</span></span>
<span data-ttu-id="9443a-125">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="9443a-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="9443a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9443a-126">-Confirm</span></span>
<span data-ttu-id="9443a-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9443a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9443a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9443a-128">-WhatIf</span></span>
<span data-ttu-id="9443a-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9443a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9443a-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9443a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9443a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9443a-131">CommonParameters</span></span>
<span data-ttu-id="9443a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9443a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9443a-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9443a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9443a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9443a-134">INPUTS</span></span>

### <span data-ttu-id="9443a-135">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="9443a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="9443a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9443a-136">System.String</span></span>

## <span data-ttu-id="9443a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9443a-137">OUTPUTS</span></span>

### <span data-ttu-id="9443a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="9443a-138">System.Boolean</span></span>

## <span data-ttu-id="9443a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9443a-139">NOTES</span></span>

## <span data-ttu-id="9443a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9443a-140">RELATED LINKS</span></span>
