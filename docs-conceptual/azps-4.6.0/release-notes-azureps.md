---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: ea8169e0aa04fb4cc27b715ef9dfde86f0e75e85
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821461"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="b69a3-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="b69a3-104">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-105">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-106">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="b69a3-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="b69a3-107">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="b69a3-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-108">Az.Automation</span></span>
* <span data-ttu-id="b69a3-109">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="b69a3-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-110">Az.Compute</span></span>
* <span data-ttu-id="b69a3-111">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="b69a3-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="b69a3-112">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="b69a3-113">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="b69a3-114">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-115">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-116">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="b69a3-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-117">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-118">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="b69a3-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-119">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-120">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="b69a3-121">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="b69a3-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="b69a3-122">Az.Maintenance</span></span>
* <span data-ttu-id="b69a3-123">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="b69a3-124">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b69a3-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-125">Az.ManagedServices</span></span>
* <span data-ttu-id="b69a3-126">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="b69a3-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-127">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-128">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="b69a3-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="b69a3-129">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-130">Az.Resources</span></span>
* <span data-ttu-id="b69a3-131">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="b69a3-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="b69a3-132">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="b69a3-133">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="b69a3-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="b69a3-134">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="b69a3-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="b69a3-135">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="b69a3-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="b69a3-136">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="b69a3-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="b69a3-137">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="b69a3-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="b69a3-138">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b69a3-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b69a3-139">Az.SignalR</span></span>
* <span data-ttu-id="b69a3-140">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="b69a3-141">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-142">Az.Storage</span></span>
* <span data-ttu-id="b69a3-143">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="b69a3-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="b69a3-144">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="b69a3-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="b69a3-145">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="b69a3-146">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="b69a3-147">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="b69a3-148">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="b69a3-149">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="b69a3-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="b69a3-150">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="b69a3-151">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="b69a3-152">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="b69a3-153">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="b69a3-154">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="b69a3-155">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="b69a3-156">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="b69a3-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="b69a3-157">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="b69a3-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="b69a3-158">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-159">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-160">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="b69a3-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="b69a3-161">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="b69a3-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="b69a3-162">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="b69a3-163">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="b69a3-164">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="b69a3-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-165">Az.Aks</span></span>
* <span data-ttu-id="b69a3-166">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="b69a3-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="b69a3-167">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="b69a3-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-168">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-169">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-170">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-171">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b69a3-172">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="b69a3-173">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-174">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b69a3-175">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="b69a3-176">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-177">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-178">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="b69a3-179">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="b69a3-180">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-182">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="b69a3-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-183">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-184">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="b69a3-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-185">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-186">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="b69a3-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="b69a3-187">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="b69a3-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="b69a3-188">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="b69a3-189">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="b69a3-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="b69a3-190">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="b69a3-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="b69a3-191">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="b69a3-192">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-193">Az.Network</span></span>
* <span data-ttu-id="b69a3-194">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="b69a3-195">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="b69a3-196">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="b69a3-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="b69a3-197">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b69a3-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-199">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="b69a3-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="b69a3-200">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="b69a3-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="b69a3-201">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="b69a3-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-203">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="b69a3-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-204">Az.Resources</span></span>
* <span data-ttu-id="b69a3-205">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="b69a3-206">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-207">Az.Sql</span></span>
* <span data-ttu-id="b69a3-208">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="b69a3-209">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-210">Az.Storage</span></span>
* <span data-ttu-id="b69a3-211">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="b69a3-212">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="b69a3-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="b69a3-213">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="b69a3-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="b69a3-214">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="b69a3-215">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="b69a3-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="b69a3-216">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="b69a3-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="b69a3-217">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="b69a3-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="b69a3-218">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-219">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-220">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="b69a3-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="b69a3-221">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="b69a3-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-222">Az.Aks</span></span>
* <span data-ttu-id="b69a3-223">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="b69a3-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="b69a3-225">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="b69a3-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-226">Az.Automation</span></span>
* <span data-ttu-id="b69a3-227">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-228">Az.Compute</span></span>
* <span data-ttu-id="b69a3-229">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="b69a3-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-230">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-231">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="b69a3-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b69a3-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b69a3-232">Az.EventGrid</span></span>
* <span data-ttu-id="b69a3-233">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="b69a3-234">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="b69a3-234">Added new features:</span></span>
    - <span data-ttu-id="b69a3-235">輸入對應</span><span class="sxs-lookup"><span data-stu-id="b69a3-235">Input mapping</span></span>
    - <span data-ttu-id="b69a3-236">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="b69a3-237">私人連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-237">Private Link</span></span>
    - <span data-ttu-id="b69a3-238">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="b69a3-239">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="b69a3-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="b69a3-240">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="b69a3-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="b69a3-241">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-241">WebHook Batching</span></span>
    - <span data-ttu-id="b69a3-242">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="b69a3-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="b69a3-243">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="b69a3-243">IpFiltering</span></span>
* <span data-ttu-id="b69a3-244">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="b69a3-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="b69a3-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="b69a3-246">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="b69a3-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="b69a3-247">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="b69a3-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="b69a3-248">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="b69a3-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="b69a3-249">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="b69a3-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="b69a3-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="b69a3-251">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="b69a3-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="b69a3-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="b69a3-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="b69a3-253">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="b69a3-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-254">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-255">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="b69a3-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="b69a3-256">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-257">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-258">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="b69a3-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-259">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-260">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="b69a3-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-261">Az.Network</span></span>
* <span data-ttu-id="b69a3-262">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="b69a3-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="b69a3-263">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="b69a3-264">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="b69a3-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b69a3-265">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="b69a3-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b69a3-266">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="b69a3-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b69a3-267">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="b69a3-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="b69a3-268">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="b69a3-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="b69a3-269">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="b69a3-270">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="b69a3-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b69a3-271">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="b69a3-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b69a3-272">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="b69a3-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b69a3-273">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="b69a3-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="b69a3-274">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="b69a3-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="b69a3-275">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="b69a3-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="b69a3-276">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="b69a3-277">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="b69a3-278">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-280">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="b69a3-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="b69a3-281">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="b69a3-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="b69a3-282">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-283">Az.Resources</span></span>
* <span data-ttu-id="b69a3-284">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="b69a3-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="b69a3-285">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-286">Az.Sql</span></span>
* <span data-ttu-id="b69a3-287">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="b69a3-288">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="b69a3-289">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="b69a3-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-290">Az.Storage</span></span>
* <span data-ttu-id="b69a3-291">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="b69a3-292">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="b69a3-293">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="b69a3-294">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-295">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="b69a3-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="b69a3-296">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="b69a3-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="b69a3-297">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="b69a3-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="b69a3-298">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="b69a3-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="b69a3-299">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="b69a3-300">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="b69a3-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="b69a3-301">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="b69a3-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="b69a3-302">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="b69a3-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="b69a3-303">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="b69a3-304">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="b69a3-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="b69a3-305">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="b69a3-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="b69a3-306">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="b69a3-307">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b69a3-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b69a3-308">Az.StorageSync</span></span>
* <span data-ttu-id="b69a3-309">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="b69a3-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="b69a3-310">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="b69a3-311">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="b69a3-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="b69a3-312">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-313">Az.Websites</span></span>
* <span data-ttu-id="b69a3-314">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="b69a3-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="b69a3-315">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-316">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-317">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="b69a3-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="b69a3-318">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="b69a3-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="b69a3-319">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="b69a3-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="b69a3-320">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="b69a3-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-321">Az.Aks</span></span>
* <span data-ttu-id="b69a3-322">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="b69a3-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-323">Az.Batch</span></span>
* <span data-ttu-id="b69a3-324">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="b69a3-325">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-327">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="b69a3-328">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="b69a3-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-329">Az.Compute</span></span>
* <span data-ttu-id="b69a3-330">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="b69a3-331">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="b69a3-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="b69a3-332">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="b69a3-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="b69a3-333">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="b69a3-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="b69a3-334">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-335">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-336">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-337">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-338">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="b69a3-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b69a3-339">Az.Functions</span></span>
* <span data-ttu-id="b69a3-340">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-341">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-342">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="b69a3-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b69a3-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b69a3-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="b69a3-344">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="b69a3-345">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-346">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-347">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="b69a3-348">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="b69a3-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-349">Az.Network</span></span>
* <span data-ttu-id="b69a3-350">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="b69a3-351">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="b69a3-352">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="b69a3-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="b69a3-353">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="b69a3-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="b69a3-354">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="b69a3-355">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="b69a3-356">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="b69a3-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b69a3-357">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="b69a3-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b69a3-358">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="b69a3-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="b69a3-359">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="b69a3-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="b69a3-360">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="b69a3-361">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="b69a3-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="b69a3-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="b69a3-363">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b69a3-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="b69a3-364">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="b69a3-365">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="b69a3-366">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="b69a3-367">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="b69a3-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="b69a3-368">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="b69a3-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="b69a3-369">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="b69a3-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="b69a3-370">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="b69a3-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="b69a3-371">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="b69a3-372">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="b69a3-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="b69a3-373">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="b69a3-374">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="b69a3-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="b69a3-375">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="b69a3-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="b69a3-376">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="b69a3-377">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="b69a3-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="b69a3-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b69a3-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b69a3-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b69a3-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b69a3-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="b69a3-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="b69a3-384">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="b69a3-385">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="b69a3-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="b69a3-386">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b69a3-387">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b69a3-388">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="b69a3-389">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="b69a3-390">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="b69a3-391">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="b69a3-392">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="b69a3-393">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b69a3-394">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b69a3-395">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="b69a3-396">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="b69a3-397">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="b69a3-398">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-400">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="b69a3-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="b69a3-401">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="b69a3-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="b69a3-402">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="b69a3-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="b69a3-403">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="b69a3-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="b69a3-404">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="b69a3-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-406">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="b69a3-407">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="b69a3-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-408">Az.Resources</span></span>
* <span data-ttu-id="b69a3-409">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="b69a3-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="b69a3-410">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="b69a3-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="b69a3-411">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="b69a3-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="b69a3-412">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="b69a3-413">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="b69a3-414">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-415">Az.Sql</span></span>
* <span data-ttu-id="b69a3-416">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="b69a3-417">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="b69a3-418">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="b69a3-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-419">Az.Storage</span></span>
* <span data-ttu-id="b69a3-420">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="b69a3-421">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-422">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-423">Az.Websites</span></span>
* <span data-ttu-id="b69a3-424">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="b69a3-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b69a3-425">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="b69a3-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="b69a3-426">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="b69a3-427">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="b69a3-428">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="b69a3-429">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="b69a3-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="b69a3-430">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-431">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-432">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="b69a3-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="b69a3-434">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-435">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-436">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="b69a3-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b69a3-437">Az.Billing</span></span>
* <span data-ttu-id="b69a3-438">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-440">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="b69a3-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-441">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-442">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="b69a3-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-443">Az.DataShare</span></span>
* <span data-ttu-id="b69a3-444">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="b69a3-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="b69a3-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="b69a3-446">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-448">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="b69a3-449">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="b69a3-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="b69a3-450">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="b69a3-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="b69a3-451">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="b69a3-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-453">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="b69a3-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b69a3-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b69a3-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b69a3-455">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="b69a3-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="b69a3-456">Az.PrivateDns</span></span>
* <span data-ttu-id="b69a3-457">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="b69a3-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-459">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="b69a3-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="b69a3-460">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-461">Az.Resources</span></span>
* <span data-ttu-id="b69a3-462">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="b69a3-463">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="b69a3-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="b69a3-464">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="b69a3-465">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="b69a3-466">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-467">Az.Sql</span></span>
* <span data-ttu-id="b69a3-468">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="b69a3-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="b69a3-469">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="b69a3-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="b69a3-470">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-471">Az.Storage</span></span>
* <span data-ttu-id="b69a3-472">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="b69a3-473">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b69a3-474">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-474">Highlights since the last release</span></span>
* <span data-ttu-id="b69a3-475">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b69a3-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="b69a3-476">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="b69a3-477">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-478">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-479">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="b69a3-480">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="b69a3-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-481">Az.Aks</span></span>
* <span data-ttu-id="b69a3-482">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="b69a3-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="b69a3-483">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="b69a3-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="b69a3-484">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="b69a3-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-485">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-486">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="b69a3-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="b69a3-487">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="b69a3-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="b69a3-488">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b69a3-489">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="b69a3-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b69a3-490">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b69a3-491">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="b69a3-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="b69a3-492">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b69a3-493">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="b69a3-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b69a3-494">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="b69a3-495">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="b69a3-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="b69a3-496">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="b69a3-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="b69a3-497">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="b69a3-498">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="b69a3-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="b69a3-499">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="b69a3-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="b69a3-500">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="b69a3-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="b69a3-501">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="b69a3-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b69a3-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b69a3-503">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="b69a3-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="b69a3-504">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="b69a3-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="b69a3-505">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-506">Az.Batch</span></span>
* <span data-ttu-id="b69a3-507">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="b69a3-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="b69a3-508">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="b69a3-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="b69a3-509">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="b69a3-510">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="b69a3-511">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="b69a3-512">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="b69a3-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="b69a3-513">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="b69a3-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="b69a3-514">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="b69a3-515">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-516">Az.Compute</span></span>
* <span data-ttu-id="b69a3-517">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="b69a3-518">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="b69a3-519">重大變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-519">Breaking changes</span></span>
    - <span data-ttu-id="b69a3-520">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="b69a3-521">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="b69a3-522">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="b69a3-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="b69a3-523">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="b69a3-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="b69a3-524">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="b69a3-525">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="b69a3-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="b69a3-526">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="b69a3-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-527">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-528">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="b69a3-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-529">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-530">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b69a3-531">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="b69a3-532">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="b69a3-533">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="b69a3-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="b69a3-534">Az.Functions</span></span>
