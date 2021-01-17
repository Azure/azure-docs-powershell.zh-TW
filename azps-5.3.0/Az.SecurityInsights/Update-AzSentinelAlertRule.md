---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448519"
---
# <span data-ttu-id="e1da9-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1da9-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="e1da9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1da9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1da9-103">) 建立分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="e1da9-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="e1da9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1da9-104">SYNTAX</span></span>

### <span data-ttu-id="e1da9-105">AlertRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="e1da9-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="e1da9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1da9-106">InputObject</span></span>
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

### <span data-ttu-id="e1da9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1da9-107">ResourceId</span></span>
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

## <span data-ttu-id="e1da9-108">說明</span><span class="sxs-lookup"><span data-stu-id="e1da9-108">DESCRIPTION</span></span>
<span data-ttu-id="e1da9-109">**更新-AzSentinelAlertRule** Cmdlet 會更新指定工作區中) 的分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="e1da9-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="e1da9-110">您可以使用-InputObject 或-ResourceId 或-AlertId。</span><span class="sxs-lookup"><span data-stu-id="e1da9-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="e1da9-111">您可以更新1個或多個 proprtery parmaters。</span><span class="sxs-lookup"><span data-stu-id="e1da9-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="e1da9-112">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1da9-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="e1da9-113">示例</span><span class="sxs-lookup"><span data-stu-id="e1da9-113">EXAMPLES</span></span>

### <span data-ttu-id="e1da9-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e1da9-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="e1da9-115">這個範例會將 **AlertRule** 設定為 [ *已停用* ]，並重新命名為 [ *disabled-AlertRuleDisplayName*]。</span><span class="sxs-lookup"><span data-stu-id="e1da9-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="e1da9-116">所有其他屬性都將保持不變。</span><span class="sxs-lookup"><span data-stu-id="e1da9-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="e1da9-117">範例2</span><span class="sxs-lookup"><span data-stu-id="e1da9-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="e1da9-118">這個範例使用 InputObject 設定為 [*停* 用] 來更新 **AlertRule** 。</span><span class="sxs-lookup"><span data-stu-id="e1da9-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="e1da9-119">所有其他屬性都將保持不變。</span><span class="sxs-lookup"><span data-stu-id="e1da9-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="e1da9-120">參數</span><span class="sxs-lookup"><span data-stu-id="e1da9-120">PARAMETERS</span></span>

### <span data-ttu-id="e1da9-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e1da9-121">-AlertRuleId</span></span>
<span data-ttu-id="e1da9-122">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e1da9-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="e1da9-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="e1da9-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="e1da9-124">[警示規則] 範本。</span><span class="sxs-lookup"><span data-stu-id="e1da9-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="e1da9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1da9-125">-DefaultProfile</span></span>
<span data-ttu-id="e1da9-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1da9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1da9-127">-描述</span><span class="sxs-lookup"><span data-stu-id="e1da9-127">-Description</span></span>
<span data-ttu-id="e1da9-128">說明.</span><span class="sxs-lookup"><span data-stu-id="e1da9-128">Description.</span></span>

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

### <span data-ttu-id="e1da9-129">-已停用</span><span class="sxs-lookup"><span data-stu-id="e1da9-129">-Disabled</span></span>
<span data-ttu-id="e1da9-130">已停用通知規則。</span><span class="sxs-lookup"><span data-stu-id="e1da9-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="e1da9-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1da9-131">-DisplayName</span></span>
<span data-ttu-id="e1da9-132">警示規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e1da9-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="e1da9-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="e1da9-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="e1da9-134">警示規則顯示名稱排除篩選器。</span><span class="sxs-lookup"><span data-stu-id="e1da9-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="e1da9-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="e1da9-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="e1da9-136">[警示規則顯示名稱] 篩選。</span><span class="sxs-lookup"><span data-stu-id="e1da9-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="e1da9-137">-啟用</span><span class="sxs-lookup"><span data-stu-id="e1da9-137">-Enabled</span></span>
<span data-ttu-id="e1da9-138">已啟用通知規則。</span><span class="sxs-lookup"><span data-stu-id="e1da9-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="e1da9-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1da9-139">-InputObject</span></span>
<span data-ttu-id="e1da9-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="e1da9-140">InputObject.</span></span>

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

