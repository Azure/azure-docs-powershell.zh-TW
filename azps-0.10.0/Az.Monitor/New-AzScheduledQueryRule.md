---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: cbaf71a19d0fb823fd44040d34fcde5d68c7c2c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794588"
---
# <span data-ttu-id="f9858-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9858-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f9858-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9858-102">SYNOPSIS</span></span>
<span data-ttu-id="f9858-103"> (排程的查詢規則類型建立記錄警報規則) </span><span class="sxs-lookup"><span data-stu-id="f9858-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f9858-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9858-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9858-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9858-105">DESCRIPTION</span></span>
<span data-ttu-id="f9858-106"> (排程的查詢規則類型建立記錄警報規則) </span><span class="sxs-lookup"><span data-stu-id="f9858-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f9858-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9858-107">EXAMPLES</span></span>

### <span data-ttu-id="f9858-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f9858-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="f9858-109">參數</span><span class="sxs-lookup"><span data-stu-id="f9858-109">PARAMETERS</span></span>

### <span data-ttu-id="f9858-110">-動作</span><span class="sxs-lookup"><span data-stu-id="f9858-110">-Action</span></span>
<span data-ttu-id="f9858-111">[排程查詢規則] 警示動作</span><span class="sxs-lookup"><span data-stu-id="f9858-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="f9858-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9858-112">-AsJob</span></span>
<span data-ttu-id="f9858-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9858-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9858-114">-DefaultProfile</span></span>
<span data-ttu-id="f9858-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9858-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9858-116">-描述</span><span class="sxs-lookup"><span data-stu-id="f9858-116">-Description</span></span>
<span data-ttu-id="f9858-117">此提醒的描述</span><span class="sxs-lookup"><span data-stu-id="f9858-117">The description for this alert</span></span>

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

### <span data-ttu-id="f9858-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="f9858-118">-Enabled</span></span>
<span data-ttu-id="f9858-119">Azure 警示狀態-有效的值-$true、$false</span><span class="sxs-lookup"><span data-stu-id="f9858-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="f9858-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f9858-120">-Location</span></span>
<span data-ttu-id="f9858-121">此提醒的位置</span><span class="sxs-lookup"><span data-stu-id="f9858-121">The location for this alert</span></span>

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

### <span data-ttu-id="f9858-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9858-122">-Name</span></span>
<span data-ttu-id="f9858-123">警示名稱</span><span class="sxs-lookup"><span data-stu-id="f9858-123">The alert name</span></span>

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

### <span data-ttu-id="f9858-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9858-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9858-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f9858-125">The resource group name</span></span>

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

### <span data-ttu-id="f9858-126">-排程</span><span class="sxs-lookup"><span data-stu-id="f9858-126">-Schedule</span></span>
<span data-ttu-id="f9858-127">排程查詢規則排程</span><span class="sxs-lookup"><span data-stu-id="f9858-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="f9858-128">-來源</span><span class="sxs-lookup"><span data-stu-id="f9858-128">-Source</span></span>
<span data-ttu-id="f9858-129">排程查詢規則來源</span><span class="sxs-lookup"><span data-stu-id="f9858-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="f9858-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9858-130">-Tag</span></span>
<span data-ttu-id="f9858-131">資源標記</span><span class="sxs-lookup"><span data-stu-id="f9858-131">Resource tags</span></span>

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

### <span data-ttu-id="f9858-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f9858-132">-Confirm</span></span>
<span data-ttu-id="f9858-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9858-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9858-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9858-134">-WhatIf</span></span>
<span data-ttu-id="f9858-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9858-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9858-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9858-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9858-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9858-137">CommonParameters</span></span>
<span data-ttu-id="f9858-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9858-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9858-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9858-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9858-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f9858-140">INPUTS</span></span>

### <span data-ttu-id="f9858-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f9858-141">System.String</span></span>

## <span data-ttu-id="f9858-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f9858-142">OUTPUTS</span></span>

### <span data-ttu-id="f9858-143">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="f9858-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f9858-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f9858-144">NOTES</span></span>

## <span data-ttu-id="f9858-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9858-145">RELATED LINKS</span></span>