* <span data-ttu-id="b69a3-535">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-536">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-537">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="b69a3-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b69a3-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b69a3-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="b69a3-539">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="b69a3-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-540">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-541">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="b69a3-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="b69a3-542">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="b69a3-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="b69a3-543">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="b69a3-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="b69a3-544">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="b69a3-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="b69a3-545">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="b69a3-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="b69a3-546">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-546">New cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-547">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b69a3-548">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b69a3-549">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="b69a3-550">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="b69a3-551">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="b69a3-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="b69a3-552">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="b69a3-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-553">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-554">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="b69a3-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="b69a3-555">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="b69a3-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="b69a3-556">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="b69a3-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="b69a3-557">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="b69a3-558">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="b69a3-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="b69a3-559">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="b69a3-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="b69a3-560">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="b69a3-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-561">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-562">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="b69a3-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="b69a3-563">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="b69a3-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="b69a3-564">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="b69a3-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="b69a3-565">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="b69a3-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="b69a3-566">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="b69a3-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="b69a3-567">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="b69a3-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="b69a3-568">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="b69a3-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-569">Az.Network</span></span>
* <span data-ttu-id="b69a3-570">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="b69a3-571">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="b69a3-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="b69a3-572">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="b69a3-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="b69a3-573">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="b69a3-574">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="b69a3-575">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-575">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b69a3-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b69a3-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b69a3-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b69a3-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b69a3-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="b69a3-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b69a3-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="b69a3-580">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="b69a3-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="b69a3-581">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="b69a3-582">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="b69a3-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="b69a3-583">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="b69a3-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="b69a3-584">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="b69a3-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="b69a3-585">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="b69a3-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="b69a3-586">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="b69a3-587">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="b69a3-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b69a3-588">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="b69a3-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b69a3-589">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="b69a3-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="b69a3-590">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="b69a3-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="b69a3-591">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="b69a3-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="b69a3-592">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="b69a3-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="b69a3-593">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="b69a3-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b69a3-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-596">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="b69a3-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="b69a3-597">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="b69a3-598">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="b69a3-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="b69a3-599">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="b69a3-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="b69a3-600">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="b69a3-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="b69a3-601">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="b69a3-602">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="b69a3-603">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-605">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="b69a3-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="b69a3-606">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="b69a3-607">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="b69a3-608">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="b69a3-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="b69a3-609">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-610">Az.Resources</span></span>
* <span data-ttu-id="b69a3-611">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="b69a3-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="b69a3-612">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="b69a3-613">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="b69a3-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="b69a3-614">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="b69a3-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="b69a3-615">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="b69a3-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="b69a3-616">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="b69a3-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="b69a3-617">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="b69a3-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="b69a3-618">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="b69a3-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="b69a3-619">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="b69a3-620">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="b69a3-621">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="b69a3-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="b69a3-622">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="b69a3-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="b69a3-623">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="b69a3-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="b69a3-624">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="b69a3-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="b69a3-625">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="b69a3-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="b69a3-626">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="b69a3-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="b69a3-627">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="b69a3-628">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="b69a3-629">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b69a3-630">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="b69a3-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-632">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="b69a3-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-633">Az.Sql</span></span>
* <span data-ttu-id="b69a3-634">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="b69a3-634">Enhance performance of:</span></span>
    - <span data-ttu-id="b69a3-635">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="b69a3-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b69a3-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="b69a3-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b69a3-637">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="b69a3-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b69a3-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="b69a3-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="b69a3-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="b69a3-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b69a3-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="b69a3-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b69a3-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="b69a3-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="b69a3-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="b69a3-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="b69a3-643">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="b69a3-644">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-645">Az.Storage</span></span>
