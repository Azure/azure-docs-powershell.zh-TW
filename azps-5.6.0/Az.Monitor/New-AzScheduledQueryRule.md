---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 49863fd8102aef7b0175328edc0b4523f13921d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904377"
---
# <span data-ttu-id="02094-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="02094-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="02094-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02094-102">SYNOPSIS</span></span>
<span data-ttu-id="02094-103">建立記錄提醒規則 (排程查詢規則類型) </span><span class="sxs-lookup"><span data-stu-id="02094-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="02094-104">語法</span><span class="sxs-lookup"><span data-stu-id="02094-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02094-105">描述</span><span class="sxs-lookup"><span data-stu-id="02094-105">DESCRIPTION</span></span>
<span data-ttu-id="02094-106">建立記錄提醒規則 (排程查詢規則類型) </span><span class="sxs-lookup"><span data-stu-id="02094-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="02094-107">例子</span><span class="sxs-lookup"><span data-stu-id="02094-107">EXAMPLES</span></span>

### <span data-ttu-id="02094-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="02094-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="02094-109">參數</span><span class="sxs-lookup"><span data-stu-id="02094-109">PARAMETERS</span></span>

### <span data-ttu-id="02094-110">-動作</span><span class="sxs-lookup"><span data-stu-id="02094-110">-Action</span></span>
<span data-ttu-id="02094-111">已排程查詢規則警示動作</span><span class="sxs-lookup"><span data-stu-id="02094-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02094-112">-AsJob</span></span>
<span data-ttu-id="02094-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02094-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02094-114">-DefaultProfile</span></span>
<span data-ttu-id="02094-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02094-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02094-116">-描述</span><span class="sxs-lookup"><span data-stu-id="02094-116">-Description</span></span>
<span data-ttu-id="02094-117">此通知的描述</span><span class="sxs-lookup"><span data-stu-id="02094-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-118">-已啟用</span><span class="sxs-lookup"><span data-stu-id="02094-118">-Enabled</span></span>
<span data-ttu-id="02094-119">Azure 警示狀態 - 有效的值 - $true，$false</span><span class="sxs-lookup"><span data-stu-id="02094-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-120">-位置</span><span class="sxs-lookup"><span data-stu-id="02094-120">-Location</span></span>
<span data-ttu-id="02094-121">此通知的位置</span><span class="sxs-lookup"><span data-stu-id="02094-121">The location for this alert</span></span>

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

### <span data-ttu-id="02094-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="02094-122">-Name</span></span>
<span data-ttu-id="02094-123">警示名稱</span><span class="sxs-lookup"><span data-stu-id="02094-123">The alert name</span></span>

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

### <span data-ttu-id="02094-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02094-124">-ResourceGroupName</span></span>
<span data-ttu-id="02094-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="02094-125">The resource group name</span></span>

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

### <span data-ttu-id="02094-126">-排程</span><span class="sxs-lookup"><span data-stu-id="02094-126">-Schedule</span></span>
<span data-ttu-id="02094-127">已排程的查詢規則排程</span><span class="sxs-lookup"><span data-stu-id="02094-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-128">-來源</span><span class="sxs-lookup"><span data-stu-id="02094-128">-Source</span></span>
<span data-ttu-id="02094-129">已排程查詢規則來源</span><span class="sxs-lookup"><span data-stu-id="02094-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-130">-標記</span><span class="sxs-lookup"><span data-stu-id="02094-130">-Tag</span></span>
<span data-ttu-id="02094-131">資源標記</span><span class="sxs-lookup"><span data-stu-id="02094-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02094-132">-確認</span><span class="sxs-lookup"><span data-stu-id="02094-132">-Confirm</span></span>
<span data-ttu-id="02094-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02094-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02094-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02094-134">-WhatIf</span></span>
<span data-ttu-id="02094-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02094-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02094-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02094-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02094-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02094-137">CommonParameters</span></span>
<span data-ttu-id="02094-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02094-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02094-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02094-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02094-140">輸入</span><span class="sxs-lookup"><span data-stu-id="02094-140">INPUTS</span></span>

### <span data-ttu-id="02094-141">System.String</span><span class="sxs-lookup"><span data-stu-id="02094-141">System.String</span></span>

## <span data-ttu-id="02094-142">輸出</span><span class="sxs-lookup"><span data-stu-id="02094-142">OUTPUTS</span></span>

### <span data-ttu-id="02094-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="02094-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="02094-144">筆記</span><span class="sxs-lookup"><span data-stu-id="02094-144">NOTES</span></span>

## <span data-ttu-id="02094-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="02094-145">RELATED LINKS</span></span>
