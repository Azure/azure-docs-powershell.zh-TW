---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279280"
---
# <span data-ttu-id="7033b-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="7033b-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="7033b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7033b-102">SYNOPSIS</span></span>
<span data-ttu-id="7033b-103">建立 log analytics 方案。</span><span class="sxs-lookup"><span data-stu-id="7033b-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="7033b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7033b-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7033b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7033b-105">DESCRIPTION</span></span>
<span data-ttu-id="7033b-106">建立 log analytics 方案。</span><span class="sxs-lookup"><span data-stu-id="7033b-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="7033b-107">示例</span><span class="sxs-lookup"><span data-stu-id="7033b-107">EXAMPLES</span></span>

### <span data-ttu-id="7033b-108">範例1：為 log analytics 工作區建立監視器記錄分析方案</span><span class="sxs-lookup"><span data-stu-id="7033b-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="7033b-109">這個命令會為 log analytics 工作區建立監視器記錄分析方案。</span><span class="sxs-lookup"><span data-stu-id="7033b-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="7033b-110">常用類型如下：</span><span class="sxs-lookup"><span data-stu-id="7033b-110">Commonly used types are:</span></span>

| <span data-ttu-id="7033b-111">輸入</span><span class="sxs-lookup"><span data-stu-id="7033b-111">Type</span></span> | <span data-ttu-id="7033b-112">說明</span><span class="sxs-lookup"><span data-stu-id="7033b-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="7033b-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="7033b-113">SecurityCenterFree</span></span> |  <span data-ttu-id="7033b-114">Azure 安全中心-免費版</span><span class="sxs-lookup"><span data-stu-id="7033b-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="7033b-115">安全性</span><span class="sxs-lookup"><span data-stu-id="7033b-115">Security</span></span> | <span data-ttu-id="7033b-116">Azure 安全中心</span><span class="sxs-lookup"><span data-stu-id="7033b-116">Azure Security Center</span></span> |
| <span data-ttu-id="7033b-117">更新</span><span class="sxs-lookup"><span data-stu-id="7033b-117">Updates</span></span> | <span data-ttu-id="7033b-118">更新管理</span><span class="sxs-lookup"><span data-stu-id="7033b-118">Update Management</span></span> |
| <span data-ttu-id="7033b-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="7033b-119">ContainerInsights</span></span> | <span data-ttu-id="7033b-120">容器的 Azure 監視器</span><span class="sxs-lookup"><span data-stu-id="7033b-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="7033b-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="7033b-121">ServiceMap</span></span> | <span data-ttu-id="7033b-122">服務地圖</span><span class="sxs-lookup"><span data-stu-id="7033b-122">Service Map</span></span> |
| <span data-ttu-id="7033b-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="7033b-123">AzureActivity</span></span> | <span data-ttu-id="7033b-124">活動記錄分析</span><span class="sxs-lookup"><span data-stu-id="7033b-124">Activity log analytics</span></span> |
| <span data-ttu-id="7033b-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="7033b-125">ChangeTracking</span></span> | <span data-ttu-id="7033b-126">變更追蹤與庫存</span><span class="sxs-lookup"><span data-stu-id="7033b-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="7033b-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="7033b-127">VMInsights</span></span> | <span data-ttu-id="7033b-128">Vm 的 Azure 監視器</span><span class="sxs-lookup"><span data-stu-id="7033b-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="7033b-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="7033b-129">SecurityInsights</span></span> | <span data-ttu-id="7033b-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="7033b-130">Azure Sentinel</span></span> |
| <span data-ttu-id="7033b-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="7033b-131">NetworkMonitoring</span></span> | <span data-ttu-id="7033b-132">網路效能監視器</span><span class="sxs-lookup"><span data-stu-id="7033b-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="7033b-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="7033b-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="7033b-134">SQL 漏洞評估</span><span class="sxs-lookup"><span data-stu-id="7033b-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="7033b-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7033b-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="7033b-136">SQL 高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="7033b-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="7033b-137">軟體</span><span class="sxs-lookup"><span data-stu-id="7033b-137">AntiMalware</span></span> | <span data-ttu-id="7033b-138">反惡意程式碼評估</span><span class="sxs-lookup"><span data-stu-id="7033b-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="7033b-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="7033b-139">AzureAutomation</span></span> | <span data-ttu-id="7033b-140">自動化混合式輔助角色</span><span class="sxs-lookup"><span data-stu-id="7033b-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="7033b-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="7033b-141">LogicAppsManagement</span></span> | <span data-ttu-id="7033b-142">邏輯 App 管理</span><span class="sxs-lookup"><span data-stu-id="7033b-142">Logic Apps Management</span></span> |
| <span data-ttu-id="7033b-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="7033b-143">SQLDataClassification</span></span> | <span data-ttu-id="7033b-144">SQL 資料探索 & 分類</span><span class="sxs-lookup"><span data-stu-id="7033b-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="7033b-145">參數</span><span class="sxs-lookup"><span data-stu-id="7033b-145">PARAMETERS</span></span>

