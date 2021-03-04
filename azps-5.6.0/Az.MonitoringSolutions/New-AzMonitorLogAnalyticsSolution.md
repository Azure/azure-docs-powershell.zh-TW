---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905357"
---
# <span data-ttu-id="a0075-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="a0075-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="a0075-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a0075-102">SYNOPSIS</span></span>
<span data-ttu-id="a0075-103">建立記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="a0075-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="a0075-104">語法</span><span class="sxs-lookup"><span data-stu-id="a0075-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0075-105">描述</span><span class="sxs-lookup"><span data-stu-id="a0075-105">DESCRIPTION</span></span>
<span data-ttu-id="a0075-106">建立記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="a0075-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="a0075-107">例子</span><span class="sxs-lookup"><span data-stu-id="a0075-107">EXAMPLES</span></span>

### <span data-ttu-id="a0075-108">範例 1：為記錄分析工作區建立監視器記錄分析解決方案</span><span class="sxs-lookup"><span data-stu-id="a0075-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="a0075-109">此命令會針對記錄分析工作區建立監視器記錄分析解決方案。</span><span class="sxs-lookup"><span data-stu-id="a0075-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="a0075-110">常用的類型有：</span><span class="sxs-lookup"><span data-stu-id="a0075-110">Commonly used types are:</span></span>

| <span data-ttu-id="a0075-111">類型</span><span class="sxs-lookup"><span data-stu-id="a0075-111">Type</span></span> | <span data-ttu-id="a0075-112">描述</span><span class="sxs-lookup"><span data-stu-id="a0075-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="a0075-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="a0075-113">SecurityCenterFree</span></span> |  <span data-ttu-id="a0075-114">Azure 資訊安全中心 – 免費版</span><span class="sxs-lookup"><span data-stu-id="a0075-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="a0075-115">安全</span><span class="sxs-lookup"><span data-stu-id="a0075-115">Security</span></span> | <span data-ttu-id="a0075-116">Azure 資訊安全中心</span><span class="sxs-lookup"><span data-stu-id="a0075-116">Azure Security Center</span></span> |
| <span data-ttu-id="a0075-117">更新</span><span class="sxs-lookup"><span data-stu-id="a0075-117">Updates</span></span> | <span data-ttu-id="a0075-118">更新管理</span><span class="sxs-lookup"><span data-stu-id="a0075-118">Update Management</span></span> |
| <span data-ttu-id="a0075-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="a0075-119">ContainerInsights</span></span> | <span data-ttu-id="a0075-120">容器的 Azure 監視器</span><span class="sxs-lookup"><span data-stu-id="a0075-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="a0075-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="a0075-121">ServiceMap</span></span> | <span data-ttu-id="a0075-122">服務地圖</span><span class="sxs-lookup"><span data-stu-id="a0075-122">Service Map</span></span> |
| <span data-ttu-id="a0075-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="a0075-123">AzureActivity</span></span> | <span data-ttu-id="a0075-124">活動記錄分析</span><span class="sxs-lookup"><span data-stu-id="a0075-124">Activity log analytics</span></span> |
| <span data-ttu-id="a0075-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="a0075-125">ChangeTracking</span></span> | <span data-ttu-id="a0075-126">追蹤和庫存變更</span><span class="sxs-lookup"><span data-stu-id="a0075-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="a0075-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="a0075-127">VMInsights</span></span> | <span data-ttu-id="a0075-128">適用于虛擬機器的 Azure 監視器</span><span class="sxs-lookup"><span data-stu-id="a0075-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="a0075-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="a0075-129">SecurityInsights</span></span> | <span data-ttu-id="a0075-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="a0075-130">Azure Sentinel</span></span> |
| <span data-ttu-id="a0075-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="a0075-131">NetworkMonitoring</span></span> | <span data-ttu-id="a0075-132">網路績效監視器</span><span class="sxs-lookup"><span data-stu-id="a0075-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="a0075-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="a0075-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="a0075-134">SQL 弱點評估</span><span class="sxs-lookup"><span data-stu-id="a0075-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="a0075-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a0075-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="a0075-136">SQL 進位威脅防護</span><span class="sxs-lookup"><span data-stu-id="a0075-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="a0075-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="a0075-137">AntiMalware</span></span> | <span data-ttu-id="a0075-138">反惡意軟體評定</span><span class="sxs-lookup"><span data-stu-id="a0075-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="a0075-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="a0075-139">AzureAutomation</span></span> | <span data-ttu-id="a0075-140">自動化混合式員工</span><span class="sxs-lookup"><span data-stu-id="a0075-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="a0075-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="a0075-141">LogicAppsManagement</span></span> | <span data-ttu-id="a0075-142">邏輯應用程式管理</span><span class="sxs-lookup"><span data-stu-id="a0075-142">Logic Apps Management</span></span> |
| <span data-ttu-id="a0075-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="a0075-143">SQLDataClassification</span></span> | <span data-ttu-id="a0075-144">SQL 資料探索&分類</span><span class="sxs-lookup"><span data-stu-id="a0075-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="a0075-145">參數</span><span class="sxs-lookup"><span data-stu-id="a0075-145">PARAMETERS</span></span>

