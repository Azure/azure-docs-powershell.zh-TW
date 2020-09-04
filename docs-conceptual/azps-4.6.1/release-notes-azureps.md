---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244223"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ad4cd-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="ad4cd-104">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="ad4cd-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-105">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-106">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="ad4cd-107">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-108">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-109">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="ad4cd-110">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-111">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-112">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="ad4cd-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-113">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-114">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="ad4cd-115">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="ad4cd-116">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="ad4cd-117">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-118">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-119">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-120">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-121">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-122">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-123">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="ad4cd-124">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="ad4cd-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-125">Az.Maintenance</span></span>
* <span data-ttu-id="ad4cd-126">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="ad4cd-127">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ad4cd-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-128">Az.ManagedServices</span></span>
* <span data-ttu-id="ad4cd-129">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="ad4cd-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-130">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-131">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="ad4cd-132">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-133">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-134">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="ad4cd-135">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="ad4cd-136">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="ad4cd-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="ad4cd-137">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="ad4cd-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="ad4cd-138">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="ad4cd-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="ad4cd-139">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="ad4cd-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="ad4cd-140">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="ad4cd-141">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad4cd-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad4cd-142">Az.SignalR</span></span>
* <span data-ttu-id="ad4cd-143">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="ad4cd-144">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-145">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-146">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="ad4cd-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="ad4cd-147">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="ad4cd-148">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="ad4cd-149">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="ad4cd-150">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="ad4cd-151">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="ad4cd-152">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="ad4cd-153">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="ad4cd-154">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="ad4cd-155">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="ad4cd-156">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="ad4cd-157">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="ad4cd-158">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="ad4cd-159">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="ad4cd-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="ad4cd-160">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="ad4cd-161">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-162">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-163">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="ad4cd-164">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="ad4cd-165">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="ad4cd-166">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="ad4cd-167">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-168">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-169">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="ad4cd-170">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-171">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-172">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-173">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-174">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-175">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-176">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-177">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-178">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-179">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-180">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-181">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-182">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-183">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-185">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-186">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-187">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-188">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-189">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="ad4cd-190">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="ad4cd-191">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="ad4cd-192">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="ad4cd-193">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="ad4cd-194">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="ad4cd-195">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-196">Az.Network</span></span>
* <span data-ttu-id="ad4cd-197">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="ad4cd-198">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="ad4cd-199">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="ad4cd-200">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-202">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="ad4cd-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="ad4cd-203">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="ad4cd-204">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-206">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-207">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-208">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="ad4cd-209">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-210">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-211">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="ad4cd-212">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-213">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-214">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="ad4cd-215">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="ad4cd-216">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="ad4cd-217">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="ad4cd-218">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="ad4cd-219">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="ad4cd-220">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="ad4cd-221">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-222">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-223">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="ad4cd-224">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-225">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-226">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad4cd-228">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="ad4cd-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-229">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-230">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-231">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-232">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="ad4cd-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-233">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-234">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad4cd-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad4cd-235">Az.EventGrid</span></span>
* <span data-ttu-id="ad4cd-236">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="ad4cd-237">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-237">Added new features:</span></span>
    - <span data-ttu-id="ad4cd-238">輸入對應</span><span class="sxs-lookup"><span data-stu-id="ad4cd-238">Input mapping</span></span>
    - <span data-ttu-id="ad4cd-239">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="ad4cd-240">私人連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-240">Private Link</span></span>
    - <span data-ttu-id="ad4cd-241">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="ad4cd-242">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="ad4cd-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="ad4cd-243">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="ad4cd-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="ad4cd-244">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-244">WebHook Batching</span></span>
    - <span data-ttu-id="ad4cd-245">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="ad4cd-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="ad4cd-246">IpFiltering</span></span>
* <span data-ttu-id="ad4cd-247">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="ad4cd-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="ad4cd-249">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="ad4cd-250">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="ad4cd-251">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="ad4cd-252">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="ad4cd-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="ad4cd-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="ad4cd-254">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="ad4cd-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="ad4cd-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="ad4cd-256">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-257">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-258">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="ad4cd-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="ad4cd-259">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-260">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-261">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-262">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-263">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-264">Az.Network</span></span>
* <span data-ttu-id="ad4cd-265">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="ad4cd-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="ad4cd-266">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="ad4cd-267">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="ad4cd-268">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="ad4cd-269">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="ad4cd-270">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="ad4cd-271">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="ad4cd-272">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="ad4cd-273">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="ad4cd-274">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="ad4cd-275">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="ad4cd-276">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="ad4cd-277">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="ad4cd-278">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="ad4cd-279">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="ad4cd-280">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="ad4cd-281">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-283">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="ad4cd-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="ad4cd-284">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="ad4cd-285">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-286">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-287">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="ad4cd-288">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-289">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-290">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="ad4cd-291">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="ad4cd-292">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-293">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-294">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="ad4cd-295">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="ad4cd-296">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="ad4cd-297">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-298">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="ad4cd-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="ad4cd-299">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="ad4cd-300">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="ad4cd-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="ad4cd-301">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="ad4cd-302">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="ad4cd-303">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="ad4cd-304">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="ad4cd-305">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="ad4cd-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="ad4cd-306">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="ad4cd-307">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="ad4cd-308">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="ad4cd-309">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="ad4cd-310">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad4cd-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad4cd-311">Az.StorageSync</span></span>
* <span data-ttu-id="ad4cd-312">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="ad4cd-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="ad4cd-313">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="ad4cd-314">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="ad4cd-315">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-316">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-317">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="ad4cd-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="ad4cd-318">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-319">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-320">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="ad4cd-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="ad4cd-321">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="ad4cd-322">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="ad4cd-323">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-324">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-325">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-326">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-327">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="ad4cd-328">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-330">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="ad4cd-331">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-332">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-333">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="ad4cd-334">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="ad4cd-335">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="ad4cd-336">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="ad4cd-337">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-338">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-339">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-340">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-341">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="ad4cd-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="ad4cd-342">Az.Functions</span></span>
* <span data-ttu-id="ad4cd-343">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-344">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-345">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ad4cd-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ad4cd-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="ad4cd-347">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="ad4cd-348">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-349">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-350">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="ad4cd-351">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-352">Az.Network</span></span>
* <span data-ttu-id="ad4cd-353">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="ad4cd-354">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="ad4cd-355">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="ad4cd-356">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="ad4cd-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="ad4cd-357">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="ad4cd-358">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="ad4cd-359">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="ad4cd-360">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="ad4cd-361">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="ad4cd-362">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="ad4cd-363">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="ad4cd-364">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="ad4cd-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="ad4cd-366">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="ad4cd-367">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="ad4cd-368">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="ad4cd-369">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="ad4cd-370">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="ad4cd-371">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="ad4cd-372">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="ad4cd-373">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="ad4cd-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="ad4cd-374">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="ad4cd-375">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="ad4cd-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="ad4cd-376">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="ad4cd-377">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="ad4cd-378">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="ad4cd-379">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="ad4cd-380">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="ad4cd-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="ad4cd-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="ad4cd-387">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="ad4cd-388">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="ad4cd-389">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="ad4cd-390">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="ad4cd-391">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="ad4cd-392">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="ad4cd-393">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="ad4cd-394">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="ad4cd-395">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="ad4cd-396">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ad4cd-397">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ad4cd-398">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="ad4cd-399">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="ad4cd-400">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="ad4cd-401">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-403">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="ad4cd-404">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="ad4cd-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="ad4cd-405">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="ad4cd-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="ad4cd-406">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="ad4cd-407">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-409">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="ad4cd-410">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-411">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-412">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="ad4cd-413">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="ad4cd-414">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="ad4cd-415">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="ad4cd-416">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="ad4cd-417">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-418">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-419">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="ad4cd-420">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="ad4cd-421">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-422">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-423">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="ad4cd-424">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-425">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-426">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-427">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ad4cd-428">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="ad4cd-429">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="ad4cd-430">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="ad4cd-431">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="ad4cd-432">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="ad4cd-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="ad4cd-433">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-434">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-435">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad4cd-437">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-438">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-439">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="ad4cd-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ad4cd-440">Az.Billing</span></span>
* <span data-ttu-id="ad4cd-441">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-443">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-444">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-445">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="ad4cd-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-446">Az.DataShare</span></span>
* <span data-ttu-id="ad4cd-447">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="ad4cd-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="ad4cd-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="ad4cd-449">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-451">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="ad4cd-452">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="ad4cd-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="ad4cd-453">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="ad4cd-454">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-456">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="ad4cd-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ad4cd-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad4cd-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad4cd-458">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="ad4cd-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="ad4cd-459">Az.PrivateDns</span></span>
* <span data-ttu-id="ad4cd-460">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-462">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="ad4cd-463">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-464">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-465">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="ad4cd-466">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="ad4cd-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="ad4cd-467">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="ad4cd-468">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="ad4cd-469">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-470">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-471">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="ad4cd-472">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="ad4cd-473">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-474">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-475">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="ad4cd-476">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="ad4cd-477">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-477">Highlights since the last release</span></span>
* <span data-ttu-id="ad4cd-478">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="ad4cd-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="ad4cd-479">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="ad4cd-480">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-481">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-482">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="ad4cd-483">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="ad4cd-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-484">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-485">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="ad4cd-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="ad4cd-486">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="ad4cd-487">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-488">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-489">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="ad4cd-490">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="ad4cd-491">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="ad4cd-492">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="ad4cd-493">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="ad4cd-494">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="ad4cd-495">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="ad4cd-496">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="ad4cd-497">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="ad4cd-498">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="ad4cd-499">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="ad4cd-500">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="ad4cd-501">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="ad4cd-502">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="ad4cd-503">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="ad4cd-504">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ad4cd-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ad4cd-506">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="ad4cd-507">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="ad4cd-508">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-509">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-510">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="ad4cd-511">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="ad4cd-512">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="ad4cd-513">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="ad4cd-514">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="ad4cd-515">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="ad4cd-516">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="ad4cd-517">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="ad4cd-518">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-519">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-520">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="ad4cd-521">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="ad4cd-522">重大變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-522">Breaking changes</span></span>
    - <span data-ttu-id="ad4cd-523">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="ad4cd-524">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="ad4cd-525">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="ad4cd-526">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="ad4cd-527">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="ad4cd-528">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="ad4cd-529">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-530">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-531">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-532">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-533">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="ad4cd-534">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="ad4cd-535">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="ad4cd-536">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="ad4cd-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="ad4cd-537">Az.Functions</span></span>