* <span data-ttu-id="b69a3-646">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-647">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="b69a3-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="b69a3-648">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-649">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="b69a3-650">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="b69a3-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b69a3-651">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="b69a3-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="b69a3-652">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="b69a3-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="b69a3-653">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="b69a3-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="b69a3-654">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="b69a3-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="b69a3-655">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="b69a3-656">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="b69a3-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="b69a3-657">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="b69a3-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="b69a3-658">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b69a3-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="b69a3-659">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="b69a3-660">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="b69a3-661">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-662">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="b69a3-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="b69a3-663">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="b69a3-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="b69a3-664">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="b69a3-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b69a3-665">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="b69a3-666">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="b69a3-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="b69a3-667">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="b69a3-668">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="b69a3-669">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="b69a3-670">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b69a3-671">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="b69a3-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="b69a3-672">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="b69a3-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="b69a3-673">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b69a3-674">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="b69a3-675">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="b69a3-676">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b69a3-677">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="b69a3-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="b69a3-678">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="b69a3-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="b69a3-679">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="b69a3-680">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="b69a3-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="b69a3-681">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="b69a3-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="b69a3-682">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="b69a3-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="b69a3-683">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="b69a3-684">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="b69a3-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b69a3-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b69a3-685">Az.TrafficManager</span></span>
* <span data-ttu-id="b69a3-686">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-687">Az.Websites</span></span>
* <span data-ttu-id="b69a3-688">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="b69a3-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="b69a3-689">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="b69a3-690">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-690">Highlights since the last release</span></span>
* <span data-ttu-id="b69a3-691">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="b69a3-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-692">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-693">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="b69a3-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-694">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-695">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="b69a3-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b69a3-696">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-697">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-698">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="b69a3-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-700">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="b69a3-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-701">Az.Compute</span></span>
* <span data-ttu-id="b69a3-702">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="b69a3-703">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="b69a3-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-704">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-705">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-706">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b69a3-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="b69a3-707">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="b69a3-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="b69a3-708">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="b69a3-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="b69a3-709">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-710">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b69a3-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="b69a3-711">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="b69a3-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="b69a3-712">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="b69a3-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="b69a3-713">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-713">New cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-714">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b69a3-715">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b69a3-716">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="b69a3-717">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="b69a3-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="b69a3-718">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="b69a3-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-719">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-720">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="b69a3-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="b69a3-721">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="b69a3-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="b69a3-722">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="b69a3-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="b69a3-723">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="b69a3-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="b69a3-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="b69a3-724">Az.Maintenance</span></span>
* <span data-ttu-id="b69a3-725">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-726">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-727">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="b69a3-728">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b69a3-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b69a3-729">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b69a3-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b69a3-730">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b69a3-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b69a3-731">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="b69a3-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="b69a3-732">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b69a3-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b69a3-733">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b69a3-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="b69a3-734">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="b69a3-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-735">Az.Network</span></span>
* <span data-ttu-id="b69a3-736">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="b69a3-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="b69a3-737">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b69a3-738">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="b69a3-739">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="b69a3-740">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="b69a3-741">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="b69a3-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="b69a3-742">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="b69a3-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="b69a3-743">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="b69a3-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="b69a3-744">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="b69a3-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="b69a3-745">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b69a3-746">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="b69a3-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="b69a3-747">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="b69a3-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="b69a3-748">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="b69a3-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="b69a3-749">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="b69a3-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="b69a3-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="b69a3-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-753">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="b69a3-754">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="b69a3-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-756">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-757">Az.Sql</span></span>
* <span data-ttu-id="b69a3-758">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="b69a3-759">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="b69a3-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-760">Az.Storage</span></span>
* <span data-ttu-id="b69a3-761">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="b69a3-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="b69a3-762">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="b69a3-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="b69a3-763">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="b69a3-764">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="b69a3-765">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="b69a3-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="b69a3-766">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b69a3-767">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b69a3-768">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="b69a3-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="b69a3-769">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b69a3-770">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="b69a3-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="b69a3-771">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="b69a3-772">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="b69a3-773">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="b69a3-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="b69a3-774">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="b69a3-775">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-775">General</span></span>
* <span data-ttu-id="b69a3-776">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="b69a3-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="b69a3-777">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="b69a3-778">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="b69a3-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="b69a3-779">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="b69a3-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="b69a3-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b69a3-780">Az.Billing</span></span>
  - <span data-ttu-id="b69a3-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-781">Az.Compute</span></span>
  - <span data-ttu-id="b69a3-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b69a3-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="b69a3-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-783">Az.EventHub</span></span>
  - <span data-ttu-id="b69a3-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-784">Az.IotHub</span></span>
  - <span data-ttu-id="b69a3-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-785">Az.KeyVault</span></span>
  - <span data-ttu-id="b69a3-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-786">Az.Monitor</span></span>
  - <span data-ttu-id="b69a3-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-787">Az.Network</span></span>
  - <span data-ttu-id="b69a3-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-788">Az.Resources</span></span>
  - <span data-ttu-id="b69a3-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-789">Az.Storage</span></span>
  - <span data-ttu-id="b69a3-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-790">Az.Websites</span></span>
