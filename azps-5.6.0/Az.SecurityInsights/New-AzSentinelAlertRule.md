---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 0efb30f9c740362ac6e8c432179599c7d4aef88d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908014"
---
# <span data-ttu-id="3bc62-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="3bc62-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="3bc62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3bc62-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc62-103">建立分析 (警示規則) 。</span><span class="sxs-lookup"><span data-stu-id="3bc62-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="3bc62-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bc62-104">SYNTAX</span></span>

### <span data-ttu-id="3bc62-105">ScheduledAlertRule (預設) </span><span class="sxs-lookup"><span data-stu-id="3bc62-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc62-106">RuleAlertRule</span><span class="sxs-lookup"><span data-stu-id="3bc62-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc62-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="3bc62-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc62-108">描述</span><span class="sxs-lookup"><span data-stu-id="3bc62-108">DESCRIPTION</span></span>
<span data-ttu-id="3bc62-109">**New-AzSentinelAlertRule** Cmdlet 會建立 (工作區) 警示規則。</span><span class="sxs-lookup"><span data-stu-id="3bc62-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="3bc62-110">您必須指定三個參數的其中一個，即 *通知*、排程或 *MicrosoftSecurityIncidentCreation，* 以指定要建立的警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="3bc62-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="3bc62-111">每種類型都有不同的所需參數。</span><span class="sxs-lookup"><span data-stu-id="3bc62-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="3bc62-112">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3bc62-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3bc62-113">例子</span><span class="sxs-lookup"><span data-stu-id="3bc62-113">EXAMPLES</span></span>

### <span data-ttu-id="3bc62-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="3bc62-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="3bc62-115">此範例會依據進一級多階段攻擊偵測的範本建立 **一** 個通知規則 ，然後將它儲存在 $AlertRule 變數中。</span><span class="sxs-lookup"><span data-stu-id="3bc62-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="3bc62-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="3bc62-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="3bc62-117">此範例根據 Azure 資訊安全中心 For *IoT* 警示建立事件範本，建立 *MicrosoftSecurityIncidentCreation* 類型的 **AlertRule，** 然後將它儲存在 $AlertRule varaible 中。</span><span class="sxs-lookup"><span data-stu-id="3bc62-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="3bc62-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="3bc62-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="3bc62-119">此範例會建立一個排程類型的 **DataConnector，** 然後將它儲存在$AlertRule中。 </span><span class="sxs-lookup"><span data-stu-id="3bc62-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="3bc62-120">參數</span><span class="sxs-lookup"><span data-stu-id="3bc62-120">PARAMETERS</span></span>

### <span data-ttu-id="3bc62-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="3bc62-121">-AlertRuleId</span></span>
<span data-ttu-id="3bc62-122">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bc62-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="3bc62-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="3bc62-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="3bc62-124">警示規則範本。</span><span class="sxs-lookup"><span data-stu-id="3bc62-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="3bc62-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc62-125">-DefaultProfile</span></span>
<span data-ttu-id="3bc62-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bc62-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc62-127">-描述</span><span class="sxs-lookup"><span data-stu-id="3bc62-127">-Description</span></span>
<span data-ttu-id="3bc62-128">描述。</span><span class="sxs-lookup"><span data-stu-id="3bc62-128">Description.</span></span>

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

### <span data-ttu-id="3bc62-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bc62-129">-DisplayName</span></span>
<span data-ttu-id="3bc62-130">警示規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc62-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="3bc62-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="3bc62-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="3bc62-132">警示規則顯示名稱排除篩選。</span><span class="sxs-lookup"><span data-stu-id="3bc62-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="3bc62-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="3bc62-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="3bc62-134">警示規則顯示名稱篩選。</span><span class="sxs-lookup"><span data-stu-id="3bc62-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="3bc62-135">-已啟用</span><span class="sxs-lookup"><span data-stu-id="3bc62-135">-Enabled</span></span>
<span data-ttu-id="3bc62-136">警示規則已啟用。</span><span class="sxs-lookup"><span data-stu-id="3bc62-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="3bc62-137">-外接式</span><span class="sxs-lookup"><span data-stu-id="3bc62-137">-Fusion</span></span>
<span data-ttu-id="3bc62-138">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="3bc62-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="3bc62-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="3bc62-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="3bc62-140">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="3bc62-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="3bc62-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="3bc62-141">-ProductFilter</span></span>
<span data-ttu-id="3bc62-142">警示規則產品篩選。</span><span class="sxs-lookup"><span data-stu-id="3bc62-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="3bc62-143">-查詢</span><span class="sxs-lookup"><span data-stu-id="3bc62-143">-Query</span></span>
<span data-ttu-id="3bc62-144">警示規則查詢。</span><span class="sxs-lookup"><span data-stu-id="3bc62-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="3bc62-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="3bc62-145">-QueryFrequency</span></span>
<span data-ttu-id="3bc62-146">警示規則查詢頻率。</span><span class="sxs-lookup"><span data-stu-id="3bc62-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="3bc62-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="3bc62-147">-QueryPeriod</span></span>
<span data-ttu-id="3bc62-148">警示規則查詢期間。</span><span class="sxs-lookup"><span data-stu-id="3bc62-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="3bc62-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc62-149">-ResourceGroupName</span></span>
<span data-ttu-id="3bc62-150">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3bc62-150">Resource group name.</span></span>

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

