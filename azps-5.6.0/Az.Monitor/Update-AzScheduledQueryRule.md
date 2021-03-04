---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8b1658ef2ff2779243d42461f4b94964017a6847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910454"
---
# <span data-ttu-id="c3d43-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c3d43-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="c3d43-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c3d43-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d43-103">更新記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="c3d43-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="c3d43-104">語法</span><span class="sxs-lookup"><span data-stu-id="c3d43-104">SYNTAX</span></span>

### <span data-ttu-id="c3d43-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="c3d43-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d43-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3d43-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d43-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d43-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d43-108">描述</span><span class="sxs-lookup"><span data-stu-id="c3d43-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d43-109">更新記錄提醒規則，此命令僅支援更新 「Enabled」屬性。</span><span class="sxs-lookup"><span data-stu-id="c3d43-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="c3d43-110">若要更新其他屬性，請參閱 [Set-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule) 命令。</span><span class="sxs-lookup"><span data-stu-id="c3d43-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="c3d43-111">例子</span><span class="sxs-lookup"><span data-stu-id="c3d43-111">EXAMPLES</span></span>

### <span data-ttu-id="c3d43-112">範例 1：依規則名稱更新</span><span class="sxs-lookup"><span data-stu-id="c3d43-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c3d43-113">範例 2：按輸入物件更新</span><span class="sxs-lookup"><span data-stu-id="c3d43-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c3d43-114">範例 3：根據資源識別碼更新</span><span class="sxs-lookup"><span data-stu-id="c3d43-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="c3d43-115">參數</span><span class="sxs-lookup"><span data-stu-id="c3d43-115">PARAMETERS</span></span>

### <span data-ttu-id="c3d43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d43-116">-DefaultProfile</span></span>
<span data-ttu-id="c3d43-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3d43-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d43-118">-已啟用</span><span class="sxs-lookup"><span data-stu-id="c3d43-118">-Enabled</span></span>
<span data-ttu-id="c3d43-119">Azure 警示狀態 - 有效的值 - $true，$false</span><span class="sxs-lookup"><span data-stu-id="c3d43-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="c3d43-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d43-120">-InputObject</span></span>
<span data-ttu-id="c3d43-121">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="c3d43-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3d43-122">-Name</span></span>
<span data-ttu-id="c3d43-123">警示名稱</span><span class="sxs-lookup"><span data-stu-id="c3d43-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d43-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3d43-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="c3d43-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d43-126">-ResourceId</span></span>
<span data-ttu-id="c3d43-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c3d43-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d43-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c3d43-128">-Confirm</span></span>
<span data-ttu-id="c3d43-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c3d43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d43-130">-WhatIf</span></span>
<span data-ttu-id="c3d43-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3d43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d43-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3d43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d43-133">CommonParameters</span></span>
<span data-ttu-id="c3d43-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c3d43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d43-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3d43-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d43-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c3d43-136">INPUTS</span></span>

### <span data-ttu-id="c3d43-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c3d43-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="c3d43-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c3d43-138">System.String</span></span>

## <span data-ttu-id="c3d43-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c3d43-139">OUTPUTS</span></span>

### <span data-ttu-id="c3d43-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c3d43-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="c3d43-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c3d43-141">NOTES</span></span>

## <span data-ttu-id="c3d43-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3d43-142">RELATED LINKS</span></span>