* <span data-ttu-id="b69a3-791">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="b69a3-792">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="b69a3-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="b69a3-793">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="b69a3-794">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-795">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-796">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="b69a3-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-797">Az.Compute</span></span>
* <span data-ttu-id="b69a3-798">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="b69a3-799">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="b69a3-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="b69a3-800">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="b69a3-801">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="b69a3-802">[#11354]</span><span class="sxs-lookup"><span data-stu-id="b69a3-802">[#11354]</span></span>
* <span data-ttu-id="b69a3-803">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="b69a3-804">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="b69a3-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b69a3-805">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="b69a3-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b69a3-806">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="b69a3-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="b69a3-807">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="b69a3-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="b69a3-808">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="b69a3-809">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="b69a3-810">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="b69a3-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="b69a3-811">[#11257]</span><span class="sxs-lookup"><span data-stu-id="b69a3-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-812">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-813">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="b69a3-814">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="b69a3-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-816">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="b69a3-817">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="b69a3-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-818">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-819">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-820">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-821">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="b69a3-822">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-823">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="b69a3-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="b69a3-824">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="b69a3-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-825">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-826">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="b69a3-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-827">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-828">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-829">Az.Network</span></span>
* <span data-ttu-id="b69a3-830">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="b69a3-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="b69a3-831">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b69a3-832">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="b69a3-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="b69a3-833">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="b69a3-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="b69a3-834">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="b69a3-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="b69a3-835">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-837">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-839">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="b69a3-840">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="b69a3-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="b69a3-841">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="b69a3-842">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="b69a3-843">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="b69a3-844">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-845">Az.Resources</span></span>
* <span data-ttu-id="b69a3-846">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="b69a3-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="b69a3-847">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="b69a3-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="b69a3-848">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="b69a3-849">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-849">Added example.</span></span>
* <span data-ttu-id="b69a3-850">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="b69a3-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="b69a3-851">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-852">Az.Sql</span></span>
* <span data-ttu-id="b69a3-853">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="b69a3-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="b69a3-854">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="b69a3-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="b69a3-855">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="b69a3-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="b69a3-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="b69a3-856">Az.Support</span></span>
* <span data-ttu-id="b69a3-857">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-858">Az.Websites</span></span>
* <span data-ttu-id="b69a3-859">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="b69a3-860">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="b69a3-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b69a3-861">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="b69a3-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b69a3-862">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="b69a3-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="b69a3-863">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="b69a3-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="b69a3-864">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-865">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-866">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="b69a3-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="b69a3-867">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="b69a3-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="b69a3-868">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-869">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-870">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="b69a3-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="b69a3-871">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="b69a3-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="b69a3-872">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="b69a3-873">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="b69a3-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-875">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="b69a3-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-876">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-877">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b69a3-878">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-879">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-880">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-881">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-882">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="b69a3-883">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="b69a3-884">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-885">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="b69a3-886">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="b69a3-887">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="b69a3-888">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="b69a3-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="b69a3-889">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="b69a3-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b69a3-890">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="b69a3-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="b69a3-891">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="b69a3-892">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-893">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="b69a3-894">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="b69a3-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="b69a3-895">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-896">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-897">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="b69a3-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-898">Az.Network</span></span>
* <span data-ttu-id="b69a3-899">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="b69a3-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="b69a3-900">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="b69a3-901">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="b69a3-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="b69a3-902">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-903">Az.Resources</span></span>
* <span data-ttu-id="b69a3-904">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="b69a3-905">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="b69a3-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="b69a3-906">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="b69a3-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="b69a3-907">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="b69a3-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="b69a3-908">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="b69a3-909">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="b69a3-910">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="b69a3-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="b69a3-911">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="b69a3-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b69a3-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="b69a3-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="b69a3-915">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="b69a3-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="b69a3-917">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="b69a3-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-918">Az.Sql</span></span>
* <span data-ttu-id="b69a3-919">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="b69a3-920">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="b69a3-921">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="b69a3-922">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="b69a3-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="b69a3-923">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="b69a3-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="b69a3-924">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="b69a3-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="b69a3-925">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b69a3-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="b69a3-926">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="b69a3-927">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-928">Az.Storage</span></span>
* <span data-ttu-id="b69a3-929">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="b69a3-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="b69a3-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="b69a3-931">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="b69a3-932">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="b69a3-933">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="b69a3-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-934">Az.Websites</span></span>
* <span data-ttu-id="b69a3-935">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="b69a3-936">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="b69a3-937">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="b69a3-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="b69a3-938">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="b69a3-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="b69a3-939">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="b69a3-940">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-941">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-941">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-942">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="b69a3-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="b69a3-943">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="b69a3-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="b69a3-944">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-945">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-946">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="b69a3-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-947">Az.Automation</span></span>
* <span data-ttu-id="b69a3-948">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-950">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="b69a3-951">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-952">Az.Compute</span></span>
* <span data-ttu-id="b69a3-953">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="b69a3-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-954">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-955">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="b69a3-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-956">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-957">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="b69a3-958">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-959">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-960">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-961">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="b69a3-962">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="b69a3-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-963">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-964">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="b69a3-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-965">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-966">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="b69a3-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="b69a3-967">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="b69a3-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="b69a3-968">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-969">Az.Network</span></span>
* <span data-ttu-id="b69a3-970">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="b69a3-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="b69a3-971">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b69a3-972">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="b69a3-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="b69a3-973">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="b69a3-974">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-974">No new cmdlets are added.</span></span> <span data-ttu-id="b69a3-975">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="b69a3-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-977">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-978">Az.Resources</span></span>
* <span data-ttu-id="b69a3-979">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="b69a3-980">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b69a3-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="b69a3-981">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b69a3-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="b69a3-982">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="b69a3-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="b69a3-983">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="b69a3-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="b69a3-984">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="b69a3-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="b69a3-985">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="b69a3-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="b69a3-986">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="b69a3-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-987">Az.Sql</span></span>
* <span data-ttu-id="b69a3-988">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="b69a3-989">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="b69a3-990">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="b69a3-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b69a3-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b69a3-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b69a3-992">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b69a3-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b69a3-993">Az.StorageSync</span></span>
* <span data-ttu-id="b69a3-994">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="b69a3-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="b69a3-995">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-996">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-996">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-997">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="b69a3-998">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="b69a3-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-999">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1000">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="b69a3-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="b69a3-1001">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="b69a3-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-1003">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="b69a3-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="b69a3-1004">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="b69a3-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="b69a3-1005">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="b69a3-1006">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="b69a3-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1007">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1008">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="b69a3-1009">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="b69a3-1010">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="b69a3-1011">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="b69a3-1012">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1013">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1014">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b69a3-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b69a3-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="b69a3-1016">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="b69a3-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="b69a3-1017">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-1018">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-1019">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-1020">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-1021">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1022">Az.Network</span></span>
* <span data-ttu-id="b69a3-1023">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="b69a3-1024">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="b69a3-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="b69a3-1025">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1026">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="b69a3-1027">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="b69a3-1028">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="b69a3-1029">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="b69a3-1030">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="b69a3-1031">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="b69a3-1033">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="b69a3-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="b69a3-1035">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-1037">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="b69a3-1038">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="b69a3-1039">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="b69a3-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="b69a3-1040">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b69a3-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1042">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="b69a3-1043">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1044">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1045">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="b69a3-1046">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1047">Az.Sql</span></span>
<span data-ttu-id="b69a3-1048">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1049">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1050">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="b69a3-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="b69a3-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="b69a3-1052">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="b69a3-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="b69a3-1053">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="b69a3-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1054">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1055">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="b69a3-1056">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="b69a3-1057">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1058">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1059">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-1060">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-1061">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="b69a3-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1062">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1063">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b69a3-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="b69a3-1065">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b69a3-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b69a3-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b69a3-1067">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b69a3-1068">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="b69a3-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="b69a3-1069">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b69a3-1070">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="b69a3-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="b69a3-1071">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b69a3-1072">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="b69a3-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="b69a3-1073">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="b69a3-1074">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="b69a3-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="b69a3-1075">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b69a3-1076">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="b69a3-1077">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b69a3-1078">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="b69a3-1079">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="b69a3-1080">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="b69a3-1081">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="b69a3-1082">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="b69a3-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="b69a3-1083">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="b69a3-1084">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="b69a3-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1085">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1086">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="b69a3-1087">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="b69a3-1088">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="b69a3-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b69a3-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="b69a3-1090">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1091">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-1092">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="b69a3-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-1093">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-1094">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b69a3-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b69a3-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="b69a3-1096">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="b69a3-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b69a3-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="b69a3-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="b69a3-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b69a3-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="b69a3-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b69a3-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="b69a3-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b69a3-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="b69a3-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="b69a3-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="b69a3-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1104">Az.Network</span></span>
* <span data-ttu-id="b69a3-1105">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="b69a3-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1107">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="b69a3-1108">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b69a3-1109">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="b69a3-1110">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1111">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1112">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1113">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1114">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="b69a3-1115">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="b69a3-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b69a3-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="b69a3-1117">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1118">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1119">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="b69a3-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="b69a3-1121">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="b69a3-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="b69a3-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="b69a3-1123">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="b69a3-1124">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-1124">General</span></span>
* <span data-ttu-id="b69a3-1125">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="b69a3-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1126">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1127">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="b69a3-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="b69a3-1128">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-1129">Az.Batch</span></span>
* <span data-ttu-id="b69a3-1130">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1131">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1132">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-1134">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="b69a3-1135">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="b69a3-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b69a3-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b69a3-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="b69a3-1137">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-1138">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-1139">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="b69a3-1140">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="b69a3-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="b69a3-1141">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1142">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-1143">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="b69a3-1144">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="b69a3-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="b69a3-1145">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1146">Az.Network</span></span>
* <span data-ttu-id="b69a3-1147">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1148">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1149">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="b69a3-1150">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1151">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1152">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="b69a3-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1153">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1154">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="b69a3-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b69a3-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="b69a3-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b69a3-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="b69a3-1157">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="b69a3-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="b69a3-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="b69a3-1159">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="b69a3-1160">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="b69a3-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="b69a3-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="b69a3-1163">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="b69a3-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b69a3-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="b69a3-1165">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="b69a3-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b69a3-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="b69a3-1167">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-1168">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-1169">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="b69a3-1170">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1171">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1172">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="b69a3-1173">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="b69a3-1174">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="b69a3-1175">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b69a3-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="b69a3-1176">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="b69a3-1177">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="b69a3-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b69a3-1178">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="b69a3-1179">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="b69a3-1180">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="b69a3-1181">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="b69a3-1182">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="b69a3-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="b69a3-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="b69a3-1184">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b69a3-1185">取得訂單</span><span class="sxs-lookup"><span data-stu-id="b69a3-1185">Get the Order</span></span>
* <span data-ttu-id="b69a3-1186">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b69a3-1187">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="b69a3-1187">Create new Order</span></span>
* <span data-ttu-id="b69a3-1188">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="b69a3-1189">移除訂單</span><span class="sxs-lookup"><span data-stu-id="b69a3-1189">Remove the Order</span></span>
* <span data-ttu-id="b69a3-1190">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="b69a3-1191">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="b69a3-1191">Now creates Local Share</span></span>
* <span data-ttu-id="b69a3-1192">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="b69a3-1193">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="b69a3-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="b69a3-1194">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="b69a3-1195">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="b69a3-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="b69a3-1196">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b69a3-1197">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="b69a3-1198">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b69a3-1199">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="b69a3-1199">Create new Triggers</span></span>
* <span data-ttu-id="b69a3-1200">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="b69a3-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="b69a3-1201">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="b69a3-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1202">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1203">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="b69a3-1204">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-1206">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1207">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-1208">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="b69a3-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-1210">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="b69a3-1211">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="b69a3-1212">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="b69a3-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="b69a3-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1214">Az.Network</span></span>
* <span data-ttu-id="b69a3-1215">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="b69a3-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="b69a3-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="b69a3-1217">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="b69a3-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1219">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="b69a3-1220">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="b69a3-1221">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="b69a3-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b69a3-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b69a3-1222">Az.RedisCache</span></span>
* <span data-ttu-id="b69a3-1223">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="b69a3-1224">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="b69a3-1225">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1226">Az.Resources</span></span>
- <span data-ttu-id="b69a3-1227">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="b69a3-1228">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="b69a3-1229">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="b69a3-1230">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="b69a3-1231">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1232">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1233">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="b69a3-1234">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b69a3-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="b69a3-1235">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="b69a3-1236">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-1236">General</span></span>
* <span data-ttu-id="b69a3-1237">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1238">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1239">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b69a3-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1240">Az.Advisor</span></span>
* <span data-ttu-id="b69a3-1241">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-1242">Az.Batch</span></span>
* <span data-ttu-id="b69a3-1243">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="b69a3-1244">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="b69a3-1245">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="b69a3-1246">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="b69a3-1247">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="b69a3-1248">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="b69a3-1249">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="b69a3-1250">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="b69a3-1251">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="b69a3-1252">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b69a3-1253">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="b69a3-1254">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="b69a3-1255">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="b69a3-1256">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="b69a3-1257">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="b69a3-1258">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="b69a3-1259">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="b69a3-1260">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="b69a3-1261">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="b69a3-1262">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="b69a3-1263">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b69a3-1264">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="b69a3-1265">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="b69a3-1266">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="b69a3-1267">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="b69a3-1268">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="b69a3-1269">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="b69a3-1270">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="b69a3-1271">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="b69a3-1272">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="b69a3-1273">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="b69a3-1274">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="b69a3-1275">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="b69a3-1276">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="b69a3-1277">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="b69a3-1278">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-1279">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-1280">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="b69a3-1281">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1282">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1283">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="b69a3-1284">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="b69a3-1285">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b69a3-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="b69a3-1286">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b69a3-1287">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="b69a3-1288">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="b69a3-1289">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="b69a3-1290">重大變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-1290">Breaking changes</span></span>
    - <span data-ttu-id="b69a3-1291">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b69a3-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="b69a3-1292">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="b69a3-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1293">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1294">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-1296">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="b69a3-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="b69a3-1297">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="b69a3-1298">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="b69a3-1299">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="b69a3-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="b69a3-1300">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="b69a3-1301">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-1303">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-1304">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-1305">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="b69a3-1306">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="b69a3-1307">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="b69a3-1308">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="b69a3-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b69a3-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b69a3-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b69a3-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b69a3-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="b69a3-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="b69a3-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b69a3-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="b69a3-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b69a3-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="b69a3-1314">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="b69a3-1315">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b69a3-1316">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="b69a3-1317">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="b69a3-1318">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="b69a3-1319">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="b69a3-1320">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="b69a3-1321">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="b69a3-1322">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="b69a3-1323">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="b69a3-1324">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="b69a3-1325">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="b69a3-1326">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="b69a3-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1327">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-1328">重大變更：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1328">Breaking changes:</span></span>
    - <span data-ttu-id="b69a3-1329">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b69a3-1330">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b69a3-1331">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b69a3-1332">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b69a3-1333">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="b69a3-1334">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="b69a3-1335">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="b69a3-1336">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="b69a3-1337">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b69a3-1338">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="b69a3-1339">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="b69a3-1340">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1342">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1343">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="b69a3-1344">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="b69a3-1345">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1346">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1347">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1348">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1349">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-1350">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="b69a3-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1351">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1352">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="b69a3-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1353">Az.Network</span></span>