* <span data-ttu-id="ad4cd-538">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-539">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-540">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ad4cd-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ad4cd-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="ad4cd-542">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="ad4cd-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-543">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-544">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="ad4cd-545">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="ad4cd-546">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="ad4cd-547">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="ad4cd-548">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="ad4cd-549">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-549">New cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-550">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="ad4cd-551">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="ad4cd-552">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="ad4cd-553">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="ad4cd-554">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="ad4cd-555">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-556">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-557">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="ad4cd-558">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="ad4cd-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="ad4cd-559">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="ad4cd-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="ad4cd-560">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="ad4cd-561">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="ad4cd-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="ad4cd-562">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="ad4cd-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="ad4cd-563">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="ad4cd-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-564">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-565">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="ad4cd-566">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="ad4cd-567">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="ad4cd-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="ad4cd-568">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="ad4cd-569">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="ad4cd-570">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="ad4cd-571">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-572">Az.Network</span></span>
* <span data-ttu-id="ad4cd-573">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="ad4cd-574">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="ad4cd-575">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="ad4cd-576">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="ad4cd-577">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="ad4cd-578">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-578">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ad4cd-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="ad4cd-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ad4cd-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="ad4cd-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ad4cd-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="ad4cd-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ad4cd-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="ad4cd-583">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="ad4cd-584">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="ad4cd-585">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="ad4cd-586">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="ad4cd-587">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="ad4cd-588">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="ad4cd-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="ad4cd-589">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="ad4cd-590">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="ad4cd-591">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="ad4cd-592">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="ad4cd-593">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="ad4cd-594">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="ad4cd-595">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="ad4cd-596">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ad4cd-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-599">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="ad4cd-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="ad4cd-600">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="ad4cd-601">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="ad4cd-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="ad4cd-602">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="ad4cd-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="ad4cd-603">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="ad4cd-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="ad4cd-604">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="ad4cd-605">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="ad4cd-606">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-608">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="ad4cd-609">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="ad4cd-610">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="ad4cd-611">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="ad4cd-612">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-613">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-614">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="ad4cd-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="ad4cd-615">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="ad4cd-616">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="ad4cd-617">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="ad4cd-618">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="ad4cd-619">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="ad4cd-620">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="ad4cd-621">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="ad4cd-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="ad4cd-622">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="ad4cd-623">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="ad4cd-624">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="ad4cd-625">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="ad4cd-626">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="ad4cd-627">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="ad4cd-628">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="ad4cd-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="ad4cd-629">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="ad4cd-630">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="ad4cd-631">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="ad4cd-632">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ad4cd-633">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-635">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="ad4cd-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-636">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-637">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-637">Enhance performance of:</span></span>
    - <span data-ttu-id="ad4cd-638">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="ad4cd-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="ad4cd-640">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="ad4cd-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="ad4cd-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="ad4cd-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="ad4cd-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="ad4cd-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="ad4cd-646">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="ad4cd-647">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-648">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-649">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-650">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="ad4cd-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="ad4cd-651">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-652">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="ad4cd-653">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="ad4cd-654">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="ad4cd-655">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="ad4cd-656">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="ad4cd-657">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="ad4cd-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="ad4cd-658">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="ad4cd-659">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="ad4cd-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="ad4cd-660">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="ad4cd-661">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="ad4cd-662">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="ad4cd-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="ad4cd-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-665">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="ad4cd-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="ad4cd-666">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="ad4cd-667">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ad4cd-668">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="ad4cd-669">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="ad4cd-670">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="ad4cd-671">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="ad4cd-672">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="ad4cd-673">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="ad4cd-674">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="ad4cd-675">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="ad4cd-676">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="ad4cd-677">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="ad4cd-678">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="ad4cd-679">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="ad4cd-680">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="ad4cd-681">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="ad4cd-682">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="ad4cd-683">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="ad4cd-684">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="ad4cd-685">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="ad4cd-686">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="ad4cd-687">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ad4cd-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad4cd-688">Az.TrafficManager</span></span>
