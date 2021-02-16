---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139895"
---
# <span data-ttu-id="c3ee2-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3ee2-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="c3ee2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ee2-103">) 建立分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="c3ee2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3ee2-104">SYNTAX</span></span>

### <span data-ttu-id="c3ee2-105">ScheduledAlertRule (預設) </span><span class="sxs-lookup"><span data-stu-id="c3ee2-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3ee2-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3ee2-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3ee2-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="c3ee2-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ee2-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3ee2-108">DESCRIPTION</span></span>
<span data-ttu-id="c3ee2-109">**新的-AzSentinelAlertRule** Cmdlet 會在指定的工作區中建立) 的分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="c3ee2-110">您必須指定其中一個參數（ *合成*、 *排程* 或 *MicrosoftSecurityIncidentCreation*），才能指定要建立的報警規則類型。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="c3ee2-111">每個類型都有不同的必要 paramaters。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="c3ee2-112">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c3ee2-113">示例</span><span class="sxs-lookup"><span data-stu-id="c3ee2-113">EXAMPLES</span></span>

### <span data-ttu-id="c3ee2-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c3ee2-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="c3ee2-115">這個範例會根據針對 *高級 Multistage 攻擊偵測* 的範本，建立 *融合* 類型的 **AlertRule** ，然後將它儲存在 $AlertRule 變數中。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="c3ee2-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c3ee2-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="c3ee2-117">這個範例會根據針對 *IoT 通知的 Azure 安全中心建立事件* 的範本，建立 *MicrosoftSecurityIncidentCreation* 類型的 **AlertRule** ，然後將其儲存在 $AlertRule varaible 中。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="c3ee2-118">範例2</span><span class="sxs-lookup"><span data-stu-id="c3ee2-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="c3ee2-119">這個範例會建立 *排程* 類型的 **DataConnector** ，然後將其儲存在 $AlertRule varaible 中。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="c3ee2-120">參數</span><span class="sxs-lookup"><span data-stu-id="c3ee2-120">PARAMETERS</span></span>

### <span data-ttu-id="c3ee2-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c3ee2-121">-AlertRuleId</span></span>
<span data-ttu-id="c3ee2-122">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="c3ee2-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="c3ee2-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="c3ee2-124">[警示規則] 範本。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ee2-125">-DefaultProfile</span></span>
<span data-ttu-id="c3ee2-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3ee2-127">-描述</span><span class="sxs-lookup"><span data-stu-id="c3ee2-127">-Description</span></span>
<span data-ttu-id="c3ee2-128">說明.</span><span class="sxs-lookup"><span data-stu-id="c3ee2-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3ee2-129">-DisplayName</span></span>
<span data-ttu-id="c3ee2-130">警示規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="c3ee2-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="c3ee2-132">警示規則顯示名稱排除篩選器。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="c3ee2-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="c3ee2-134">[警示規則顯示名稱] 篩選。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-135">-啟用</span><span class="sxs-lookup"><span data-stu-id="c3ee2-135">-Enabled</span></span>
<span data-ttu-id="c3ee2-136">已啟用通知規則。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="c3ee2-137">合成</span><span class="sxs-lookup"><span data-stu-id="c3ee2-137">-Fusion</span></span>
<span data-ttu-id="c3ee2-138">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="c3ee2-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="c3ee2-140">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="c3ee2-141">-ProductFilter</span></span>
<span data-ttu-id="c3ee2-142">[警示規則產品] 篩選。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-143">-Query</span><span class="sxs-lookup"><span data-stu-id="c3ee2-143">-Query</span></span>
<span data-ttu-id="c3ee2-144">[警示規則查詢]。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="c3ee2-145">-QueryFrequency</span></span>
<span data-ttu-id="c3ee2-146">警報規則查詢頻率。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="c3ee2-147">-QueryPeriod</span></span>
<span data-ttu-id="c3ee2-148">[警示規則] 查詢期間。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ee2-149">-ResourceGroupName</span></span>
<span data-ttu-id="c3ee2-150">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-150">Resource group name.</span></span>

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

### <span data-ttu-id="c3ee2-151">-排程</span><span class="sxs-lookup"><span data-stu-id="c3ee2-151">-Scheduled</span></span>
<span data-ttu-id="c3ee2-152">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="c3ee2-153">-SeveritiesFilter</span></span>
<span data-ttu-id="c3ee2-154">[警示規則嚴重性] 篩選。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-155">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="c3ee2-155">-Severity</span></span>
<span data-ttu-id="c3ee2-156">事件嚴重度。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="c3ee2-157">-SuppressionDuration</span></span>
<span data-ttu-id="c3ee2-158">警示規則抑制工期。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="c3ee2-159">-SuppressionEnabled</span></span>
<span data-ttu-id="c3ee2-160">已啟用警示規則。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-161">-戰術</span><span class="sxs-lookup"><span data-stu-id="c3ee2-161">-Tactics</span></span>
<span data-ttu-id="c3ee2-162">警示規則戰術。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="c3ee2-163">-TriggerOperator</span></span>
<span data-ttu-id="c3ee2-164">[警示規則引發] 運算子。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="c3ee2-165">-TriggerThreshold</span></span>
<span data-ttu-id="c3ee2-166">警報規則引發閥值。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ee2-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3ee2-167">-WorkspaceName</span></span>
<span data-ttu-id="c3ee2-168">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-168">Workspace Name.</span></span>

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

### <span data-ttu-id="c3ee2-169">-確認</span><span class="sxs-lookup"><span data-stu-id="c3ee2-169">-Confirm</span></span>
<span data-ttu-id="c3ee2-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ee2-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ee2-171">-WhatIf</span></span>
<span data-ttu-id="c3ee2-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3ee2-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ee2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ee2-174">CommonParameters</span></span>
<span data-ttu-id="c3ee2-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ee2-176">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3ee2-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ee2-177">輸入</span><span class="sxs-lookup"><span data-stu-id="c3ee2-177">INPUTS</span></span>

### <span data-ttu-id="c3ee2-178">所有</span><span class="sxs-lookup"><span data-stu-id="c3ee2-178">None</span></span>
## <span data-ttu-id="c3ee2-179">輸出</span><span class="sxs-lookup"><span data-stu-id="c3ee2-179">OUTPUTS</span></span>

### <span data-ttu-id="c3ee2-180">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="c3ee2-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="c3ee2-181">筆記</span><span class="sxs-lookup"><span data-stu-id="c3ee2-181">NOTES</span></span>

## <span data-ttu-id="c3ee2-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3ee2-182">RELATED LINKS</span></span>