* <span data-ttu-id="b69a3-1354">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="b69a3-1355">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b69a3-1361">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="b69a3-1362">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1362">New cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="b69a3-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="b69a3-1364">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="b69a3-1365">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="b69a3-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="b69a3-1366">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="b69a3-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="b69a3-1367">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="b69a3-1368">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="b69a3-1369">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="b69a3-1370">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="b69a3-1371">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="b69a3-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b69a3-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b69a3-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="b69a3-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="b69a3-1377">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="b69a3-1378">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b69a3-1379">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="b69a3-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b69a3-1380">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="b69a3-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="b69a3-1381">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="b69a3-1382">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="b69a3-1383">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="b69a3-1384">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="b69a3-1386">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b69a3-1387">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b69a3-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b69a3-1388">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b69a3-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b69a3-1389">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b69a3-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b69a3-1390">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b69a3-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="b69a3-1391">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b69a3-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="b69a3-1392">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="b69a3-1393">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="b69a3-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="b69a3-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="b69a3-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="b69a3-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b69a3-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="b69a3-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="b69a3-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="b69a3-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="b69a3-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="b69a3-1400">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b69a3-1401">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="b69a3-1402">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="b69a3-1403">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="b69a3-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="b69a3-1404">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="b69a3-1405">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="b69a3-1406">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b69a3-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="b69a3-1407">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b69a3-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="b69a3-1408">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="b69a3-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="b69a3-1409">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="b69a3-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="b69a3-1410">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="b69a3-1411">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="b69a3-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="b69a3-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="b69a3-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-1417">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1418">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1419">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="b69a3-1420">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="b69a3-1421">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="b69a3-1422">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="b69a3-1423">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="b69a3-1424">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b69a3-1425">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="b69a3-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="b69a3-1426">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="b69a3-1427">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1428">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1429">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="b69a3-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="b69a3-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b69a3-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b69a3-1432">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="b69a3-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="b69a3-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b69a3-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="b69a3-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b69a3-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="b69a3-1435">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="b69a3-1436">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-1436">General</span></span>
* <span data-ttu-id="b69a3-1437">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1438">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1439">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-1441">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="b69a3-1442">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1443">Az.Automation</span></span>
* <span data-ttu-id="b69a3-1444">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-1445">Az.Batch</span></span>
* <span data-ttu-id="b69a3-1446">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1447">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1448">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b69a3-1449">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="b69a3-1450">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="b69a3-1451">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1452">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1453">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="b69a3-1454">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="b69a3-1455">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-1457">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b69a3-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b69a3-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="b69a3-1459">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="b69a3-1460">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="b69a3-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="b69a3-1461">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="b69a3-1462">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1463">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-1464">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="b69a3-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="b69a3-1465">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="b69a3-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1466">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-1467">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b69a3-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="b69a3-1468">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="b69a3-1469">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="b69a3-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="b69a3-1470">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1471">Az.Network</span></span>
* <span data-ttu-id="b69a3-1472">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="b69a3-1473">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="b69a3-1474">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="b69a3-1476">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b69a3-1477">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="b69a3-1478">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="b69a3-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b69a3-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b69a3-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b69a3-1482">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="b69a3-1483">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="b69a3-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="b69a3-1484">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="b69a3-1485">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b69a3-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b69a3-1486">Az.RedisCache</span></span>
* <span data-ttu-id="b69a3-1487">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="b69a3-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1488">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1489">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1490">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1491">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="b69a3-1492">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="b69a3-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b69a3-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b69a3-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="b69a3-1494">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="b69a3-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b69a3-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b69a3-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b69a3-1496">Az.StorageSync</span></span>
* <span data-ttu-id="b69a3-1497">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1498">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1499">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="b69a3-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="b69a3-1500">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-1502">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="b69a3-1503">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="b69a3-1504">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1505">Az.Automation</span></span>
* <span data-ttu-id="b69a3-1506">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="b69a3-1507">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="b69a3-1508">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1509">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1510">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="b69a3-1511">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b69a3-1512">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="b69a3-1513">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="b69a3-1514">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="b69a3-1515">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="b69a3-1516">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="b69a3-1517">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="b69a3-1518">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1519">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1520">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b69a3-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="b69a3-1521">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="b69a3-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-1522">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-1523">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1524">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-1525">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="b69a3-1526">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="b69a3-1527">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="b69a3-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b69a3-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b69a3-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b69a3-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b69a3-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b69a3-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b69a3-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b69a3-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1532">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-1533">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="b69a3-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="b69a3-1534">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="b69a3-1535">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="b69a3-1536">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="b69a3-1537">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="b69a3-1538">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="b69a3-1539">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="b69a3-1540">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="b69a3-1541">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b69a3-1542">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="b69a3-1543">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b69a3-1544">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="b69a3-1545">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="b69a3-1546">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="b69a3-1547">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="b69a3-1548">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="b69a3-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="b69a3-1549">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="b69a3-1550">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="b69a3-1551">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="b69a3-1552">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="b69a3-1552">Overall improved help files</span></span>
* <span data-ttu-id="b69a3-1553">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1554">Az.Network</span></span>
* <span data-ttu-id="b69a3-1555">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="b69a3-1556">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="b69a3-1557">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="b69a3-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="b69a3-1558">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="b69a3-1559">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="b69a3-1560">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="b69a3-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="b69a3-1561">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="b69a3-1562">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="b69a3-1563">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="b69a3-1564">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="b69a3-1565">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="b69a3-1566">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="b69a3-1567">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1567">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b69a3-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="b69a3-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="b69a3-1570">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b69a3-1571">New-VpnSite</span></span>
        - <span data-ttu-id="b69a3-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b69a3-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="b69a3-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="b69a3-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="b69a3-1575">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1577">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="b69a3-1578">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="b69a3-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1579">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1580">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-1582">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="b69a3-1583">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="b69a3-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b69a3-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b69a3-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b69a3-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b69a3-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b69a3-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="b69a3-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b69a3-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b69a3-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b69a3-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b69a3-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b69a3-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b69a3-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b69a3-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="b69a3-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b69a3-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b69a3-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b69a3-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b69a3-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b69a3-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="b69a3-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="b69a3-1597">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b69a3-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b69a3-1598">Az.SignalR</span></span>
* <span data-ttu-id="b69a3-1599">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1600">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1601">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="b69a3-1602">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="b69a3-1603">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="b69a3-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b69a3-1604">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="b69a3-1605">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1606">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1607">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b69a3-1608">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="b69a3-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="b69a3-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="b69a3-1611">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="b69a3-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="b69a3-1613">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="b69a3-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="b69a3-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b69a3-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b69a3-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b69a3-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b69a3-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1618">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1619">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="b69a3-1620">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="b69a3-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="b69a3-1621">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="b69a3-1622">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b69a3-1623">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-1623">General</span></span>
* <span data-ttu-id="b69a3-1624">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1625">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1626">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-1627">Az.Aks</span></span>
* <span data-ttu-id="b69a3-1628">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b69a3-1629">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b69a3-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-1631">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b69a3-1632">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="b69a3-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b69a3-1633">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b69a3-1634">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b69a3-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b69a3-1635">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-1636">Az.Batch</span></span>
* <span data-ttu-id="b69a3-1637">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="b69a3-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-1638">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-1639">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1640">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1641">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b69a3-1642">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="b69a3-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b69a3-1643">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="b69a3-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b69a3-1644">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="b69a3-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b69a3-1645">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b69a3-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b69a3-1646">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="b69a3-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b69a3-1647">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b69a3-1648">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1649">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1650">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="b69a3-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b69a3-1651">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="b69a3-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b69a3-1652">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="b69a3-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b69a3-1653">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-1655">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1656">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-1657">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b69a3-1658">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="b69a3-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b69a3-1659">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b69a3-1660">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b69a3-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b69a3-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b69a3-1662">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1663">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-1664">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1665">Az.Network</span></span>
* <span data-ttu-id="b69a3-1666">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b69a3-1667">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b69a3-1668">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b69a3-1669">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b69a3-1670">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="b69a3-1671">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b69a3-1672">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-1674">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b69a3-1675">新增了範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1675">Added example</span></span>
    - <span data-ttu-id="b69a3-1676">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b69a3-1677">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b69a3-1678">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1680">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1681">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1682">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b69a3-1683">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b69a3-1684">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="b69a3-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b69a3-1685">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-1687">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b69a3-1688">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b69a3-1689">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-1691">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b69a3-1692">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b69a3-1693">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b69a3-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b69a3-1694">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b69a3-1695">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b69a3-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b69a3-1696">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1697">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1698">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1699">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1700">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b69a3-1701">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="b69a3-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b69a3-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b69a3-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b69a3-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b69a3-1704">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="b69a3-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b69a3-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b69a3-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1706">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1707">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="b69a3-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b69a3-1708">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1709">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1710">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b69a3-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b69a3-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b69a3-1712">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1713">Az.Automation</span></span>
* <span data-ttu-id="b69a3-1714">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-1716">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1717">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1718">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b69a3-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b69a3-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b69a3-1720">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b69a3-1721">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b69a3-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1722">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1723">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b69a3-1724">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1725">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-1726">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b69a3-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b69a3-1727">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-1728">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-1729">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b69a3-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b69a3-1730">Az.LogicApp</span></span>
* <span data-ttu-id="b69a3-1731">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b69a3-1732">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b69a3-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="b69a3-1734">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1735">Az.Network</span></span>
* <span data-ttu-id="b69a3-1736">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b69a3-1737">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1737">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b69a3-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b69a3-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b69a3-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b69a3-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b69a3-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b69a3-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b69a3-1746">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="b69a3-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b69a3-1747">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b69a3-1748">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="b69a3-1749">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b69a3-1750">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="b69a3-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b69a3-1751">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="b69a3-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b69a3-1752">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="b69a3-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b69a3-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b69a3-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b69a3-1756">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b69a3-1757">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b69a3-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b69a3-1758">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b69a3-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b69a3-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b69a3-1762">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="b69a3-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b69a3-1763">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b69a3-1764">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-1766">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="b69a3-1767">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1769">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b69a3-1770">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b69a3-1771">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b69a3-1772">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b69a3-1773">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b69a3-1774">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b69a3-1775">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b69a3-1776">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b69a3-1777">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="b69a3-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b69a3-1778">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="b69a3-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1779">Az.Resources</span></span>
- <span data-ttu-id="b69a3-1780">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b69a3-1781">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b69a3-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-1783">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b69a3-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b69a3-1784">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1785">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1786">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b69a3-1787">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b69a3-1788">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1789">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1790">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b69a3-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b69a3-1791">Az.StorageSync</span></span>
* <span data-ttu-id="b69a3-1792">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b69a3-1793">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="b69a3-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1794">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1795">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b69a3-1796">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b69a3-1797">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b69a3-1798">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1799">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1800">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b69a3-1801">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b69a3-1802">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b69a3-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1803">Az.Advisor</span></span>
* <span data-ttu-id="b69a3-1804">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b69a3-1805">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="b69a3-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-1807">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b69a3-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b69a3-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b69a3-1809">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b69a3-1810">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b69a3-1811">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b69a3-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b69a3-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b69a3-1813">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-1814">Az.Automation</span></span>
* <span data-ttu-id="b69a3-1815">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1816">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1817">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-1818">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-1819">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b69a3-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b69a3-1820">Az.EventGrid</span></span>
* <span data-ttu-id="b69a3-1821">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1822">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-1823">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1824">Az.Network</span></span>
* <span data-ttu-id="b69a3-1825">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="b69a3-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b69a3-1826">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-1828">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b69a3-1829">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b69a3-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-1831">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="b69a3-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1833">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="b69a3-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1834">Az.Resources</span></span>
    - <span data-ttu-id="b69a3-1835">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b69a3-1836">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b69a3-1837">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b69a3-1838">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="b69a3-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-1840">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="b69a3-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1841">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1842">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b69a3-1843">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b69a3-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b69a3-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b69a3-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b69a3-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b69a3-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b69a3-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b69a3-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b69a3-1850">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="b69a3-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1851">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1852">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b69a3-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b69a3-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b69a3-1854">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b69a3-1855">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b69a3-1856">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="b69a3-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b69a3-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b69a3-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b69a3-1859">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="b69a3-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b69a3-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b69a3-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b69a3-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b69a3-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b69a3-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b69a3-1862">Az.StorageSync</span></span>