### <span data-ttu-id="e1da9-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="e1da9-141">-ProductFilter</span></span>
<span data-ttu-id="e1da9-142">[警示規則產品] 篩選。</span><span class="sxs-lookup"><span data-stu-id="e1da9-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="e1da9-143">-Query</span><span class="sxs-lookup"><span data-stu-id="e1da9-143">-Query</span></span>
<span data-ttu-id="e1da9-144">[警示規則查詢]。</span><span class="sxs-lookup"><span data-stu-id="e1da9-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="e1da9-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="e1da9-145">-QueryFrequency</span></span>
<span data-ttu-id="e1da9-146">警報規則查詢頻率。</span><span class="sxs-lookup"><span data-stu-id="e1da9-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="e1da9-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="e1da9-147">-QueryPeriod</span></span>
<span data-ttu-id="e1da9-148">[警示規則] 查詢期間。</span><span class="sxs-lookup"><span data-stu-id="e1da9-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="e1da9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1da9-149">-ResourceGroupName</span></span>
<span data-ttu-id="e1da9-150">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e1da9-150">Resource group name.</span></span>

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

### <span data-ttu-id="e1da9-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1da9-151">-ResourceId</span></span>
<span data-ttu-id="e1da9-152">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e1da9-152">Resource Id.</span></span>

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

### <span data-ttu-id="e1da9-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="e1da9-153">-SeveritiesFilter</span></span>
<span data-ttu-id="e1da9-154">[警示規則嚴重性] 篩選。</span><span class="sxs-lookup"><span data-stu-id="e1da9-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="e1da9-155">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="e1da9-155">-Severity</span></span>
<span data-ttu-id="e1da9-156">事件嚴重度。</span><span class="sxs-lookup"><span data-stu-id="e1da9-156">Incident Severity.</span></span>

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

### <span data-ttu-id="e1da9-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="e1da9-157">-SuppressionDisabled</span></span>
<span data-ttu-id="e1da9-158">停用警報規則禁止。</span><span class="sxs-lookup"><span data-stu-id="e1da9-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="e1da9-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="e1da9-159">-SuppressionDuration</span></span>
<span data-ttu-id="e1da9-160">警示規則抑制工期。</span><span class="sxs-lookup"><span data-stu-id="e1da9-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="e1da9-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="e1da9-161">-SuppressionEnabled</span></span>
<span data-ttu-id="e1da9-162">已啟用警示規則。</span><span class="sxs-lookup"><span data-stu-id="e1da9-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="e1da9-163">-戰術</span><span class="sxs-lookup"><span data-stu-id="e1da9-163">-Tactics</span></span>
<span data-ttu-id="e1da9-164">警示規則戰術。</span><span class="sxs-lookup"><span data-stu-id="e1da9-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="e1da9-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="e1da9-165">-TriggerOperator</span></span>
<span data-ttu-id="e1da9-166">[警示規則引發] 運算子。</span><span class="sxs-lookup"><span data-stu-id="e1da9-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="e1da9-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="e1da9-167">-TriggerThreshold</span></span>
<span data-ttu-id="e1da9-168">警報規則引發閥值。</span><span class="sxs-lookup"><span data-stu-id="e1da9-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="e1da9-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1da9-169">-WorkspaceName</span></span>
<span data-ttu-id="e1da9-170">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e1da9-170">Workspace Name.</span></span>

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

### <span data-ttu-id="e1da9-171">-確認</span><span class="sxs-lookup"><span data-stu-id="e1da9-171">-Confirm</span></span>
<span data-ttu-id="e1da9-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1da9-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1da9-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1da9-173">-WhatIf</span></span>
<span data-ttu-id="e1da9-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1da9-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1da9-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1da9-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1da9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1da9-176">CommonParameters</span></span>
<span data-ttu-id="e1da9-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1da9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1da9-178">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1da9-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1da9-179">輸入</span><span class="sxs-lookup"><span data-stu-id="e1da9-179">INPUTS</span></span>

### <span data-ttu-id="e1da9-180">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="e1da9-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="e1da9-181">System.object</span><span class="sxs-lookup"><span data-stu-id="e1da9-181">System.String</span></span>

## <span data-ttu-id="e1da9-182">輸出</span><span class="sxs-lookup"><span data-stu-id="e1da9-182">OUTPUTS</span></span>

### <span data-ttu-id="e1da9-183">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="e1da9-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="e1da9-184">筆記</span><span class="sxs-lookup"><span data-stu-id="e1da9-184">NOTES</span></span>

## <span data-ttu-id="e1da9-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1da9-185">RELATED LINKS</span></span>