### <span data-ttu-id="a0075-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0075-146">-DefaultProfile</span></span>
<span data-ttu-id="a0075-147">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0075-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0075-148">-位置</span><span class="sxs-lookup"><span data-stu-id="a0075-148">-Location</span></span>
<span data-ttu-id="a0075-149">資源位置。</span><span class="sxs-lookup"><span data-stu-id="a0075-149">Resource location.</span></span>
<span data-ttu-id="a0075-150">必須與記錄分析工作區相同。</span><span class="sxs-lookup"><span data-stu-id="a0075-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="a0075-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0075-151">-ResourceGroupName</span></span>
<span data-ttu-id="a0075-152">要取得的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a0075-152">The name of the resource group to get.</span></span>
<span data-ttu-id="a0075-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0075-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0075-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0075-154">-SubscriptionId</span></span>
<span data-ttu-id="a0075-155">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a0075-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0075-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a0075-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0075-157">-標記</span><span class="sxs-lookup"><span data-stu-id="a0075-157">-Tag</span></span>
<span data-ttu-id="a0075-158">資源標記</span><span class="sxs-lookup"><span data-stu-id="a0075-158">Resource tags</span></span>

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

### <span data-ttu-id="a0075-159">-類型</span><span class="sxs-lookup"><span data-stu-id="a0075-159">-Type</span></span>
<span data-ttu-id="a0075-160">要建立的解決方案類型。</span><span class="sxs-lookup"><span data-stu-id="a0075-160">Type of the solution to be created.</span></span>
<span data-ttu-id="a0075-161">例如"Container"。</span><span class="sxs-lookup"><span data-stu-id="a0075-161">For example "Container".</span></span>

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

### <span data-ttu-id="a0075-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a0075-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="a0075-163">將部署/啟用解決方案之工作區的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0075-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="a0075-164">-確認</span><span class="sxs-lookup"><span data-stu-id="a0075-164">-Confirm</span></span>
<span data-ttu-id="a0075-165">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a0075-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0075-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0075-166">-WhatIf</span></span>
<span data-ttu-id="a0075-167">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0075-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0075-168">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0075-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0075-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0075-169">CommonParameters</span></span>
<span data-ttu-id="a0075-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a0075-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0075-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0075-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0075-172">輸入</span><span class="sxs-lookup"><span data-stu-id="a0075-172">INPUTS</span></span>

## <span data-ttu-id="a0075-173">輸出</span><span class="sxs-lookup"><span data-stu-id="a0075-173">OUTPUTS</span></span>

### <span data-ttu-id="a0075-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="a0075-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="a0075-175">筆記</span><span class="sxs-lookup"><span data-stu-id="a0075-175">NOTES</span></span>

<span data-ttu-id="a0075-176">別名</span><span class="sxs-lookup"><span data-stu-id="a0075-176">ALIASES</span></span>

## <span data-ttu-id="a0075-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0075-177">RELATED LINKS</span></span>



[<span data-ttu-id="a0075-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a0075-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