* <span data-ttu-id="b69a3-1863">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="b69a3-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b69a3-1864">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-1865">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-1866">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b69a3-1867">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b69a3-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b69a3-1868">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b69a3-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b69a3-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b69a3-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b69a3-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1871">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1872">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b69a3-1873">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b69a3-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b69a3-1874">Az.Dns</span></span>
* <span data-ttu-id="b69a3-1875">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b69a3-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b69a3-1876">Az.EventGrid</span></span>
* <span data-ttu-id="b69a3-1877">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b69a3-1878">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1878">New cmdlets:</span></span>
    - <span data-ttu-id="b69a3-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b69a3-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b69a3-1880">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b69a3-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b69a3-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b69a3-1882">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b69a3-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b69a3-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b69a3-1884">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b69a3-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b69a3-1886">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b69a3-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b69a3-1888">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b69a3-1889">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b69a3-1890">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b69a3-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b69a3-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b69a3-1892">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="b69a3-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="b69a3-1893">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b69a3-1894">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b69a3-1895">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="b69a3-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b69a3-1897">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b69a3-1898">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b69a3-1899">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b69a3-1900">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b69a3-1901">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="b69a3-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b69a3-1902">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b69a3-1903">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b69a3-1904">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="b69a3-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="b69a3-1905">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b69a3-1906">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b69a3-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b69a3-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b69a3-1908">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b69a3-1909">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b69a3-1912">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="b69a3-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b69a3-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b69a3-1914">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="b69a3-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1915">Az.Network</span></span>
* <span data-ttu-id="b69a3-1916">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b69a3-1917">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1917">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b69a3-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b69a3-1919">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b69a3-1920">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1920">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b69a3-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b69a3-1922">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b69a3-1923">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1923">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b69a3-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b69a3-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b69a3-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b69a3-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b69a3-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b69a3-1929">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b69a3-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b69a3-1930">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-1930">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b69a3-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b69a3-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b69a3-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b69a3-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b69a3-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b69a3-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b69a3-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b69a3-1935">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="b69a3-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b69a3-1936">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b69a3-1937">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b69a3-1938">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b69a3-1939">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b69a3-1940">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="b69a3-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b69a3-1941">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b69a3-1942">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b69a3-1943">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b69a3-1944">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="b69a3-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b69a3-1945">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="b69a3-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b69a3-1946">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b69a3-1947">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="b69a3-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b69a3-1948">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b69a3-1949">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b69a3-1950">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b69a3-1951">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="b69a3-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b69a3-1952">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="b69a3-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b69a3-1953">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="b69a3-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="b69a3-1954">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="b69a3-1955">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b69a3-1956">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b69a3-1957">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-1959">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="b69a3-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-1960">Az.Resources</span></span>
* <span data-ttu-id="b69a3-1961">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="b69a3-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b69a3-1962">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b69a3-1963">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b69a3-1964">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="b69a3-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-1966">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-1967">Az.Sql</span></span>
* <span data-ttu-id="b69a3-1968">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="b69a3-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b69a3-1969">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b69a3-1970">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="b69a3-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b69a3-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b69a3-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b69a3-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b69a3-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b69a3-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b69a3-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b69a3-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b69a3-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-1976">Az.Storage</span></span>
* <span data-ttu-id="b69a3-1977">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="b69a3-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b69a3-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="b69a3-1979">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b69a3-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-1981">Az.Websites</span></span>
* <span data-ttu-id="b69a3-1982">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="b69a3-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b69a3-1983">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b69a3-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b69a3-1984">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b69a3-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-1985">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-1986">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-1987">Az.Compute</span></span>
* <span data-ttu-id="b69a3-1988">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="b69a3-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b69a3-1989">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b69a3-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-1990">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-1991">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="b69a3-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b69a3-1992">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69a3-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-1993">Az.Network</span></span>
* <span data-ttu-id="b69a3-1994">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b69a3-1995">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="b69a3-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-1997">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-1999">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="b69a3-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-2001">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69a3-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-2003">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b69a3-2004">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2005">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2006">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b69a3-2007">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b69a3-2008">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="b69a3-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b69a3-2009">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2010">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2011">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b69a3-2012">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b69a3-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-2014">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="b69a3-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b69a3-2015">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="b69a3-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b69a3-2016">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="b69a3-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b69a3-2017">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b69a3-2018">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b69a3-2019">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b69a3-2020">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="b69a3-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b69a3-2021">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="b69a3-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b69a3-2022">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="b69a3-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b69a3-2023">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="b69a3-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b69a3-2024">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="b69a3-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b69a3-2025">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="b69a3-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b69a3-2026">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="b69a3-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b69a3-2027">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b69a3-2028">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b69a3-2029">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b69a3-2030">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b69a3-2031">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b69a3-2032">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="b69a3-2033">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="b69a3-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b69a3-2034">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="b69a3-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b69a3-2035">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b69a3-2036">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b69a3-2037">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="b69a3-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="b69a3-2038">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b69a3-2039">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b69a3-2040">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b69a3-2041">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b69a3-2042">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b69a3-2043">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="b69a3-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b69a3-2044">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="b69a3-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b69a3-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b69a3-2046">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="b69a3-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b69a3-2047">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b69a3-2048">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="b69a3-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b69a3-2049">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b69a3-2050">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b69a3-2051">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b69a3-2052">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b69a3-2053">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b69a3-2054">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b69a3-2055">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="b69a3-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b69a3-2056">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b69a3-2057">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b69a3-2058">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b69a3-2059">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b69a3-2060">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="b69a3-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b69a3-2061">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b69a3-2062">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b69a3-2063">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b69a3-2064">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b69a3-2065">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b69a3-2066">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b69a3-2067">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b69a3-2068">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b69a3-2069">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b69a3-2070">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b69a3-2071">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="b69a3-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b69a3-2072">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="b69a3-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b69a3-2073">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b69a3-2074">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b69a3-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b69a3-2075">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="b69a3-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b69a3-2076">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="b69a3-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b69a3-2077">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b69a3-2078">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="b69a3-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b69a3-2079">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b69a3-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b69a3-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b69a3-2081">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b69a3-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b69a3-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b69a3-2083">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b69a3-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b69a3-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b69a3-2085">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b69a3-2086">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b69a3-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b69a3-2088">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="b69a3-2089">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b69a3-2090">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2091">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2092">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b69a3-2093">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b69a3-2094">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b69a3-2095">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b69a3-2096">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b69a3-2097">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b69a3-2098">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2099">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2100">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b69a3-2101">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="b69a3-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2103">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="b69a3-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2104">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-2105">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2106">Az.Network</span></span>
* <span data-ttu-id="b69a3-2107">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="b69a3-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b69a3-2108">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="b69a3-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b69a3-2110">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="b69a3-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2111">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2112">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="b69a3-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2113">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2114">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="b69a3-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b69a3-2115">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2116">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2117">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-2119">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b69a3-2120">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2121">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2122">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b69a3-2123">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b69a3-2124">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b69a3-2125">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b69a3-2126">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b69a3-2127">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b69a3-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="b69a3-2128">重大變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-2128">Breaking changes</span></span>
    - <span data-ttu-id="b69a3-2129">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b69a3-2130">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b69a3-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b69a3-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="b69a3-2132">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b69a3-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b69a3-2133">Az.Dns</span></span>
* <span data-ttu-id="b69a3-2134">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="b69a3-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b69a3-2135">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b69a3-2136">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="b69a3-2138">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b69a3-2139">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-2140">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-2141">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b69a3-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b69a3-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b69a3-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b69a3-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b69a3-2144">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b69a3-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b69a3-2145">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b69a3-2146">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b69a3-2147">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2148">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-2149">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="b69a3-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b69a3-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b69a3-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b69a3-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b69a3-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b69a3-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b69a3-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b69a3-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b69a3-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b69a3-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b69a3-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b69a3-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b69a3-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b69a3-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b69a3-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b69a3-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b69a3-2161">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b69a3-2162">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2163">Az.Network</span></span>
* <span data-ttu-id="b69a3-2164">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b69a3-2165">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2165">New cmdlets</span></span>
        - <span data-ttu-id="b69a3-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b69a3-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="b69a3-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b69a3-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b69a3-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b69a3-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b69a3-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b69a3-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b69a3-2170">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="b69a3-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b69a3-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b69a3-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b69a3-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b69a3-2173">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b69a3-2174">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b69a3-2175">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-2177">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b69a3-2178">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b69a3-2179">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-2181">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b69a3-2182">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b69a3-2183">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b69a3-2184">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b69a3-2185">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b69a3-2186">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b69a3-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b69a3-2187">Az.Relay</span></span>
