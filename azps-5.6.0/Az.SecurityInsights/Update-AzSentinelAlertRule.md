---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906393"
---
# <span data-ttu-id="a5917-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a5917-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="a5917-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5917-102">SYNOPSIS</span></span>
<span data-ttu-id="a5917-103">建立分析 (警示規則) 。</span><span class="sxs-lookup"><span data-stu-id="a5917-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="a5917-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5917-104">SYNTAX</span></span>

### <span data-ttu-id="a5917-105">AlertRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="a5917-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5917-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a5917-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5917-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5917-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5917-108">描述</span><span class="sxs-lookup"><span data-stu-id="a5917-108">DESCRIPTION</span></span>
<span data-ttu-id="a5917-109">**Update-AzSentinelAlertRule** Cmdlet 會更新 (工作區) 警示規則。</span><span class="sxs-lookup"><span data-stu-id="a5917-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="a5917-110">您可以使用 -InputObject 或 -ResourceId 或 -AlertId。</span><span class="sxs-lookup"><span data-stu-id="a5917-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="a5917-111">您可以更新 1 或更多的帕mater。</span><span class="sxs-lookup"><span data-stu-id="a5917-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="a5917-112">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5917-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="a5917-113">例子</span><span class="sxs-lookup"><span data-stu-id="a5917-113">EXAMPLES</span></span>

### <span data-ttu-id="a5917-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5917-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="a5917-115">此範例會更新 **AlertRule** 將其設定 *為停用，* 並重新命名為 *Disabled-AlertRuleDisplayName。*</span><span class="sxs-lookup"><span data-stu-id="a5917-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="a5917-116">所有其他屬性會維持不變。</span><span class="sxs-lookup"><span data-stu-id="a5917-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="a5917-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="a5917-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="a5917-118">此範例會使用 InputObject 將通知規則設定為 *停用來更新 AlertRule。* </span><span class="sxs-lookup"><span data-stu-id="a5917-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="a5917-119">所有其他屬性會維持不變。</span><span class="sxs-lookup"><span data-stu-id="a5917-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="a5917-120">參數</span><span class="sxs-lookup"><span data-stu-id="a5917-120">PARAMETERS</span></span>

