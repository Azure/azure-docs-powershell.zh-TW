---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969626"
---
# <span data-ttu-id="fe8e0-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fe8e0-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="fe8e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8e0-103">私人連結範圍的更新</span><span class="sxs-lookup"><span data-stu-id="fe8e0-103">Update for private link scope</span></span>

## <span data-ttu-id="fe8e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe8e0-104">SYNTAX</span></span>

### <span data-ttu-id="fe8e0-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe8e0-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8e0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8e0-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8e0-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8e0-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe8e0-108">DESCRIPTION</span></span>
<span data-ttu-id="fe8e0-109">私人連結範圍的更新</span><span class="sxs-lookup"><span data-stu-id="fe8e0-109">Update for private link scope</span></span>

## <span data-ttu-id="fe8e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe8e0-110">EXAMPLES</span></span>

### <span data-ttu-id="fe8e0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe8e0-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="fe8e0-112">在資源組 "rg_name" 下，更新名為 "scope_name" 的私人連結範圍，以使用標記 "key： value"</span><span class="sxs-lookup"><span data-stu-id="fe8e0-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="fe8e0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="fe8e0-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="fe8e0-114">更新私人連結範圍與資源識別碼，以使用標記 "key： value"</span><span class="sxs-lookup"><span data-stu-id="fe8e0-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="fe8e0-115">範例3</span><span class="sxs-lookup"><span data-stu-id="fe8e0-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="fe8e0-116">使用輸入私人連結範圍物件更新私人連結範圍，以使用標記 "key： value"</span><span class="sxs-lookup"><span data-stu-id="fe8e0-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="fe8e0-117">參數</span><span class="sxs-lookup"><span data-stu-id="fe8e0-117">PARAMETERS</span></span>

### <span data-ttu-id="fe8e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8e0-118">-DefaultProfile</span></span>
<span data-ttu-id="fe8e0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe8e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8e0-120">-InputObject</span></span>
<span data-ttu-id="fe8e0-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fe8e0-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="fe8e0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe8e0-122">-Name</span></span>
<span data-ttu-id="fe8e0-123">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="fe8e0-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="fe8e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe8e0-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fe8e0-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fe8e0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe8e0-126">-ResourceId</span></span>
<span data-ttu-id="fe8e0-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fe8e0-127">Resource Id</span></span>

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

### <span data-ttu-id="fe8e0-128">-標記</span><span class="sxs-lookup"><span data-stu-id="fe8e0-128">-Tags</span></span>
<span data-ttu-id="fe8e0-129">間</span><span class="sxs-lookup"><span data-stu-id="fe8e0-129">Tags</span></span>

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

### <span data-ttu-id="fe8e0-130">-確認</span><span class="sxs-lookup"><span data-stu-id="fe8e0-130">-Confirm</span></span>
<span data-ttu-id="fe8e0-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8e0-132">-WhatIf</span></span>
<span data-ttu-id="fe8e0-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8e0-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8e0-135">CommonParameters</span></span>
<span data-ttu-id="fe8e0-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8e0-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8e0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fe8e0-138">INPUTS</span></span>

### <span data-ttu-id="fe8e0-139">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="fe8e0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fe8e0-140">System.String</span></span>

## <span data-ttu-id="fe8e0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="fe8e0-141">OUTPUTS</span></span>

### <span data-ttu-id="fe8e0-142">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="fe8e0-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="fe8e0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fe8e0-143">NOTES</span></span>

## <span data-ttu-id="fe8e0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe8e0-144">RELATED LINKS</span></span>