* <span data-ttu-id="ad4cd-689">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-690">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-691">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="ad4cd-692">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="ad4cd-693">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-693">Highlights since the last release</span></span>
* <span data-ttu-id="ad4cd-694">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="ad4cd-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-695">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-696">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-697">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-698">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="ad4cd-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="ad4cd-699">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-700">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-701">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="ad4cd-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-703">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-704">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-705">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-706">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-707">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-708">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-709">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="ad4cd-710">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="ad4cd-711">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="ad4cd-712">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-713">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="ad4cd-714">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="ad4cd-715">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="ad4cd-716">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-716">New cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-717">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-718">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-719">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ad4cd-720">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="ad4cd-721">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-722">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-723">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="ad4cd-724">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="ad4cd-725">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="ad4cd-726">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="ad4cd-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-727">Az.Maintenance</span></span>
* <span data-ttu-id="ad4cd-728">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-729">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-730">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="ad4cd-731">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ad4cd-732">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ad4cd-733">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ad4cd-734">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ad4cd-735">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="ad4cd-736">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="ad4cd-737">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-738">Az.Network</span></span>
* <span data-ttu-id="ad4cd-739">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="ad4cd-740">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="ad4cd-741">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="ad4cd-742">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="ad4cd-743">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="ad4cd-744">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="ad4cd-745">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="ad4cd-746">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="ad4cd-747">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="ad4cd-748">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="ad4cd-749">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="ad4cd-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="ad4cd-750">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="ad4cd-751">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="ad4cd-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="ad4cd-752">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="ad4cd-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="ad4cd-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-756">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="ad4cd-757">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-759">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-760">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-761">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="ad4cd-762">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-763">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-764">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="ad4cd-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="ad4cd-765">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="ad4cd-766">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="ad4cd-767">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="ad4cd-768">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="ad4cd-769">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ad4cd-770">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ad4cd-771">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="ad4cd-772">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ad4cd-773">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="ad4cd-774">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ad4cd-775">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="ad4cd-776">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="ad4cd-777">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="ad4cd-778">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-778">General</span></span>
* <span data-ttu-id="ad4cd-779">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="ad4cd-780">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="ad4cd-781">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="ad4cd-782">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="ad4cd-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ad4cd-783">Az.Billing</span></span>
  - <span data-ttu-id="ad4cd-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-784">Az.Compute</span></span>
  - <span data-ttu-id="ad4cd-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ad4cd-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="ad4cd-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-786">Az.EventHub</span></span>
  - <span data-ttu-id="ad4cd-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-787">Az.IotHub</span></span>
  - <span data-ttu-id="ad4cd-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-788">Az.KeyVault</span></span>
  - <span data-ttu-id="ad4cd-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-789">Az.Monitor</span></span>
  - <span data-ttu-id="ad4cd-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-790">Az.Network</span></span>
  - <span data-ttu-id="ad4cd-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-791">Az.Resources</span></span>
  - <span data-ttu-id="ad4cd-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-792">Az.Storage</span></span>
  - <span data-ttu-id="ad4cd-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-793">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-794">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-795">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="ad4cd-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="ad4cd-796">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="ad4cd-797">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-798">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-799">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-800">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-801">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="ad4cd-802">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="ad4cd-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="ad4cd-803">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-804">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="ad4cd-805">[#11354]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-805">[#11354]</span></span>
* <span data-ttu-id="ad4cd-806">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="ad4cd-807">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ad4cd-808">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ad4cd-809">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ad4cd-810">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="ad4cd-811">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="ad4cd-812">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="ad4cd-813">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="ad4cd-814">[#11257]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-815">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-816">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="ad4cd-817">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-819">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="ad4cd-820">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="ad4cd-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-821">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-822">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-823">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-824">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="ad4cd-825">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-826">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="ad4cd-827">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-828">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-829">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-830">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-831">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-832">Az.Network</span></span>
* <span data-ttu-id="ad4cd-833">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="ad4cd-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="ad4cd-834">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ad4cd-835">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ad4cd-836">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="ad4cd-837">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="ad4cd-838">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-840">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-842">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="ad4cd-843">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="ad4cd-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="ad4cd-844">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="ad4cd-845">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="ad4cd-846">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="ad4cd-847">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-848">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-849">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="ad4cd-850">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="ad4cd-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="ad4cd-851">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="ad4cd-852">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-852">Added example.</span></span>
* <span data-ttu-id="ad4cd-853">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="ad4cd-854">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-855">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-856">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="ad4cd-857">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="ad4cd-858">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="ad4cd-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="ad4cd-859">Az.Support</span></span>
* <span data-ttu-id="ad4cd-860">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-861">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-862">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="ad4cd-863">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ad4cd-864">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ad4cd-865">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ad4cd-866">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="ad4cd-867">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-868">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-869">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="ad4cd-870">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="ad4cd-871">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-872">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-873">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="ad4cd-874">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="ad4cd-875">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="ad4cd-876">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-878">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-879">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-880">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ad4cd-881">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-882">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-883">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-884">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-885">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="ad4cd-886">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="ad4cd-887">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-888">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="ad4cd-889">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="ad4cd-890">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="ad4cd-891">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="ad4cd-892">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ad4cd-893">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ad4cd-894">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="ad4cd-895">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-896">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="ad4cd-897">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="ad4cd-898">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-899">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-900">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-901">Az.Network</span></span>
* <span data-ttu-id="ad4cd-902">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="ad4cd-903">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="ad4cd-904">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="ad4cd-905">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-906">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-907">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="ad4cd-908">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="ad4cd-909">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="ad4cd-910">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="ad4cd-911">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="ad4cd-912">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="ad4cd-913">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="ad4cd-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="ad4cd-914">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="ad4cd-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ad4cd-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ad4cd-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="ad4cd-918">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="ad4cd-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="ad4cd-920">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-921">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-922">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="ad4cd-923">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="ad4cd-924">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="ad4cd-925">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="ad4cd-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="ad4cd-926">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="ad4cd-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="ad4cd-927">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="ad4cd-928">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ad4cd-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="ad4cd-929">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="ad4cd-930">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-931">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-932">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="ad4cd-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="ad4cd-934">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="ad4cd-935">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="ad4cd-936">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-937">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-938">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="ad4cd-939">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="ad4cd-940">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="ad4cd-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="ad4cd-941">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="ad4cd-942">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="ad4cd-943">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-944">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-944">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-945">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="ad4cd-946">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="ad4cd-947">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-948">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-949">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="ad4cd-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-950">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-951">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-953">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="ad4cd-954">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-955">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-956">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="ad4cd-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-957">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-958">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="ad4cd-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-959">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-960">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ad4cd-961">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-962">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-963">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-964">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ad4cd-965">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-966">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-967">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-968">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-969">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="ad4cd-970">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="ad4cd-971">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-972">Az.Network</span></span>
* <span data-ttu-id="ad4cd-973">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-974">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ad4cd-975">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ad4cd-976">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="ad4cd-977">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-977">No new cmdlets are added.</span></span> <span data-ttu-id="ad4cd-978">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="ad4cd-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-980">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-981">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-982">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="ad4cd-983">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="ad4cd-984">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="ad4cd-985">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="ad4cd-986">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="ad4cd-987">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="ad4cd-988">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="ad4cd-989">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="ad4cd-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-990">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-991">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="ad4cd-992">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="ad4cd-993">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ad4cd-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ad4cd-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ad4cd-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ad4cd-995">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad4cd-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad4cd-996">Az.StorageSync</span></span>
* <span data-ttu-id="ad4cd-997">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="ad4cd-998">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-999">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-999">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-1000">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="ad4cd-1001">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1002">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1003">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="ad4cd-1004">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-1006">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="ad4cd-1007">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="ad4cd-1008">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="ad4cd-1009">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1010">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1011">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="ad4cd-1012">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="ad4cd-1013">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-1014">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="ad4cd-1015">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1016">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1017">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ad4cd-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="ad4cd-1019">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="ad4cd-1020">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1021">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-1022">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1023">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-1024">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1025">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1026">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="ad4cd-1027">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="ad4cd-1028">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1029">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="ad4cd-1030">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="ad4cd-1031">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="ad4cd-1032">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="ad4cd-1033">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="ad4cd-1034">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="ad4cd-1036">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="ad4cd-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="ad4cd-1038">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-1040">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="ad4cd-1041">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="ad4cd-1042">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="ad4cd-1043">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1045">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="ad4cd-1046">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1047">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1048">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="ad4cd-1049">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1050">Az.Sql</span></span>
<span data-ttu-id="ad4cd-1051">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1052">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1053">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="ad4cd-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="ad4cd-1055">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="ad4cd-1056">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1057">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1058">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="ad4cd-1059">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="ad4cd-1060">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1061">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1062">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1063">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-1064">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1065">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1066">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ad4cd-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="ad4cd-1068">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ad4cd-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ad4cd-1070">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ad4cd-1071">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="ad4cd-1072">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ad4cd-1073">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="ad4cd-1074">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ad4cd-1075">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="ad4cd-1076">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ad4cd-1077">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="ad4cd-1078">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ad4cd-1079">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="ad4cd-1080">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ad4cd-1081">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="ad4cd-1082">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ad4cd-1083">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="ad4cd-1084">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="ad4cd-1085">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="ad4cd-1086">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="ad4cd-1087">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1088">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1089">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="ad4cd-1090">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="ad4cd-1091">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="ad4cd-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="ad4cd-1093">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1094">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-1095">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1096">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-1097">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ad4cd-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="ad4cd-1099">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="ad4cd-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="ad4cd-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="ad4cd-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="ad4cd-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="ad4cd-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="ad4cd-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="ad4cd-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1107">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1108">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1110">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="ad4cd-1111">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ad4cd-1112">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ad4cd-1113">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1114">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1115">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1116">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1117">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="ad4cd-1118">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ad4cd-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ad4cd-1120">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1121">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1122">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="ad4cd-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="ad4cd-1124">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="ad4cd-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="ad4cd-1126">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="ad4cd-1127">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1127">General</span></span>
* <span data-ttu-id="ad4cd-1128">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1129">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1130">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="ad4cd-1131">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1132">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-1133">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1134">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1135">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-1137">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="ad4cd-1138">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ad4cd-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="ad4cd-1140">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1141">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-1142">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="ad4cd-1143">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="ad4cd-1144">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1145">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-1146">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="ad4cd-1147">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="ad4cd-1148">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1149">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1150">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1151">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1152">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="ad4cd-1153">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1154">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1155">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1156">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1157">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="ad4cd-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="ad4cd-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="ad4cd-1160">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="ad4cd-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="ad4cd-1162">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="ad4cd-1163">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="ad4cd-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="ad4cd-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="ad4cd-1166">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="ad4cd-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="ad4cd-1168">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="ad4cd-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="ad4cd-1170">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-1171">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-1172">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="ad4cd-1173">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1174">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1175">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="ad4cd-1176">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="ad4cd-1177">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="ad4cd-1178">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="ad4cd-1179">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="ad4cd-1180">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ad4cd-1181">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="ad4cd-1182">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="ad4cd-1183">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="ad4cd-1184">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="ad4cd-1185">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ad4cd-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ad4cd-1187">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ad4cd-1188">取得訂單</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1188">Get the Order</span></span>
* <span data-ttu-id="ad4cd-1189">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ad4cd-1190">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1190">Create new Order</span></span>
* <span data-ttu-id="ad4cd-1191">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ad4cd-1192">移除訂單</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1192">Remove the Order</span></span>
* <span data-ttu-id="ad4cd-1193">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="ad4cd-1194">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1194">Now creates Local Share</span></span>
* <span data-ttu-id="ad4cd-1195">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="ad4cd-1196">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="ad4cd-1197">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="ad4cd-1198">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="ad4cd-1199">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ad4cd-1200">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="ad4cd-1201">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ad4cd-1202">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1202">Create new Triggers</span></span>
* <span data-ttu-id="ad4cd-1203">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ad4cd-1204">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1205">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1206">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="ad4cd-1207">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-1209">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1210">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-1211">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-1213">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="ad4cd-1214">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="ad4cd-1215">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="ad4cd-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1217">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1218">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="ad4cd-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="ad4cd-1220">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1222">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="ad4cd-1223">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="ad4cd-1224">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad4cd-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1225">Az.RedisCache</span></span>
* <span data-ttu-id="ad4cd-1226">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="ad4cd-1227">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="ad4cd-1228">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1229">Az.Resources</span></span>
- <span data-ttu-id="ad4cd-1230">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="ad4cd-1231">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="ad4cd-1232">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="ad4cd-1233">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="ad4cd-1234">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1235">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1236">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="ad4cd-1237">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="ad4cd-1238">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="ad4cd-1239">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1239">General</span></span>
* <span data-ttu-id="ad4cd-1240">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1241">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1242">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ad4cd-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1243">Az.Advisor</span></span>
* <span data-ttu-id="ad4cd-1244">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1245">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-1246">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="ad4cd-1247">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="ad4cd-1248">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="ad4cd-1249">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="ad4cd-1250">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="ad4cd-1251">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="ad4cd-1252">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="ad4cd-1253">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="ad4cd-1254">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="ad4cd-1255">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ad4cd-1256">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="ad4cd-1257">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="ad4cd-1258">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ad4cd-1259">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="ad4cd-1260">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="ad4cd-1261">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="ad4cd-1262">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="ad4cd-1263">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="ad4cd-1264">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="ad4cd-1265">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="ad4cd-1266">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ad4cd-1267">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ad4cd-1268">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="ad4cd-1269">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="ad4cd-1270">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="ad4cd-1271">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="ad4cd-1272">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="ad4cd-1273">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="ad4cd-1274">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="ad4cd-1275">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="ad4cd-1276">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="ad4cd-1277">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="ad4cd-1278">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="ad4cd-1279">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="ad4cd-1280">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="ad4cd-1281">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1282">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-1283">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="ad4cd-1284">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1285">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1286">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="ad4cd-1287">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="ad4cd-1288">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="ad4cd-1289">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ad4cd-1290">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="ad4cd-1291">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="ad4cd-1292">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="ad4cd-1293">重大變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1293">Breaking changes</span></span>
    - <span data-ttu-id="ad4cd-1294">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="ad4cd-1295">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1296">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1297">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-1299">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="ad4cd-1300">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="ad4cd-1301">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="ad4cd-1302">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="ad4cd-1303">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="ad4cd-1304">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-1306">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1307">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-1308">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="ad4cd-1309">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="ad4cd-1310">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="ad4cd-1311">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ad4cd-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ad4cd-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ad4cd-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="ad4cd-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="ad4cd-1317">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-1318">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ad4cd-1319">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ad4cd-1320">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="ad4cd-1321">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="ad4cd-1322">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="ad4cd-1323">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="ad4cd-1324">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="ad4cd-1325">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="ad4cd-1326">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="ad4cd-1327">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="ad4cd-1328">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="ad4cd-1329">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1330">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-1331">重大變更：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1331">Breaking changes:</span></span>
    - <span data-ttu-id="ad4cd-1332">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ad4cd-1333">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ad4cd-1334">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ad4cd-1335">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ad4cd-1336">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="ad4cd-1337">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="ad4cd-1338">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="ad4cd-1339">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="ad4cd-1340">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ad4cd-1341">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ad4cd-1342">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ad4cd-1343">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1345">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1346">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="ad4cd-1347">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="ad4cd-1348">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1349">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1350">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1351">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1352">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-1353">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1354">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1355">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1356">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1357">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="ad4cd-1358">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ad4cd-1364">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="ad4cd-1365">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1365">New cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="ad4cd-1367">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="ad4cd-1368">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="ad4cd-1369">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="ad4cd-1370">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="ad4cd-1371">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="ad4cd-1372">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="ad4cd-1373">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="ad4cd-1374">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="ad4cd-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ad4cd-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ad4cd-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ad4cd-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="ad4cd-1380">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="ad4cd-1381">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ad4cd-1382">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ad4cd-1383">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ad4cd-1384">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="ad4cd-1385">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="ad4cd-1386">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="ad4cd-1387">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="ad4cd-1389">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ad4cd-1390">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ad4cd-1391">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ad4cd-1392">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ad4cd-1393">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ad4cd-1394">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="ad4cd-1395">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="ad4cd-1396">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="ad4cd-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="ad4cd-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="ad4cd-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="ad4cd-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="ad4cd-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="ad4cd-1403">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ad4cd-1404">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="ad4cd-1405">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="ad4cd-1406">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="ad4cd-1407">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="ad4cd-1408">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ad4cd-1409">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="ad4cd-1410">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="ad4cd-1411">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="ad4cd-1412">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="ad4cd-1413">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="ad4cd-1414">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="ad4cd-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="ad4cd-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="ad4cd-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-1420">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1421">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1422">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="ad4cd-1423">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="ad4cd-1424">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="ad4cd-1425">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="ad4cd-1426">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="ad4cd-1427">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ad4cd-1428">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="ad4cd-1429">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="ad4cd-1430">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1431">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1432">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="ad4cd-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ad4cd-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ad4cd-1435">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="ad4cd-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="ad4cd-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="ad4cd-1438">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ad4cd-1439">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1439">General</span></span>
* <span data-ttu-id="ad4cd-1440">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1441">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1442">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-1444">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ad4cd-1445">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1446">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-1447">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1448">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-1449">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1450">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1451">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ad4cd-1452">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ad4cd-1453">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ad4cd-1454">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1455">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1456">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ad4cd-1457">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ad4cd-1458">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-1460">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ad4cd-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="ad4cd-1462">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ad4cd-1463">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ad4cd-1464">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ad4cd-1465">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1466">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-1467">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ad4cd-1468">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1469">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-1470">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ad4cd-1471">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ad4cd-1472">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ad4cd-1473">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1474">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1475">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ad4cd-1476">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ad4cd-1477">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ad4cd-1479">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ad4cd-1480">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ad4cd-1481">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="ad4cd-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad4cd-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad4cd-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ad4cd-1485">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ad4cd-1486">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ad4cd-1487">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ad4cd-1488">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad4cd-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1489">Az.RedisCache</span></span>
* <span data-ttu-id="ad4cd-1490">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1491">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1492">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1493">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1494">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ad4cd-1495">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ad4cd-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ad4cd-1497">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ad4cd-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad4cd-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1499">Az.StorageSync</span></span>
* <span data-ttu-id="ad4cd-1500">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1501">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1502">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ad4cd-1503">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-1505">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ad4cd-1506">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ad4cd-1507">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1508">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-1509">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ad4cd-1510">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ad4cd-1511">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1512">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1513">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ad4cd-1514">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ad4cd-1515">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ad4cd-1516">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ad4cd-1517">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ad4cd-1518">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ad4cd-1519">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ad4cd-1520">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ad4cd-1521">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1522">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1523">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ad4cd-1524">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1525">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-1526">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1527">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-1528">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ad4cd-1529">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ad4cd-1530">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="ad4cd-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad4cd-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad4cd-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad4cd-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1535">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-1536">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ad4cd-1537">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ad4cd-1538">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ad4cd-1539">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ad4cd-1540">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ad4cd-1541">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ad4cd-1542">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ad4cd-1543">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ad4cd-1544">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ad4cd-1545">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ad4cd-1546">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ad4cd-1547">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ad4cd-1548">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ad4cd-1549">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ad4cd-1550">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ad4cd-1551">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ad4cd-1552">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ad4cd-1553">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ad4cd-1554">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ad4cd-1555">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1555">Overall improved help files</span></span>
* <span data-ttu-id="ad4cd-1556">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1557">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1558">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ad4cd-1559">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ad4cd-1560">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ad4cd-1561">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ad4cd-1562">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ad4cd-1563">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ad4cd-1564">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ad4cd-1565">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ad4cd-1566">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ad4cd-1567">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ad4cd-1568">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ad4cd-1569">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ad4cd-1570">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1570">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ad4cd-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ad4cd-1573">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1574">New-VpnSite</span></span>
        - <span data-ttu-id="ad4cd-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="ad4cd-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="ad4cd-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="ad4cd-1578">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1580">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ad4cd-1581">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1582">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1583">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-1585">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ad4cd-1586">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ad4cd-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad4cd-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad4cd-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad4cd-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ad4cd-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad4cd-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad4cd-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad4cd-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad4cd-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ad4cd-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad4cd-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad4cd-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad4cd-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ad4cd-1600">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad4cd-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1601">Az.SignalR</span></span>
* <span data-ttu-id="ad4cd-1602">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1603">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1604">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ad4cd-1605">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ad4cd-1606">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ad4cd-1607">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ad4cd-1608">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1609">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1610">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ad4cd-1611">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ad4cd-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ad4cd-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ad4cd-1614">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ad4cd-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ad4cd-1616">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ad4cd-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad4cd-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad4cd-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad4cd-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1621">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1622">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ad4cd-1623">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ad4cd-1624">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ad4cd-1625">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ad4cd-1626">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1626">General</span></span>
* <span data-ttu-id="ad4cd-1627">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1628">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1629">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1630">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-1631">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ad4cd-1632">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-1634">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ad4cd-1635">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ad4cd-1636">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ad4cd-1637">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ad4cd-1638">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1639">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-1640">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1641">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-1642">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1643">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1644">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ad4cd-1645">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ad4cd-1646">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ad4cd-1647">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ad4cd-1648">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ad4cd-1649">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ad4cd-1650">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ad4cd-1651">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1652">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1653">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ad4cd-1654">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ad4cd-1655">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ad4cd-1656">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-1658">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1659">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-1660">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ad4cd-1661">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ad4cd-1662">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ad4cd-1663">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ad4cd-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ad4cd-1665">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1666">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-1667">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1668">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1669">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ad4cd-1670">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ad4cd-1671">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ad4cd-1672">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ad4cd-1673">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ad4cd-1674">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ad4cd-1675">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-1677">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ad4cd-1678">新增了範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1678">Added example</span></span>
    - <span data-ttu-id="ad4cd-1679">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ad4cd-1680">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ad4cd-1681">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1683">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1684">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1685">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ad4cd-1686">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ad4cd-1687">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ad4cd-1688">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-1690">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ad4cd-1691">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ad4cd-1692">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-1694">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ad4cd-1695">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ad4cd-1696">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ad4cd-1697">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ad4cd-1698">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ad4cd-1699">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1700">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1701">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1702">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1703">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ad4cd-1704">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ad4cd-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ad4cd-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ad4cd-1707">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ad4cd-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1709">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1710">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ad4cd-1711">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1712">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1713">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ad4cd-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ad4cd-1715">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1716">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-1717">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-1719">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1720">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1721">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ad4cd-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ad4cd-1723">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ad4cd-1724">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1725">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1726">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ad4cd-1727">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1728">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-1729">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ad4cd-1730">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1731">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-1732">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad4cd-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1733">Az.LogicApp</span></span>
* <span data-ttu-id="ad4cd-1734">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ad4cd-1735">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ad4cd-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="ad4cd-1737">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1738">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1739">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ad4cd-1740">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1740">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad4cd-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad4cd-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad4cd-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ad4cd-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ad4cd-1749">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ad4cd-1750">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ad4cd-1751">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ad4cd-1752">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ad4cd-1753">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ad4cd-1754">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ad4cd-1755">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad4cd-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad4cd-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ad4cd-1759">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ad4cd-1760">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ad4cd-1761">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ad4cd-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ad4cd-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ad4cd-1765">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ad4cd-1766">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ad4cd-1767">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-1769">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ad4cd-1770">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1772">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ad4cd-1773">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ad4cd-1774">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ad4cd-1775">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ad4cd-1776">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ad4cd-1777">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ad4cd-1778">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ad4cd-1779">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ad4cd-1780">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ad4cd-1781">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1782">Az.Resources</span></span>
- <span data-ttu-id="ad4cd-1783">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ad4cd-1784">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-1786">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ad4cd-1787">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1788">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1789">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ad4cd-1790">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ad4cd-1791">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1792">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1793">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad4cd-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1794">Az.StorageSync</span></span>
* <span data-ttu-id="ad4cd-1795">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ad4cd-1796">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1797">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1798">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ad4cd-1799">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ad4cd-1800">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ad4cd-1801">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1802">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1803">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ad4cd-1804">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ad4cd-1805">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ad4cd-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1806">Az.Advisor</span></span>
* <span data-ttu-id="ad4cd-1807">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ad4cd-1808">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-1810">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ad4cd-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ad4cd-1812">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ad4cd-1813">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ad4cd-1814">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ad4cd-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ad4cd-1816">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1817">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-1818">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1819">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1820">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1821">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-1822">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad4cd-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1823">Az.EventGrid</span></span>
* <span data-ttu-id="ad4cd-1824">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1825">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-1826">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1827">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1828">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ad4cd-1829">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-1831">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ad4cd-1832">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-1834">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-1836">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1837">Az.Resources</span></span>
    - <span data-ttu-id="ad4cd-1838">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ad4cd-1839">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ad4cd-1840">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ad4cd-1841">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-1843">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1844">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1845">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ad4cd-1846">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ad4cd-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad4cd-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad4cd-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad4cd-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ad4cd-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ad4cd-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ad4cd-1853">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1854">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1855">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ad4cd-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ad4cd-1857">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ad4cd-1858">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ad4cd-1859">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ad4cd-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ad4cd-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ad4cd-1862">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ad4cd-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ad4cd-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad4cd-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1865">Az.StorageSync</span></span>
* <span data-ttu-id="ad4cd-1866">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ad4cd-1867">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1868">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-1869">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ad4cd-1870">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ad4cd-1871">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ad4cd-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ad4cd-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1874">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1875">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ad4cd-1876">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ad4cd-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1877">Az.Dns</span></span>
* <span data-ttu-id="ad4cd-1878">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad4cd-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1879">Az.EventGrid</span></span>
* <span data-ttu-id="ad4cd-1880">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ad4cd-1881">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1881">New cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad4cd-1883">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad4cd-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad4cd-1885">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ad4cd-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad4cd-1887">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad4cd-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ad4cd-1889">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad4cd-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ad4cd-1891">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ad4cd-1892">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ad4cd-1893">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ad4cd-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ad4cd-1895">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ad4cd-1896">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ad4cd-1897">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ad4cd-1898">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ad4cd-1900">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ad4cd-1901">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ad4cd-1902">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ad4cd-1903">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ad4cd-1904">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ad4cd-1905">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ad4cd-1906">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ad4cd-1907">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ad4cd-1908">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ad4cd-1909">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ad4cd-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ad4cd-1911">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ad4cd-1912">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ad4cd-1915">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ad4cd-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ad4cd-1917">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1918">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1919">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ad4cd-1920">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1920">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ad4cd-1922">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ad4cd-1923">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1923">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ad4cd-1925">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ad4cd-1926">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1926">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad4cd-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad4cd-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad4cd-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ad4cd-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ad4cd-1932">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ad4cd-1933">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1933">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad4cd-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad4cd-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad4cd-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ad4cd-1938">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ad4cd-1939">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ad4cd-1940">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ad4cd-1941">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ad4cd-1942">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ad4cd-1943">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ad4cd-1944">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ad4cd-1945">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ad4cd-1946">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ad4cd-1947">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ad4cd-1948">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ad4cd-1949">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ad4cd-1950">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ad4cd-1951">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ad4cd-1952">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-1953">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ad4cd-1954">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ad4cd-1955">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ad4cd-1956">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ad4cd-1957">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ad4cd-1958">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ad4cd-1959">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ad4cd-1960">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-1962">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1963">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-1964">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ad4cd-1965">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ad4cd-1966">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ad4cd-1967">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-1969">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1970">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-1971">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ad4cd-1972">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ad4cd-1973">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ad4cd-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad4cd-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad4cd-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad4cd-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ad4cd-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1979">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-1980">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ad4cd-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="ad4cd-1982">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ad4cd-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1984">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-1985">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ad4cd-1986">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ad4cd-1987">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ad4cd-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1988">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-1989">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1990">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-1991">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ad4cd-1992">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1993">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-1994">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ad4cd-1995">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1996">Az.Network</span></span>
* <span data-ttu-id="ad4cd-1997">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ad4cd-1998">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-2000">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2002">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-2004">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-2006">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ad4cd-2007">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2008">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2009">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ad4cd-2010">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ad4cd-2011">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ad4cd-2012">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2013">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2014">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ad4cd-2015">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-2017">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ad4cd-2018">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ad4cd-2019">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ad4cd-2020">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ad4cd-2021">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ad4cd-2022">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ad4cd-2023">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ad4cd-2024">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ad4cd-2025">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ad4cd-2026">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ad4cd-2027">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ad4cd-2028">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ad4cd-2029">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ad4cd-2030">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ad4cd-2031">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ad4cd-2032">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ad4cd-2033">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ad4cd-2034">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ad4cd-2035">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ad4cd-2036">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ad4cd-2037">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ad4cd-2038">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ad4cd-2039">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ad4cd-2040">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ad4cd-2041">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ad4cd-2042">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ad4cd-2043">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ad4cd-2044">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ad4cd-2045">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ad4cd-2046">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ad4cd-2047">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ad4cd-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ad4cd-2049">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ad4cd-2050">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ad4cd-2051">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ad4cd-2052">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ad4cd-2053">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ad4cd-2054">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ad4cd-2055">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ad4cd-2056">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ad4cd-2057">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ad4cd-2058">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ad4cd-2059">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ad4cd-2060">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ad4cd-2061">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ad4cd-2062">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ad4cd-2063">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ad4cd-2064">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ad4cd-2065">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ad4cd-2066">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ad4cd-2067">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ad4cd-2068">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ad4cd-2069">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ad4cd-2070">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ad4cd-2071">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ad4cd-2072">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ad4cd-2073">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ad4cd-2074">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ad4cd-2075">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ad4cd-2076">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ad4cd-2077">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ad4cd-2078">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ad4cd-2079">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ad4cd-2080">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ad4cd-2081">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ad4cd-2082">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ad4cd-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ad4cd-2084">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ad4cd-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ad4cd-2086">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ad4cd-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ad4cd-2088">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ad4cd-2089">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ad4cd-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ad4cd-2091">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ad4cd-2092">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ad4cd-2093">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2094">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2095">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ad4cd-2096">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ad4cd-2097">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ad4cd-2098">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ad4cd-2099">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ad4cd-2100">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ad4cd-2101">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2102">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2103">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ad4cd-2104">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2106">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2107">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-2108">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2109">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2110">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ad4cd-2111">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad4cd-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ad4cd-2113">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2114">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2115">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2116">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2117">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ad4cd-2118">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2119">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2120">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-2122">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ad4cd-2123">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2124">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2125">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ad4cd-2126">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ad4cd-2127">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ad4cd-2128">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ad4cd-2129">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ad4cd-2130">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ad4cd-2131">重大變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2131">Breaking changes</span></span>
    - <span data-ttu-id="ad4cd-2132">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ad4cd-2133">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ad4cd-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="ad4cd-2135">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ad4cd-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2136">Az.Dns</span></span>
* <span data-ttu-id="ad4cd-2137">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ad4cd-2138">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ad4cd-2139">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="ad4cd-2141">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ad4cd-2142">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2143">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-2144">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ad4cd-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ad4cd-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ad4cd-2147">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ad4cd-2148">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ad4cd-2149">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ad4cd-2150">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2151">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-2152">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ad4cd-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ad4cd-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ad4cd-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ad4cd-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ad4cd-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ad4cd-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ad4cd-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad4cd-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad4cd-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad4cd-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad4cd-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad4cd-2164">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ad4cd-2165">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2166">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2167">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ad4cd-2168">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2168">New cmdlets</span></span>
        - <span data-ttu-id="ad4cd-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="ad4cd-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ad4cd-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ad4cd-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ad4cd-2173">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="ad4cd-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ad4cd-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ad4cd-2176">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ad4cd-2177">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ad4cd-2178">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-2180">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ad4cd-2181">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ad4cd-2182">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2184">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ad4cd-2185">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ad4cd-2186">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ad4cd-2187">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ad4cd-2188">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ad4cd-2189">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ad4cd-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2190">Az.Relay</span></span>
* <span data-ttu-id="ad4cd-2191">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-2193">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2194">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2195">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ad4cd-2196">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ad4cd-2197">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ad4cd-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="ad4cd-2199">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ad4cd-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ad4cd-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ad4cd-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2203">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2204">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ad4cd-2205">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ad4cd-2206">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-2207">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-2208">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="ad4cd-2209">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad4cd-2210">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad4cd-2211">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad4cd-2212">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad4cd-2213">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2214">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2215">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2216">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad4cd-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2217">Az.Batch</span></span>
* <span data-ttu-id="ad4cd-2218">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2219">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-2220">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-2222">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2223">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2224">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ad4cd-2225">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2226">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2227">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-2228">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2230">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad4cd-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2231">Az.EventGrid</span></span>
* <span data-ttu-id="ad4cd-2232">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2233">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-2234">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad4cd-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2235">Az.HDInsight</span></span>
* <span data-ttu-id="ad4cd-2236">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2237">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-2238">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2239">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-2240">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2241">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ad4cd-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="ad4cd-2243">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ad4cd-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2244">Az.Media</span></span>
* <span data-ttu-id="ad4cd-2245">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2246">Az.Monitor</span></span>
  * <span data-ttu-id="ad4cd-2247">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ad4cd-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ad4cd-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ad4cd-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ad4cd-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ad4cd-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ad4cd-2253">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2254">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2255">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2256">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ad4cd-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="ad4cd-2258">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-2260">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ad4cd-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad4cd-2262">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2264">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2265">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ad4cd-2266">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ad4cd-2267">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad4cd-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2268">Az.RedisCache</span></span>
* <span data-ttu-id="ad4cd-2269">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2270">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2271">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2272">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2273">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ad4cd-2274">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2275">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ad4cd-2276">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ad4cd-2277">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ad4cd-2278">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ad4cd-2279">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2280">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2281">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ad4cd-2282">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad4cd-2283">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ad4cd-2284">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ad4cd-2285">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-2286">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-2287">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="ad4cd-2288">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad4cd-2289">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad4cd-2290">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad4cd-2291">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad4cd-2292">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2293">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2294">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2295">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad4cd-2297">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ad4cd-2298">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2299">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2300">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ad4cd-2301">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ad4cd-2302">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2303">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2304">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ad4cd-2305">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ad4cd-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="ad4cd-2307">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2308">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-2309">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ad4cd-2310">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2311">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2312">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ad4cd-2313">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ad4cd-2314">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ad4cd-2315">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ad4cd-2316">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ad4cd-2317">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2318">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2319">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2320">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2321">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ad4cd-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="ad4cd-2323">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ad4cd-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ad4cd-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ad4cd-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ad4cd-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ad4cd-2328">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ad4cd-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ad4cd-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ad4cd-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ad4cd-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ad4cd-2333">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad4cd-2334">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="ad4cd-2335">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="ad4cd-2336">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad4cd-2337">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad4cd-2338">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad4cd-2339">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad4cd-2340">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2341">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2342">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2343">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ad4cd-2344">動態分組</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="ad4cd-2345">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2345">Pre-Post script</span></span>
    * <span data-ttu-id="ad4cd-2346">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2347">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2348">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ad4cd-2349">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2350">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-2351">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2352">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2353">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ad4cd-2354">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2356">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ad4cd-2357">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2358">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2359">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ad4cd-2360">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2361">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2362">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2363">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2364">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ad4cd-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad4cd-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad4cd-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad4cd-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ad4cd-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ad4cd-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2371">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2372">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ad4cd-2373">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2374">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2375">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ad4cd-2376">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2377">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2378">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ad4cd-2379">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ad4cd-2380">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2381">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-2382">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2383">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2384">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2385">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-2386">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad4cd-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2387">Az.LogicApp</span></span>
* <span data-ttu-id="ad4cd-2388">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2389">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2390">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2392">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ad4cd-2393">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2393">SDK Update</span></span>
* <span data-ttu-id="ad4cd-2394">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ad4cd-2395">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2396">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2397">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ad4cd-2398">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ad4cd-2399">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ad4cd-2400">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ad4cd-2401">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ad4cd-2402">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2403">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2404">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ad4cd-2405">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2406">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2407">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ad4cd-2408">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad4cd-2410">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2411">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2412">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ad4cd-2413">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ad4cd-2414">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-2416">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2417">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2418">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ad4cd-2419">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ad4cd-2420">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ad4cd-2421">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2423">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad4cd-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2424">Az.EventHub</span></span>
* <span data-ttu-id="ad4cd-2425">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2426">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-2427">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad4cd-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2428">Az.LogicApp</span></span>
* <span data-ttu-id="ad4cd-2429">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ad4cd-2430">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ad4cd-2431">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ad4cd-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad4cd-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad4cd-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad4cd-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ad4cd-2436">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ad4cd-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad4cd-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad4cd-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad4cd-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ad4cd-2441">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad4cd-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2442">Az.Monitor</span></span>
* <span data-ttu-id="ad4cd-2443">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2444">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2445">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad4cd-2447">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ad4cd-2448">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ad4cd-2449">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2450">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2451">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ad4cd-2452">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ad4cd-2453">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ad4cd-2454">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2455">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2456">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ad4cd-2457">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2458">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2459">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ad4cd-2460">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2461">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2462">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="ad4cd-2464">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2465">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2466">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ad4cd-2467">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ad4cd-2468">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="ad4cd-2470">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2471">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2472">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ad4cd-2473">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ad4cd-2474">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ad4cd-2475">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2476">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2477">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ad4cd-2478">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ad4cd-2479">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ad4cd-2480">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2481">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2482">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad4cd-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad4cd-2484">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad4cd-2486">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ad4cd-2487">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2488">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2489">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad4cd-2490">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad4cd-2491">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad4cd-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2492">Az.Aks</span></span>
* <span data-ttu-id="ad4cd-2493">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad4cd-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2494">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2495">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ad4cd-2496">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad4cd-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2497">Az.Cdn</span></span>
* <span data-ttu-id="ad4cd-2498">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2499">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2500">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ad4cd-2501">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ad4cd-2502">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ad4cd-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ad4cd-2504">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad4cd-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2505">Az.DataFactory</span></span>
* <span data-ttu-id="ad4cd-2506">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2508">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ad4cd-2509">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ad4cd-2510">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2511">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-2512">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2513">Az.KeyVault</span></span>
* <span data-ttu-id="ad4cd-2514">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2515">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2516">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2517">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2518">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ad4cd-2519">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ad4cd-2520">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ad4cd-2521">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ad4cd-2522">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ad4cd-2523">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ad4cd-2524">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-2526">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ad4cd-2527">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2527">Fix some error messages.</span></span>
* <span data-ttu-id="ad4cd-2528">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ad4cd-2529">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad4cd-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2530">Az.SignalR</span></span>
* <span data-ttu-id="ad4cd-2531">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2532">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2533">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad4cd-2534">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ad4cd-2535">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ad4cd-2536">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2537">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2538">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad4cd-2539">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ad4cd-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ad4cd-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ad4cd-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="ad4cd-2543">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2544">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2545">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad4cd-2546">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ad4cd-2547">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ad4cd-2548">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2549">Az.Accounts</span></span>
* <span data-ttu-id="ad4cd-2550">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2551">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2552">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ad4cd-2553">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ad4cd-2554">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2556">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ad4cd-2557">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad4cd-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2558">Az.EventGrid</span></span>
* <span data-ttu-id="ad4cd-2559">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ad4cd-2560">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ad4cd-2561">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ad4cd-2562">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ad4cd-2563">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ad4cd-2564">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ad4cd-2565">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ad4cd-2566">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ad4cd-2567">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ad4cd-2568">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="ad4cd-2569">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ad4cd-2570">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad4cd-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2571">Az.IotHub</span></span>
* <span data-ttu-id="ad4cd-2572">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad4cd-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2573">Az.LogicApp</span></span>
* <span data-ttu-id="ad4cd-2574">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2575">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2576">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ad4cd-2577">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ad4cd-2578">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ad4cd-2579">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ad4cd-2580">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ad4cd-2581">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad4cd-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2582">Az.SignalR</span></span>
* <span data-ttu-id="ad4cd-2583">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2584">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2585">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad4cd-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2586">Az.Storage</span></span>
* <span data-ttu-id="ad4cd-2587">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ad4cd-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="ad4cd-2589">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ad4cd-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2591">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2592">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ad4cd-2593">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ad4cd-2594">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ad4cd-2595">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2595">General</span></span>

- <span data-ttu-id="ad4cd-2596">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="ad4cd-2597">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2597">Online help for each module</span></span>
- <span data-ttu-id="ad4cd-2598">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ad4cd-2599">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ad4cd-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2600">Az.Accounts</span></span>
- <span data-ttu-id="ad4cd-2601">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="ad4cd-2602">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="ad4cd-2604">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2604">Fixes for #7002</span></span>
- <span data-ttu-id="ad4cd-2605">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ad4cd-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2606">Az.Batch</span></span>
- <span data-ttu-id="ad4cd-2607">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ad4cd-2608">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ad4cd-2609">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ad4cd-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2610">Az.Billing</span></span>
- <span data-ttu-id="ad4cd-2611">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ad4cd-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="ad4cd-2613">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ad4cd-2614">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ad4cd-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="ad4cd-2616">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ad4cd-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ad4cd-2618">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="ad4cd-2620">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ad4cd-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2621">Az.Monitor</span></span>
- <span data-ttu-id="ad4cd-2622">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ad4cd-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2623">Az.KeyVault</span></span>
- <span data-ttu-id="ad4cd-2624">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ad4cd-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="ad4cd-2626">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ad4cd-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2627">Az.Media</span></span>
- <span data-ttu-id="ad4cd-2628">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2629">Az.Network</span></span>
<span data-ttu-id="ad4cd-2630">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ad4cd-2631">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="ad4cd-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ad4cd-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ad4cd-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ad4cd-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ad4cd-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ad4cd-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ad4cd-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ad4cd-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ad4cd-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ad4cd-2646">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ad4cd-2647">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ad4cd-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ad4cd-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ad4cd-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ad4cd-2651">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ad4cd-2652">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ad4cd-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="ad4cd-2654">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ad4cd-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2655">Az.Profile</span></span>
- <span data-ttu-id="ad4cd-2656">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="ad4cd-2658">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ad4cd-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2659">Az.Resources</span></span>
- <span data-ttu-id="ad4cd-2660">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="ad4cd-2662">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ad4cd-2663">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ad4cd-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="ad4cd-2665">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ad4cd-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2666">Az.Sql</span></span>
- <span data-ttu-id="ad4cd-2667">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ad4cd-2668">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ad4cd-2669">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ad4cd-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2670">Az.Storage</span></span>
- <span data-ttu-id="ad4cd-2671">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2672">Az.Websites</span></span>
- <span data-ttu-id="ad4cd-2673">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ad4cd-2674">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ad4cd-2675">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2675">General</span></span>

* <span data-ttu-id="ad4cd-2676">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ad4cd-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2677">Az.Compute</span></span>

* <span data-ttu-id="ad4cd-2678">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="ad4cd-2680">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ad4cd-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="ad4cd-2682">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="ad4cd-2683">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ad4cd-2684">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ad4cd-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="ad4cd-2686">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ad4cd-2687">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ad4cd-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2688">Az.Resources</span></span>

* <span data-ttu-id="ad4cd-2689">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ad4cd-2690">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ad4cd-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2691">Az.Sql</span></span>

* <span data-ttu-id="ad4cd-2692">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ad4cd-2693">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ad4cd-2694">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ad4cd-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2695">Az.Storage</span></span>

* <span data-ttu-id="ad4cd-2696">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ad4cd-2697">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ad4cd-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ad4cd-2699">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="ad4cd-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ad4cd-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2702">Az.Websites</span></span>

* <span data-ttu-id="ad4cd-2703">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ad4cd-2704">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ad4cd-2705">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ad4cd-2706">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ad4cd-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="ad4cd-2708">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ad4cd-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2709">Az.Automation</span></span>
* <span data-ttu-id="ad4cd-2710">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ad4cd-2711">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ad4cd-2712">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ad4cd-2713">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ad4cd-2714">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ad4cd-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2715">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2716">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ad4cd-2717">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ad4cd-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="ad4cd-2719">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ad4cd-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ad4cd-2721">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2722">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2723">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ad4cd-2724">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ad4cd-2725">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ad4cd-2726">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ad4cd-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ad4cd-2728">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ad4cd-2729">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ad4cd-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ad4cd-2731">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ad4cd-2732">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ad4cd-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2733">Az.Relay</span></span>
* <span data-ttu-id="ad4cd-2734">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ad4cd-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2735">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2736">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ad4cd-2737">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ad4cd-2738">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-2740">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ad4cd-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2741">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2742">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ad4cd-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad4cd-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad4cd-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad4cd-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad4cd-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad4cd-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad4cd-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad4cd-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ad4cd-2751">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ad4cd-2752">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ad4cd-2753">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ad4cd-2754">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ad4cd-2755">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ad4cd-2756">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ad4cd-2757">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ad4cd-2758">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ad4cd-2759">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad4cd-2760">一般</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2760">General</span></span>
* <span data-ttu-id="ad4cd-2761">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ad4cd-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2762">Az.Profile</span></span>
* <span data-ttu-id="ad4cd-2763">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ad4cd-2764">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ad4cd-2765">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ad4cd-2766">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ad4cd-2767">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ad4cd-2768">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ad4cd-2769">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-2771">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2772">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2773">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ad4cd-2774">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ad4cd-2775">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2777">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ad4cd-2778">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ad4cd-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2779">Az.Insights</span></span>
* <span data-ttu-id="ad4cd-2780">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ad4cd-2781">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ad4cd-2782">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ad4cd-2783">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2784">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2785">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ad4cd-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ad4cd-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ad4cd-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ad4cd-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ad4cd-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ad4cd-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad4cd-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad4cd-2793">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2794">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2795">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ad4cd-2796">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad4cd-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="ad4cd-2798">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad4cd-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad4cd-2800">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ad4cd-2801">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ad4cd-2802">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ad4cd-2803">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ad4cd-2804">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ad4cd-2805">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ad4cd-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2806">Az.Profile</span></span>
* <span data-ttu-id="ad4cd-2807">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ad4cd-2808">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2809">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2810">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ad4cd-2811">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad4cd-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad4cd-2813">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ad4cd-2814">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ad4cd-2815">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ad4cd-2816">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ad4cd-2817">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2818">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2819">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ad4cd-2820">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2821">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2822">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ad4cd-2823">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ad4cd-2824">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ad4cd-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2825">Azure.Storage</span></span>
* <span data-ttu-id="ad4cd-2826">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ad4cd-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ad4cd-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ad4cd-2829">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ad4cd-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad4cd-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad4cd-2832">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad4cd-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2833">Az.Compute</span></span>
* <span data-ttu-id="ad4cd-2834">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ad4cd-2835">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ad4cd-2836">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ad4cd-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ad4cd-2838">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad4cd-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2839">Az.Network</span></span>
* <span data-ttu-id="ad4cd-2840">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ad4cd-2841">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2841">new cmdlets added</span></span>
    - <span data-ttu-id="ad4cd-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad4cd-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad4cd-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad4cd-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad4cd-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ad4cd-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ad4cd-2848">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ad4cd-2849">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ad4cd-2850">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad4cd-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2851">Az.RedisCache</span></span>
* <span data-ttu-id="ad4cd-2852">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ad4cd-2853">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad4cd-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2854">Az.Resources</span></span>
* <span data-ttu-id="ad4cd-2855">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ad4cd-2856">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad4cd-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2857">Az.Sql</span></span>
* <span data-ttu-id="ad4cd-2858">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad4cd-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2859">Az.Websites</span></span>
* <span data-ttu-id="ad4cd-2860">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ad4cd-2861">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ad4cd-2862">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ad4cd-2863">初始版本</span><span class="sxs-lookup"><span data-stu-id="ad4cd-2863">Initial Release</span></span>