### <span data-ttu-id="a5917-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a5917-121">-AlertRuleId</span></span>
<span data-ttu-id="a5917-122">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5917-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="a5917-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="a5917-124">警示規則範本。</span><span class="sxs-lookup"><span data-stu-id="a5917-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5917-125">-DefaultProfile</span></span>
<span data-ttu-id="a5917-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5917-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-127">-描述</span><span class="sxs-lookup"><span data-stu-id="a5917-127">-Description</span></span>
<span data-ttu-id="a5917-128">描述。</span><span class="sxs-lookup"><span data-stu-id="a5917-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-129">-已停用</span><span class="sxs-lookup"><span data-stu-id="a5917-129">-Disabled</span></span>
<span data-ttu-id="a5917-130">警示規則已停用。</span><span class="sxs-lookup"><span data-stu-id="a5917-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a5917-131">-DisplayName</span></span>
<span data-ttu-id="a5917-132">警示規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a5917-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="a5917-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="a5917-134">警示規則顯示名稱排除篩選。</span><span class="sxs-lookup"><span data-stu-id="a5917-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="a5917-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="a5917-136">警示規則顯示名稱篩選。</span><span class="sxs-lookup"><span data-stu-id="a5917-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-137">-已啟用</span><span class="sxs-lookup"><span data-stu-id="a5917-137">-Enabled</span></span>
<span data-ttu-id="a5917-138">警示規則已啟用。</span><span class="sxs-lookup"><span data-stu-id="a5917-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5917-139">-InputObject</span></span>
<span data-ttu-id="a5917-140">InputObject。</span><span class="sxs-lookup"><span data-stu-id="a5917-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="a5917-141">-ProductFilter</span></span>
<span data-ttu-id="a5917-142">警示規則產品篩選。</span><span class="sxs-lookup"><span data-stu-id="a5917-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-143">-查詢</span><span class="sxs-lookup"><span data-stu-id="a5917-143">-Query</span></span>
<span data-ttu-id="a5917-144">警示規則查詢。</span><span class="sxs-lookup"><span data-stu-id="a5917-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="a5917-145">-QueryFrequency</span></span>
<span data-ttu-id="a5917-146">警示規則查詢頻率。</span><span class="sxs-lookup"><span data-stu-id="a5917-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="a5917-147">-QueryPeriod</span></span>
<span data-ttu-id="a5917-148">警示規則查詢期間。</span><span class="sxs-lookup"><span data-stu-id="a5917-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5917-149">-ResourceGroupName</span></span>
<span data-ttu-id="a5917-150">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a5917-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5917-151">-ResourceId</span></span>
<span data-ttu-id="a5917-152">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5917-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-153">-嚴重性篩選</span><span class="sxs-lookup"><span data-stu-id="a5917-153">-SeveritiesFilter</span></span>
<span data-ttu-id="a5917-154">警示規則嚴重性篩選。</span><span class="sxs-lookup"><span data-stu-id="a5917-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-155">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="a5917-155">-Severity</span></span>
<span data-ttu-id="a5917-156">事件嚴重性。</span><span class="sxs-lookup"><span data-stu-id="a5917-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-157">-Disableabled</span><span class="sxs-lookup"><span data-stu-id="a5917-157">-SuppressionDisabled</span></span>
<span data-ttu-id="a5917-158">警示規則停用。</span><span class="sxs-lookup"><span data-stu-id="a5917-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-159">-Duration</span><span class="sxs-lookup"><span data-stu-id="a5917-159">-SuppressionDuration</span></span>
<span data-ttu-id="a5917-160">警示規則干擾持續時間。</span><span class="sxs-lookup"><span data-stu-id="a5917-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-161">-一應萬能</span><span class="sxs-lookup"><span data-stu-id="a5917-161">-SuppressionEnabled</span></span>
<span data-ttu-id="a5917-162">已啟用警示規則啟用。</span><span class="sxs-lookup"><span data-stu-id="a5917-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-163">-策略</span><span class="sxs-lookup"><span data-stu-id="a5917-163">-Tactics</span></span>
<span data-ttu-id="a5917-164">警示規則策略。</span><span class="sxs-lookup"><span data-stu-id="a5917-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="a5917-165">-TriggerOperator</span></span>
<span data-ttu-id="a5917-166">警示規則引發運算子。</span><span class="sxs-lookup"><span data-stu-id="a5917-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="a5917-167">-TriggerThreshold</span></span>
<span data-ttu-id="a5917-168">警示規則引發閾值。</span><span class="sxs-lookup"><span data-stu-id="a5917-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5917-169">-WorkspaceName</span></span>
<span data-ttu-id="a5917-170">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="a5917-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-171">-確認</span><span class="sxs-lookup"><span data-stu-id="a5917-171">-Confirm</span></span>
<span data-ttu-id="a5917-172">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5917-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5917-173">-WhatIf</span></span>
<span data-ttu-id="a5917-174">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5917-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5917-175">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5917-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5917-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5917-176">CommonParameters</span></span>
<span data-ttu-id="a5917-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5917-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5917-178">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5917-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5917-179">輸入</span><span class="sxs-lookup"><span data-stu-id="a5917-179">INPUTS</span></span>

### <span data-ttu-id="a5917-180">Microsoft.Azure.Commands.SecurityInsights.models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a5917-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="a5917-181">System.String</span><span class="sxs-lookup"><span data-stu-id="a5917-181">System.String</span></span>

## <span data-ttu-id="a5917-182">輸出</span><span class="sxs-lookup"><span data-stu-id="a5917-182">OUTPUTS</span></span>

### <span data-ttu-id="a5917-183">Microsoft.Azure.Commands.SecurityInsights.models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a5917-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="a5917-184">筆記</span><span class="sxs-lookup"><span data-stu-id="a5917-184">NOTES</span></span>

## <span data-ttu-id="a5917-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5917-185">RELATED LINKS</span></span>