### <span data-ttu-id="7033b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7033b-146">-DefaultProfile</span></span>
<span data-ttu-id="7033b-147">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7033b-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7033b-148">-位置</span><span class="sxs-lookup"><span data-stu-id="7033b-148">-Location</span></span>
<span data-ttu-id="7033b-149">資源位置。</span><span class="sxs-lookup"><span data-stu-id="7033b-149">Resource location.</span></span>
<span data-ttu-id="7033b-150">必須與記錄分析工作區相同。</span><span class="sxs-lookup"><span data-stu-id="7033b-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="7033b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7033b-151">-ResourceGroupName</span></span>
<span data-ttu-id="7033b-152">要取得之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7033b-152">The name of the resource group to get.</span></span>
<span data-ttu-id="7033b-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7033b-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7033b-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7033b-154">-SubscriptionId</span></span>
<span data-ttu-id="7033b-155">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7033b-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7033b-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7033b-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7033b-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="7033b-157">-Tag</span></span>
<span data-ttu-id="7033b-158">資源標記</span><span class="sxs-lookup"><span data-stu-id="7033b-158">Resource tags</span></span>

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

### <span data-ttu-id="7033b-159">-類型</span><span class="sxs-lookup"><span data-stu-id="7033b-159">-Type</span></span>
<span data-ttu-id="7033b-160">要建立的方案類型。</span><span class="sxs-lookup"><span data-stu-id="7033b-160">Type of the solution to be created.</span></span>
<span data-ttu-id="7033b-161">例如「容器」。</span><span class="sxs-lookup"><span data-stu-id="7033b-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7033b-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7033b-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="7033b-163">要部署/啟用方案之工作區的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7033b-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="7033b-164">-確認</span><span class="sxs-lookup"><span data-stu-id="7033b-164">-Confirm</span></span>
<span data-ttu-id="7033b-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7033b-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7033b-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7033b-166">-WhatIf</span></span>
<span data-ttu-id="7033b-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7033b-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7033b-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7033b-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7033b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7033b-169">CommonParameters</span></span>
<span data-ttu-id="7033b-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7033b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7033b-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7033b-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7033b-172">輸入</span><span class="sxs-lookup"><span data-stu-id="7033b-172">INPUTS</span></span>

## <span data-ttu-id="7033b-173">輸出</span><span class="sxs-lookup"><span data-stu-id="7033b-173">OUTPUTS</span></span>

### <span data-ttu-id="7033b-174">ISolution （MonitoringSolutions）。 Api20151101Preview。</span><span class="sxs-lookup"><span data-stu-id="7033b-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="7033b-175">筆記</span><span class="sxs-lookup"><span data-stu-id="7033b-175">NOTES</span></span>

<span data-ttu-id="7033b-176">別名</span><span class="sxs-lookup"><span data-stu-id="7033b-176">ALIASES</span></span>

## <span data-ttu-id="7033b-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="7033b-177">RELATED LINKS</span></span>



[<span data-ttu-id="7033b-178">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7033b-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