* <span data-ttu-id="b69a3-2188">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-2190">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2191">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2192">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="b69a3-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b69a3-2193">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b69a3-2194">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b69a3-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="b69a3-2196">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b69a3-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b69a3-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b69a3-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2200">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2201">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b69a3-2202">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="b69a3-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b69a3-2203">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-2204">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-2205">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="b69a3-2206">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b69a3-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b69a3-2207">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b69a3-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b69a3-2208">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b69a3-2209">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b69a3-2210">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b69a3-2211">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2212">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2213">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="b69a3-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b69a3-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-2214">Az.Batch</span></span>
* <span data-ttu-id="b69a3-2215">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-2216">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-2217">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-2219">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2220">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2221">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b69a3-2222">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2223">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-2224">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-2225">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2227">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b69a3-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b69a3-2228">Az.EventGrid</span></span>
* <span data-ttu-id="b69a3-2229">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-2230">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-2231">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b69a3-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b69a3-2232">Az.HDInsight</span></span>
* <span data-ttu-id="b69a3-2233">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-2234">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-2235">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-2236">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-2237">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2238">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b69a3-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b69a3-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="b69a3-2240">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b69a3-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b69a3-2241">Az.Media</span></span>
* <span data-ttu-id="b69a3-2242">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2243">Az.Monitor</span></span>
  * <span data-ttu-id="b69a3-2244">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b69a3-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b69a3-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b69a3-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b69a3-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b69a3-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b69a3-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b69a3-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b69a3-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b69a3-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b69a3-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b69a3-2250">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b69a3-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2251">Az.Network</span></span>
* <span data-ttu-id="b69a3-2252">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2253">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b69a3-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b69a3-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="b69a3-2255">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-2257">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b69a3-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b69a3-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b69a3-2259">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-2261">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2262">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="b69a3-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b69a3-2263">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="b69a3-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b69a3-2264">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="b69a3-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b69a3-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b69a3-2265">Az.RedisCache</span></span>
* <span data-ttu-id="b69a3-2266">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2267">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2268">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2269">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2270">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b69a3-2271">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2272">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b69a3-2273">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b69a3-2274">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b69a3-2275">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b69a3-2276">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b69a3-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2277">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2278">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="b69a3-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b69a3-2279">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b69a3-2280">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b69a3-2281">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b69a3-2282">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-2283">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-2284">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="b69a3-2285">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b69a3-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b69a3-2286">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b69a3-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b69a3-2287">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b69a3-2288">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b69a3-2289">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b69a3-2290">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2291">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2292">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="b69a3-2294">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="b69a3-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b69a3-2295">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2296">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2297">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b69a3-2298">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b69a3-2299">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2300">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2301">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b69a3-2302">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b69a3-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="b69a3-2304">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="b69a3-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-2305">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-2306">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b69a3-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b69a3-2307">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2308">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2309">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b69a3-2310">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b69a3-2311">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="b69a3-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b69a3-2312">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b69a3-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b69a3-2313">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="b69a3-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b69a3-2314">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b69a3-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2315">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2316">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2317">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2318">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b69a3-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b69a3-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="b69a3-2320">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b69a3-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b69a3-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b69a3-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b69a3-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b69a3-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b69a3-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b69a3-2325">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b69a3-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b69a3-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b69a3-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b69a3-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b69a3-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b69a3-2330">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b69a3-2331">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b69a3-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="b69a3-2332">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="b69a3-2333">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b69a3-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b69a3-2334">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b69a3-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b69a3-2335">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b69a3-2336">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b69a3-2337">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b69a3-2338">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2339">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2340">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b69a3-2341">動態分組</span><span class="sxs-lookup"><span data-stu-id="b69a3-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="b69a3-2342">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="b69a3-2342">Pre-Post script</span></span>
    * <span data-ttu-id="b69a3-2343">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2344">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2345">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b69a3-2346">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-2347">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-2348">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2349">Az.Network</span></span>
* <span data-ttu-id="b69a3-2350">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b69a3-2351">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="b69a3-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-2353">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="b69a3-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b69a3-2354">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2355">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2356">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b69a3-2357">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2358">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2359">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2360">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2361">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="b69a3-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b69a3-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b69a3-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b69a3-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b69a3-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b69a3-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b69a3-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b69a3-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b69a3-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2368">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2369">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="b69a3-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="b69a3-2370">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2371">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2372">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b69a3-2373">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2374">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2375">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b69a3-2376">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b69a3-2377">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="b69a3-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-2378">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-2379">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2380">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2381">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-2382">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-2383">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b69a3-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b69a3-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b69a3-2384">Az.LogicApp</span></span>
* <span data-ttu-id="b69a3-2385">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="b69a3-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2386">Az.Network</span></span>
* <span data-ttu-id="b69a3-2387">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-2389">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b69a3-2390">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="b69a3-2390">SDK Update</span></span>
* <span data-ttu-id="b69a3-2391">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="b69a3-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b69a3-2392">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="b69a3-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2393">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2394">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b69a3-2395">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b69a3-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b69a3-2396">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b69a3-2397">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b69a3-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b69a3-2398">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b69a3-2399">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b69a3-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2400">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2401">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b69a3-2402">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2403">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2404">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b69a3-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b69a3-2405">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="b69a3-2407">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2408">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2409">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b69a3-2410">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b69a3-2411">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-2413">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2414">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2415">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b69a3-2416">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="b69a3-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b69a3-2417">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b69a3-2418">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2420">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b69a3-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-2421">Az.EventHub</span></span>
* <span data-ttu-id="b69a3-2422">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="b69a3-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-2423">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-2424">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="b69a3-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b69a3-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b69a3-2425">Az.LogicApp</span></span>
* <span data-ttu-id="b69a3-2426">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="b69a3-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b69a3-2427">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="b69a3-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b69a3-2428">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b69a3-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b69a3-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b69a3-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b69a3-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b69a3-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b69a3-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b69a3-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b69a3-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b69a3-2433">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b69a3-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b69a3-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b69a3-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b69a3-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b69a3-2438">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="b69a3-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b69a3-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2439">Az.Monitor</span></span>
* <span data-ttu-id="b69a3-2440">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2441">Az.Network</span></span>
* <span data-ttu-id="b69a3-2442">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="b69a3-2444">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b69a3-2445">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="b69a3-2446">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2447">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2448">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b69a3-2449">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b69a3-2450">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b69a3-2451">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2452">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2453">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b69a3-2454">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="b69a3-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2455">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2456">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b69a3-2457">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2458">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2459">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b69a3-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="b69a3-2461">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2462">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2463">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b69a3-2464">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b69a3-2465">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="b69a3-2467">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2468">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2469">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="b69a3-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="b69a3-2470">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b69a3-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b69a3-2471">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="b69a3-2472">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b69a3-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2473">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2474">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b69a3-2475">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b69a3-2476">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="b69a3-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b69a3-2477">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2478">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2479">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="b69a3-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b69a3-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="b69a3-2481">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="b69a3-2483">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b69a3-2484">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2485">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2486">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b69a3-2487">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b69a3-2488">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b69a3-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b69a3-2489">Az.Aks</span></span>
* <span data-ttu-id="b69a3-2490">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b69a3-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2491">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2492">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b69a3-2493">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b69a3-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b69a3-2494">Az.Cdn</span></span>
* <span data-ttu-id="b69a3-2495">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2496">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2497">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b69a3-2498">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b69a3-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b69a3-2499">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b69a3-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b69a3-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b69a3-2501">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b69a3-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b69a3-2502">Az.DataFactory</span></span>
* <span data-ttu-id="b69a3-2503">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b69a3-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2505">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b69a3-2506">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b69a3-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b69a3-2507">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-2508">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-2509">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b69a3-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-2510">Az.KeyVault</span></span>
* <span data-ttu-id="b69a3-2511">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2512">Az.Network</span></span>
* <span data-ttu-id="b69a3-2513">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2514">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2515">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b69a3-2516">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b69a3-2517">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b69a3-2518">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b69a3-2519">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b69a3-2520">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b69a3-2521">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b69a3-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-2523">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b69a3-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b69a3-2524">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2524">Fix some error messages.</span></span>
* <span data-ttu-id="b69a3-2525">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b69a3-2526">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b69a3-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b69a3-2527">Az.SignalR</span></span>
* <span data-ttu-id="b69a3-2528">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2529">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2530">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b69a3-2531">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="b69a3-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b69a3-2532">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b69a3-2533">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="b69a3-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2534">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2535">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b69a3-2536">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b69a3-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b69a3-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b69a3-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b69a3-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b69a3-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b69a3-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="b69a3-2540">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2541">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2542">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b69a3-2543">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b69a3-2544">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="b69a3-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b69a3-2545">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b69a3-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2546">Az.Accounts</span></span>
* <span data-ttu-id="b69a3-2547">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b69a3-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2548">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2549">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="b69a3-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b69a3-2550">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b69a3-2551">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2553">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b69a3-2554">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="b69a3-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b69a3-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b69a3-2555">Az.EventGrid</span></span>
* <span data-ttu-id="b69a3-2556">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b69a3-2557">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b69a3-2558">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b69a3-2559">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="b69a3-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b69a3-2560">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="b69a3-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b69a3-2561">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b69a3-2562">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b69a3-2563">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="b69a3-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b69a3-2564">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="b69a3-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b69a3-2565">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="b69a3-2566">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b69a3-2567">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b69a3-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b69a3-2568">Az.IotHub</span></span>
* <span data-ttu-id="b69a3-2569">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="b69a3-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b69a3-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b69a3-2570">Az.LogicApp</span></span>
* <span data-ttu-id="b69a3-2571">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2572">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2573">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b69a3-2574">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b69a3-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b69a3-2575">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="b69a3-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b69a3-2576">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b69a3-2577">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="b69a3-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b69a3-2578">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b69a3-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b69a3-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b69a3-2579">Az.SignalR</span></span>
* <span data-ttu-id="b69a3-2580">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2581">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2582">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b69a3-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2583">Az.Storage</span></span>
* <span data-ttu-id="b69a3-2584">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b69a3-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b69a3-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="b69a3-2586">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="b69a3-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b69a3-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b69a3-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2588">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2589">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="b69a3-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b69a3-2590">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b69a3-2591">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b69a3-2592">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-2592">General</span></span>