### <span data-ttu-id="3bc62-151">-已排程</span><span class="sxs-lookup"><span data-stu-id="3bc62-151">-Scheduled</span></span>
<span data-ttu-id="3bc62-152">警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="3bc62-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="3bc62-153">-嚴重性篩選</span><span class="sxs-lookup"><span data-stu-id="3bc62-153">-SeveritiesFilter</span></span>
<span data-ttu-id="3bc62-154">警示規則嚴重性篩選。</span><span class="sxs-lookup"><span data-stu-id="3bc62-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="3bc62-155">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="3bc62-155">-Severity</span></span>
<span data-ttu-id="3bc62-156">事件嚴重性。</span><span class="sxs-lookup"><span data-stu-id="3bc62-156">Incident Severity.</span></span>

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

### <span data-ttu-id="3bc62-157">-Duration</span><span class="sxs-lookup"><span data-stu-id="3bc62-157">-SuppressionDuration</span></span>
<span data-ttu-id="3bc62-158">警示規則干擾持續時間。</span><span class="sxs-lookup"><span data-stu-id="3bc62-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="3bc62-159">-一應萬能</span><span class="sxs-lookup"><span data-stu-id="3bc62-159">-SuppressionEnabled</span></span>
<span data-ttu-id="3bc62-160">已啟用警示規則啟用。</span><span class="sxs-lookup"><span data-stu-id="3bc62-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="3bc62-161">-策略</span><span class="sxs-lookup"><span data-stu-id="3bc62-161">-Tactics</span></span>
<span data-ttu-id="3bc62-162">警示規則策略。</span><span class="sxs-lookup"><span data-stu-id="3bc62-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="3bc62-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="3bc62-163">-TriggerOperator</span></span>
<span data-ttu-id="3bc62-164">警示規則引發運算子。</span><span class="sxs-lookup"><span data-stu-id="3bc62-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="3bc62-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="3bc62-165">-TriggerThreshold</span></span>
<span data-ttu-id="3bc62-166">警示規則引發閾值。</span><span class="sxs-lookup"><span data-stu-id="3bc62-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="3bc62-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bc62-167">-WorkspaceName</span></span>
<span data-ttu-id="3bc62-168">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc62-168">Workspace Name.</span></span>

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

### <span data-ttu-id="3bc62-169">-確認</span><span class="sxs-lookup"><span data-stu-id="3bc62-169">-Confirm</span></span>
<span data-ttu-id="3bc62-170">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3bc62-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc62-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc62-171">-WhatIf</span></span>
<span data-ttu-id="3bc62-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bc62-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bc62-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bc62-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc62-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc62-174">CommonParameters</span></span>
<span data-ttu-id="3bc62-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3bc62-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc62-176">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bc62-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc62-177">輸入</span><span class="sxs-lookup"><span data-stu-id="3bc62-177">INPUTS</span></span>

### <span data-ttu-id="3bc62-178">沒有</span><span class="sxs-lookup"><span data-stu-id="3bc62-178">None</span></span>
## <span data-ttu-id="3bc62-179">輸出</span><span class="sxs-lookup"><span data-stu-id="3bc62-179">OUTPUTS</span></span>

### <span data-ttu-id="3bc62-180">Microsoft.Azure.Commands.SecurityInsights.models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="3bc62-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="3bc62-181">筆記</span><span class="sxs-lookup"><span data-stu-id="3bc62-181">NOTES</span></span>

## <span data-ttu-id="3bc62-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bc62-182">RELATED LINKS</span></span>
