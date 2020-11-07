---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1d58fba402f292c0935fc10715e06b323353046c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796730"
---
# <span data-ttu-id="a298e-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a298e-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a298e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a298e-102">SYNOPSIS</span></span>
<span data-ttu-id="a298e-103">更新記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="a298e-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="a298e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a298e-104">SYNTAX</span></span>

### <span data-ttu-id="a298e-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="a298e-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a298e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a298e-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a298e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a298e-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a298e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a298e-108">DESCRIPTION</span></span>
<span data-ttu-id="a298e-109">更新記錄警報規則，此命令只支援更新「Enabled」屬性。</span><span class="sxs-lookup"><span data-stu-id="a298e-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="a298e-110">若要更新其他屬性，請參閱「Set-AzScheduledQueryRule」命令。</span><span class="sxs-lookup"><span data-stu-id="a298e-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="a298e-111">示例</span><span class="sxs-lookup"><span data-stu-id="a298e-111">EXAMPLES</span></span>

### <span data-ttu-id="a298e-112">範例 1-依規則名稱更新</span><span class="sxs-lookup"><span data-stu-id="a298e-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="a298e-113">範例 2-依輸入物件更新</span><span class="sxs-lookup"><span data-stu-id="a298e-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="a298e-114">範例 3-依資源識別碼更新</span><span class="sxs-lookup"><span data-stu-id="a298e-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="a298e-115">參數</span><span class="sxs-lookup"><span data-stu-id="a298e-115">PARAMETERS</span></span>

### <span data-ttu-id="a298e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a298e-116">-DefaultProfile</span></span>
<span data-ttu-id="a298e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a298e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a298e-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="a298e-118">-Enabled</span></span>
<span data-ttu-id="a298e-119">Azure 警示狀態-有效的值-$true、$false</span><span class="sxs-lookup"><span data-stu-id="a298e-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="a298e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a298e-120">-InputObject</span></span>
<span data-ttu-id="a298e-121">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="a298e-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="a298e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a298e-122">-Name</span></span>
<span data-ttu-id="a298e-123">警示名稱</span><span class="sxs-lookup"><span data-stu-id="a298e-123">The alert name</span></span>

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

### <span data-ttu-id="a298e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a298e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a298e-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a298e-125">The resource group name</span></span>

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

### <span data-ttu-id="a298e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a298e-126">-ResourceId</span></span>
<span data-ttu-id="a298e-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a298e-127">The resource Id</span></span>

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

### <span data-ttu-id="a298e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a298e-128">-Confirm</span></span>
<span data-ttu-id="a298e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a298e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a298e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a298e-130">-WhatIf</span></span>
<span data-ttu-id="a298e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a298e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a298e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a298e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a298e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a298e-133">CommonParameters</span></span>
<span data-ttu-id="a298e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a298e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a298e-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a298e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a298e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a298e-136">INPUTS</span></span>

### <span data-ttu-id="a298e-137">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a298e-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="a298e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a298e-138">System.String</span></span>

## <span data-ttu-id="a298e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a298e-139">OUTPUTS</span></span>

### <span data-ttu-id="a298e-140">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a298e-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a298e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a298e-141">NOTES</span></span>

## <span data-ttu-id="a298e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a298e-142">RELATED LINKS</span></span>