- <span data-ttu-id="b69a3-2593">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="b69a3-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="b69a3-2594">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-2594">Online help for each module</span></span>
- <span data-ttu-id="b69a3-2595">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b69a3-2596">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b69a3-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2597">Az.Accounts</span></span>
- <span data-ttu-id="b69a3-2598">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="b69a3-2599">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="b69a3-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b69a3-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="b69a3-2601">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="b69a3-2601">Fixes for #7002</span></span>
- <span data-ttu-id="b69a3-2602">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b69a3-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b69a3-2603">Az.Batch</span></span>
- <span data-ttu-id="b69a3-2604">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b69a3-2605">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b69a3-2606">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b69a3-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b69a3-2607">Az.Billing</span></span>
- <span data-ttu-id="b69a3-2608">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b69a3-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="b69a3-2610">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="b69a3-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b69a3-2611">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="b69a3-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b69a3-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="b69a3-2613">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b69a3-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b69a3-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b69a3-2615">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="b69a3-2617">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b69a3-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2618">Az.Monitor</span></span>
- <span data-ttu-id="b69a3-2619">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b69a3-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b69a3-2620">Az.KeyVault</span></span>
- <span data-ttu-id="b69a3-2621">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b69a3-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b69a3-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="b69a3-2623">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b69a3-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b69a3-2624">Az.Media</span></span>
- <span data-ttu-id="b69a3-2625">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="b69a3-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b69a3-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2626">Az.Network</span></span>
<span data-ttu-id="b69a3-2627">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b69a3-2628">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b69a3-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="b69a3-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b69a3-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b69a3-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b69a3-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b69a3-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b69a3-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b69a3-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b69a3-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b69a3-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b69a3-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b69a3-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b69a3-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b69a3-2643">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b69a3-2644">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b69a3-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b69a3-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b69a3-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b69a3-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b69a3-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b69a3-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b69a3-2648">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b69a3-2649">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b69a3-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="b69a3-2651">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b69a3-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2652">Az.Profile</span></span>
- <span data-ttu-id="b69a3-2653">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b69a3-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="b69a3-2655">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b69a3-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2656">Az.Resources</span></span>
- <span data-ttu-id="b69a3-2657">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b69a3-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="b69a3-2659">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="b69a3-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b69a3-2660">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b69a3-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b69a3-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="b69a3-2662">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="b69a3-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b69a3-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2663">Az.Sql</span></span>
- <span data-ttu-id="b69a3-2664">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="b69a3-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b69a3-2665">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b69a3-2666">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b69a3-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2667">Az.Storage</span></span>
- <span data-ttu-id="b69a3-2668">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b69a3-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2669">Az.Websites</span></span>
- <span data-ttu-id="b69a3-2670">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b69a3-2671">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b69a3-2672">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-2672">General</span></span>

* <span data-ttu-id="b69a3-2673">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b69a3-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2674">Az.Compute</span></span>

* <span data-ttu-id="b69a3-2675">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="b69a3-2677">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="b69a3-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b69a3-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b69a3-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="b69a3-2679">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="b69a3-2680">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b69a3-2681">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b69a3-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="b69a3-2683">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b69a3-2684">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b69a3-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2685">Az.Resources</span></span>

* <span data-ttu-id="b69a3-2686">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b69a3-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b69a3-2687">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b69a3-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2688">Az.Sql</span></span>

* <span data-ttu-id="b69a3-2689">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="b69a3-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b69a3-2690">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b69a3-2691">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b69a3-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2692">Az.Storage</span></span>

* <span data-ttu-id="b69a3-2693">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="b69a3-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b69a3-2694">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="b69a3-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b69a3-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b69a3-2696">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="b69a3-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="b69a3-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b69a3-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b69a3-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b69a3-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b69a3-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2699">Az.Websites</span></span>

* <span data-ttu-id="b69a3-2700">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b69a3-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="b69a3-2701">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b69a3-2702">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b69a3-2703">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b69a3-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b69a3-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="b69a3-2705">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b69a3-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b69a3-2706">Az.Automation</span></span>
* <span data-ttu-id="b69a3-2707">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b69a3-2708">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b69a3-2709">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b69a3-2710">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b69a3-2711">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="b69a3-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b69a3-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2712">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2713">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b69a3-2714">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b69a3-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="b69a3-2716">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b69a3-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b69a3-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b69a3-2718">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="b69a3-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b69a3-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2719">Az.Network</span></span>
* <span data-ttu-id="b69a3-2720">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b69a3-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b69a3-2721">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="b69a3-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b69a3-2722">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="b69a3-2723">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b69a3-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b69a3-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b69a3-2725">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b69a3-2726">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b69a3-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b69a3-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b69a3-2728">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b69a3-2729">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b69a3-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b69a3-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b69a3-2730">Az.Relay</span></span>
* <span data-ttu-id="b69a3-2731">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b69a3-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2732">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2733">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="b69a3-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b69a3-2734">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="b69a3-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b69a3-2735">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="b69a3-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b69a3-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-2737">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="b69a3-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b69a3-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2738">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2739">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b69a3-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b69a3-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b69a3-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b69a3-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b69a3-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b69a3-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b69a3-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b69a3-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b69a3-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b69a3-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b69a3-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b69a3-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b69a3-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b69a3-2748">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b69a3-2749">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b69a3-2750">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b69a3-2751">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b69a3-2752">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b69a3-2753">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b69a3-2754">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b69a3-2755">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b69a3-2756">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b69a3-2757">一般</span><span class="sxs-lookup"><span data-stu-id="b69a3-2757">General</span></span>
* <span data-ttu-id="b69a3-2758">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="b69a3-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b69a3-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2759">Az.Profile</span></span>
* <span data-ttu-id="b69a3-2760">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b69a3-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b69a3-2761">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="b69a3-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b69a3-2762">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="b69a3-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b69a3-2763">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b69a3-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b69a3-2764">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b69a3-2765">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b69a3-2766">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-2768">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2769">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2770">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b69a3-2771">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b69a3-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b69a3-2772">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2774">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b69a3-2775">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b69a3-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2776">Az.Insights</span></span>
* <span data-ttu-id="b69a3-2777">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="b69a3-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b69a3-2778">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b69a3-2779">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="b69a3-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b69a3-2780">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="b69a3-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2781">Az.Network</span></span>
* <span data-ttu-id="b69a3-2782">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="b69a3-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b69a3-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b69a3-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b69a3-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b69a3-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b69a3-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b69a3-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b69a3-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b69a3-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b69a3-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b69a3-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b69a3-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="b69a3-2790">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2791">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2792">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b69a3-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b69a3-2793">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="b69a3-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b69a3-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b69a3-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="b69a3-2795">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b69a3-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b69a3-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="b69a3-2797">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b69a3-2798">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="b69a3-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b69a3-2799">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b69a3-2800">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b69a3-2801">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b69a3-2802">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b69a3-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2803">Az.Profile</span></span>
* <span data-ttu-id="b69a3-2804">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b69a3-2805">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b69a3-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2806">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2807">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="b69a3-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b69a3-2808">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b69a3-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b69a3-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="b69a3-2810">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="b69a3-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b69a3-2811">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b69a3-2812">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b69a3-2813">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b69a3-2814">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2815">Az.Network</span></span>
* <span data-ttu-id="b69a3-2816">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b69a3-2817">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2818">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2819">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b69a3-2820">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b69a3-2821">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b69a3-2822">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2822">Azure.Storage</span></span>
* <span data-ttu-id="b69a3-2823">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b69a3-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b69a3-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b69a3-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b69a3-2826">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b69a3-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b69a3-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b69a3-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b69a3-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="b69a3-2829">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b69a3-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b69a3-2830">Az.Compute</span></span>
* <span data-ttu-id="b69a3-2831">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="b69a3-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b69a3-2832">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b69a3-2833">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="b69a3-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b69a3-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b69a3-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b69a3-2835">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b69a3-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b69a3-2836">Az.Network</span></span>
* <span data-ttu-id="b69a3-2837">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b69a3-2838">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2838">new cmdlets added</span></span>
    - <span data-ttu-id="b69a3-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b69a3-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b69a3-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b69a3-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b69a3-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b69a3-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b69a3-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b69a3-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b69a3-2845">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="b69a3-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b69a3-2846">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b69a3-2847">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b69a3-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b69a3-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b69a3-2848">Az.RedisCache</span></span>
* <span data-ttu-id="b69a3-2849">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="b69a3-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b69a3-2850">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="b69a3-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b69a3-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b69a3-2851">Az.Resources</span></span>
* <span data-ttu-id="b69a3-2852">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b69a3-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b69a3-2853">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="b69a3-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b69a3-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b69a3-2854">Az.Sql</span></span>
* <span data-ttu-id="b69a3-2855">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="b69a3-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b69a3-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b69a3-2856">Az.Websites</span></span>
* <span data-ttu-id="b69a3-2857">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="b69a3-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b69a3-2858">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="b69a3-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b69a3-2859">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="b69a3-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b69a3-2860">初始版本</span><span class="sxs-lookup"><span data-stu-id="b69a3-2860">Initial Release</span></span>
