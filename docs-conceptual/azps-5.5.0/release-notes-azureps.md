---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 0fe1d2360af5a05953a08eaf3b3eaf0bf5ddcda5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012541"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f5912-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-103">Azure PowerShell release notes</span></span>

## <a name="550---february-2021"></a><span data-ttu-id="f5912-104">5.5.0-2021 年2月</span><span class="sxs-lookup"><span data-stu-id="f5912-104">5.5.0 - February 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-105">Az.Accounts</span></span>
* <span data-ttu-id="f5912-106">例外狀況中追蹤的 CloudError 程式碼</span><span class="sxs-lookup"><span data-stu-id="f5912-106">Tracked CloudError code in exception</span></span>
* <span data-ttu-id="f5912-107">執行 ' Clear Set-azcoNtext ' 時引發 ' CoNtextCleared ' 事件</span><span class="sxs-lookup"><span data-stu-id="f5912-107">Raised 'ContextCleared' event when 'Clear-AzContext' was executed</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-108">Az.Aks</span></span>
* <span data-ttu-id="f5912-109">精簡 Cmdlet 失敗的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-109">Refined error messages of cmdlet failure.</span></span>
* <span data-ttu-id="f5912-110">升級的例外狀況處理，以使用 Azure PowerShell 相關的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f5912-110">Upgraded exception handling to use Azure PowerShell related exceptions.</span></span>
* <span data-ttu-id="f5912-111">修正使用者無法使用提供的服務主體來建立 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-111">Fixed the issue that user could not use provided service principal to create Kubernetes cluster.</span></span> <span data-ttu-id="f5912-112">[#13938]</span><span class="sxs-lookup"><span data-stu-id="f5912-112">[#13938]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-113">Az.Automation</span></span>
* <span data-ttu-id="f5912-114">已修正處理 ' PSCustomObject ' 和 ' Array ' 的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-114">Fixed the issue of processing 'PSCustomObject' and 'Array'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-115">Az.Compute</span></span>
* <span data-ttu-id="f5912-116">已將參數 '-EnableAutomaticUpgrade ' 新增至 ' >remove-azvmextension ' 和 ' >add-azvmssextension '。</span><span class="sxs-lookup"><span data-stu-id="f5912-116">Added parameter '-EnableAutomaticUpgrade' to 'Set-AzVmExtension' and 'Add-AzVmssExtension'.</span></span>
* <span data-ttu-id="f5912-117">已從 ' >get-azvmimage ' Cmdlet 檔中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-117">Removed FilterExpression parameter from 'Get-AzVMImage' cmdlet documentation.</span></span> 
* <span data-ttu-id="f5912-118">已將取代訊息新增至 >microsoft.containerservice Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-118">Added deprecation message to the ContainerService cmdlets:</span></span>
    - <span data-ttu-id="f5912-119">' AzureRmContainerServiceAgentPoolProfileCommand '</span><span class="sxs-lookup"><span data-stu-id="f5912-119">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span></span>
    - <span data-ttu-id="f5912-120">' AzContainerService '</span><span class="sxs-lookup"><span data-stu-id="f5912-120">'Get-AzContainerService'</span></span>
    - <span data-ttu-id="f5912-121">' AzContainerService '</span><span class="sxs-lookup"><span data-stu-id="f5912-121">'New-AzContainerService'</span></span>
    - <span data-ttu-id="f5912-122">' AzContainerServiceConfig '</span><span class="sxs-lookup"><span data-stu-id="f5912-122">'New-AzContainerServiceConfig'</span></span>
    - <span data-ttu-id="f5912-123">' AzContainerService '</span><span class="sxs-lookup"><span data-stu-id="f5912-123">'Remove-AzContainerService'</span></span>
    - <span data-ttu-id="f5912-124">' AzContainerServiceAgentPoolProfile '</span><span class="sxs-lookup"><span data-stu-id="f5912-124">'Remove-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="f5912-125">' AzContainerService '</span><span class="sxs-lookup"><span data-stu-id="f5912-125">'Update-AzContainerService'</span></span>
* <span data-ttu-id="f5912-126">已將參數 '-BurstingEnabled ' 新增至 ' New-azdiskconfig ' 和 ' AzDiskUpdateConfig '</span><span class="sxs-lookup"><span data-stu-id="f5912-126">Added parameter '-BurstingEnabled' to 'New-AzDiskConfig' and 'New-AzDiskUpdateConfig'</span></span>
* <span data-ttu-id="f5912-127">已將 '-GroupByApplicationId ' 和 '-GroupByUserAgent ' 參數新增至 ' Export-AzLogAnalyticThrottledRequest ' 和 ' Export-AzLogAnalyticRequestRateByInterval ' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-127">Added '-GroupByApplicationId' and '-GroupByUserAgent' parameters to the 'Export-AzLogAnalyticThrottledRequest' and 'Export-AzLogAnalyticRequestRateByInterval' cmdlets.</span></span>
* <span data-ttu-id="f5912-128">已將 ' VMParameterSet ' 參數設定為 ' >remove-azvmextension ' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-128">Added 'VMParameterSet' parameter set to 'Get-AzVMExtension' cmdlet.</span></span> <span data-ttu-id="f5912-129">已將新的參數 '-VM ' 新增至此參數集。</span><span class="sxs-lookup"><span data-stu-id="f5912-129">Added new parameter '-VM' to this parameter set.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5912-130">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5912-130">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5912-131">已將 Cmdlet 新增至支援的存放庫、資訊清單和標記作業：</span><span class="sxs-lookup"><span data-stu-id="f5912-131">Added cmdlets to supported repository, manifest, and tag operations:</span></span>
    - <span data-ttu-id="f5912-132">' AzContainerRegistryRepository '</span><span class="sxs-lookup"><span data-stu-id="f5912-132">'Get-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="f5912-133">' AzContainerRegistryRepository '</span><span class="sxs-lookup"><span data-stu-id="f5912-133">'Update-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="f5912-134">' AzContainerRegistryRepository '</span><span class="sxs-lookup"><span data-stu-id="f5912-134">'Remove-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="f5912-135">' AzContainerRegistryManifest '</span><span class="sxs-lookup"><span data-stu-id="f5912-135">'Get-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="f5912-136">' AzContainerRegistryManifest '</span><span class="sxs-lookup"><span data-stu-id="f5912-136">'Update-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="f5912-137">' AzContainerRegistryManifest '</span><span class="sxs-lookup"><span data-stu-id="f5912-137">'Remove-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="f5912-138">' AzContainerRegistryTag '</span><span class="sxs-lookup"><span data-stu-id="f5912-138">'Get-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="f5912-139">' AzContainerRegistryTag '</span><span class="sxs-lookup"><span data-stu-id="f5912-139">'Update-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="f5912-140">' AzContainerRegistryTag '</span><span class="sxs-lookup"><span data-stu-id="f5912-140">'Remove-AzContainerRegistryTag'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="f5912-141">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="f5912-141">Az.Databricks</span></span>
<span data-ttu-id="f5912-142">支援-在建立 Databricks 工作區時 EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="f5912-142">Supported -EnableNoPublicIP when creating a Databricks workspace</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-143">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-143">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-144">已將 FrontDoorId 新增至屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-144">Added FrontDoorId to properties</span></span>
* <span data-ttu-id="f5912-145">已將 JSON 排除專案和 RequestBodyCheck 支援新增至受控規則</span><span class="sxs-lookup"><span data-stu-id="f5912-145">Added JSON Exclusions and RequestBodyCheck support to managed rules</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-146">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-146">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-147">已將新的參數 '-EnableComputeIsolation ' 和 '-ComputeIsolationHostSku ' 新增至 Cmdlet ' >new-azhdinsightcluster '，以支援計算隔離功能</span><span class="sxs-lookup"><span data-stu-id="f5912-147">Added new parameter '-EnableComputeIsolation' and '-ComputeIsolationHostSku' to the cmdlet 'New-AzHDInsightCluster' to support compute isolation feature</span></span>
* <span data-ttu-id="f5912-148">已在類別 AzureHDInsightCluster 中新增屬性 ' ComputeIsolationProperties ' 和 ' ConnectivityEndpoints '。</span><span class="sxs-lookup"><span data-stu-id="f5912-148">Added property 'ComputeIsolationProperties' and 'ConnectivityEndpoints' in the class AzureHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-149">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-150">在透過 BYOK 檔案匯入金鑰時，支援指定金鑰類型和曲線名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-150">Supported specifying key type and curve name when importing keys via a BYOK file</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-151">Az.Network</span></span>
* <span data-ttu-id="f5912-152">已新增新的 Cmdlet，以將舊的產品名稱 ' virtual 路由器 ' 取代為新名稱 ' route server ' （未來）。</span><span class="sxs-lookup"><span data-stu-id="f5912-152">Added new cmdlets to replace old product name 'virtual router' with new name 'route server' in the future.</span></span>
    - <span data-ttu-id="f5912-153">' AzRouteServer '</span><span class="sxs-lookup"><span data-stu-id="f5912-153">'New-AzRouteServer'</span></span>
    - <span data-ttu-id="f5912-154">' AzRouteServer '</span><span class="sxs-lookup"><span data-stu-id="f5912-154">'Get-AzRouteServer'</span></span>
    - <span data-ttu-id="f5912-155">' AzRouteServer '</span><span class="sxs-lookup"><span data-stu-id="f5912-155">'Remove-AzRouteServer'</span></span>
    - <span data-ttu-id="f5912-156">' AzRouteServer '</span><span class="sxs-lookup"><span data-stu-id="f5912-156">'Update-AzRouteServer'</span></span>
    - <span data-ttu-id="f5912-157">' AzRouteServerPeer '</span><span class="sxs-lookup"><span data-stu-id="f5912-157">'Get-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="f5912-158">' AzRouteServerPeer '</span><span class="sxs-lookup"><span data-stu-id="f5912-158">'Add-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="f5912-159">' AzRouteServerPeer '</span><span class="sxs-lookup"><span data-stu-id="f5912-159">'Update-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="f5912-160">' AzRouteServerPeer '</span><span class="sxs-lookup"><span data-stu-id="f5912-160">'Remove-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="f5912-161">已將取代屬性警告新增至舊的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-161">Added deprecation attribute warning to the old cmdlets.</span></span>
* <span data-ttu-id="f5912-162">修正 ExpressRouteLink MacSecConfig 中的 Bug。</span><span class="sxs-lookup"><span data-stu-id="f5912-162">Bug fix in ExpressRouteLink MacSecConfig.</span></span> <span data-ttu-id="f5912-163">已將新的屬性 ' SciState ' 新增至 ' PSExpressRouteLinkMacSecConfig '</span><span class="sxs-lookup"><span data-stu-id="f5912-163">Added new property 'SciState' to 'PSExpressRouteLinkMacSecConfig'</span></span>
* <span data-ttu-id="f5912-164">更新 Get-AzVirtualNetworkGatewayConnectionIkeSa 的格式清單和格式資料表視圖</span><span class="sxs-lookup"><span data-stu-id="f5912-164">Updated format list and format table views for Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-165">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-165">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-166">撤銷在 powershell 中所做的變更，以增加要求的資料列限制。</span><span class="sxs-lookup"><span data-stu-id="f5912-166">Retracted changes made in powershell that increased request row limit.</span></span> <span data-ttu-id="f5912-167">已移除不正確的支援分頁語句</span><span class="sxs-lookup"><span data-stu-id="f5912-167">Removed incorrect statement of supporting paging</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-168">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-169">依備份服務修改原則驗證限制。</span><span class="sxs-lookup"><span data-stu-id="f5912-169">modified policy validation limits as per backup service.</span></span>
* <span data-ttu-id="f5912-170">已新增復原服務保存庫的區域冗余。</span><span class="sxs-lookup"><span data-stu-id="f5912-170">Added Zone Redundancy for Recovery Service Vaults.</span></span> 
* <span data-ttu-id="f5912-171">Azure Site Recovery VMware 至 Azure 和 HyperV 對 Azure 提供者的鄰近放置群組支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-171">Azure Site Recovery support for Proximity placement group for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="f5912-172">Azure Site Recovery VMware 至 Azure 和 HyperV 對 Azure 提供者的可用性區域支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-172">Azure Site Recovery support for Availability zone for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="f5912-173">針對 UseManagedDisk for HyperV 至 Azure 提供者的支援 Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="f5912-173">Azure Site Recovery support for UseManagedDisk for HyperV to Azure provider</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-174">Az.Resources</span></span>
* <span data-ttu-id="f5912-175">已移除 New-AzRoleAssignment 和 Set-AzRoleAssignment 上的主體類型，因為目前的對應中斷了某些案例</span><span class="sxs-lookup"><span data-stu-id="f5912-175">Removed principal type on New-AzRoleAssignment and Set-AzRoleAssignment because current mapping was breaking certain scenarios</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-176">Az.Sql</span></span>
* <span data-ttu-id="f5912-177">已將 MaintenanceConfigurationId 新增至 ' >set-azsqldatabase '、' >set-azsqldatabase '、' New-AzSqlElasticPool ' 和 ' Set-AzSqlElasticPool '</span><span class="sxs-lookup"><span data-stu-id="f5912-177">Added MaintenanceConfigurationId to 'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' and 'Set-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f5912-178">修正了在提供 Predicateexpression 結構引數時，' Set-AzSqlServerAudit ' 中的回歸</span><span class="sxs-lookup"><span data-stu-id="f5912-178">Fixed regression in 'Set-AzSqlServerAudit' when PredicateExpression argument is provided</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-179">Az.Storage</span></span>
* <span data-ttu-id="f5912-180">建立/更新儲存體帳戶中支援的 RoutingPreference 設定</span><span class="sxs-lookup"><span data-stu-id="f5912-180">Supported RoutingPreference settings in create/update Storage account</span></span>
    - <span data-ttu-id="f5912-181">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-181">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f5912-182">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-182">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-183">已將 Azure 12.8.0 升級為</span><span class="sxs-lookup"><span data-stu-id="f5912-183">Upgraded Azure.Storage.Blobs to 12.8.0</span></span>
* <span data-ttu-id="f5912-184">已將12.6.0 升級為共用</span><span class="sxs-lookup"><span data-stu-id="f5912-184">Upgraded Azure.Storage.Files.Shares to 12.6.0</span></span>
* <span data-ttu-id="f5912-185">將 DataLake 升級至12.6。0</span><span class="sxs-lookup"><span data-stu-id="f5912-185">Upgraded Azure.Storage.Files.DataLake to 12.6.0</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-186">Az.Websites</span></span>
* <span data-ttu-id="f5912-187">已將匯入金鑰保存庫憑證的支援新增至 WebApp。</span><span class="sxs-lookup"><span data-stu-id="f5912-187">Added support for Importing a key vault certificate to WebApp.</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-188">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-189">@atul-ram，Update Set-AzEventHub.md ( # 13921) </span><span class="sxs-lookup"><span data-stu-id="f5912-189">@atul-ram, Update Set-AzEventHub.md (#13921)</span></span>
* <span data-ttu-id="f5912-190">Christoph Bergmeister [MVP] (@bergmeister) 、Set-AzDataLakeGen2AclRecursive.md-修正打字錯誤 (directiry > 目錄)  ( # 14082) </span><span class="sxs-lookup"><span data-stu-id="f5912-190">Christoph Bergmeister [MVP] (@bergmeister), Set-AzDataLakeGen2AclRecursive.md - Fix typo (directiry -> directory) (#14082)</span></span>
* <span data-ttu-id="f5912-191">Alexander Schmidt (@devdeer-alex) ，已修正 ( # 14009 的貢獻指導方針連結) </span><span class="sxs-lookup"><span data-stu-id="f5912-191">Alexander Schmidt (@devdeer-alex), Fixed broken link to contribution guidelines (#14009)</span></span>
* <span data-ttu-id="f5912-192">@JiangYuchun，Update Get-AzApplicationGatewayAuthenticationCertificate.md ( # 13972) </span><span class="sxs-lookup"><span data-stu-id="f5912-192">@JiangYuchun, Update Get-AzApplicationGatewayAuthenticationCertificate.md (#13972)</span></span>
* <span data-ttu-id="f5912-193">Sebastian Olsen (@Spacebjorn) ，已更正的範例命令 ( # 13901) </span><span class="sxs-lookup"><span data-stu-id="f5912-193">Sebastian Olsen (@Spacebjorn), Corrected example command (#13901)</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="f5912-194">5.4.0-2021 年1月</span><span class="sxs-lookup"><span data-stu-id="f5912-194">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-195">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-195">Az.Accounts</span></span>
* <span data-ttu-id="f5912-196">在 debug 訊息上顯示正確的用戶端要求識別碼 [#13745]</span><span class="sxs-lookup"><span data-stu-id="f5912-196">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="f5912-197">已新增常見的 Azure PowerShell 例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="f5912-197">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="f5912-198">支援的儲存體 API 2019-06-01</span><span class="sxs-lookup"><span data-stu-id="f5912-198">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-199">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-199">Az.Automation</span></span>
* <span data-ttu-id="f5912-200">修正未針對更新管理排程填入描述的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-200">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="f5912-201">Az. CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f5912-201">Az.CosmosDB</span></span>
* <span data-ttu-id="f5912-202">' Az. CosmosDB ' 模組正式推出</span><span class="sxs-lookup"><span data-stu-id="f5912-202">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="f5912-203">限制 New-AzCosmosDBAccount Cmdlet，以對現有的資料庫帳戶進行更新呼叫。</span><span class="sxs-lookup"><span data-stu-id="f5912-203">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="f5912-204">SqlContainer 中的 AnalyticalStorageTTL 簡介。</span><span class="sxs-lookup"><span data-stu-id="f5912-204">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-205">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-205">Az.IotHub</span></span>
* <span data-ttu-id="f5912-206">修正關於產生 SAS 權杖的回歸</span><span class="sxs-lookup"><span data-stu-id="f5912-206">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-207">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-208">已修正秘密管理模組中的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-208">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-209">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-210">修正了「AzLogicAppTriggerHistory」和「AzLogicAppRunAction」只會在第一頁結果中取得 [#9141] 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-210">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-211">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-211">Az.Monitor</span></span>
* <span data-ttu-id="f5912-212">已新增資料收集規則的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-212">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="f5912-213">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-213">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="f5912-214">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-214">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="f5912-215">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-215">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="f5912-216">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-216">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="f5912-217">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-217">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="f5912-218">已新增資料收集規則關聯的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-218">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="f5912-219">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="f5912-219">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="f5912-220">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="f5912-220">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="f5912-221">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="f5912-221">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-222">Az.Network</span></span>
* <span data-ttu-id="f5912-223">已新增 VpnGatewayNATRule CRUD 的新 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-223">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="f5912-224">' AzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-224">'New-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="f5912-225">' AzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-225">'Update-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="f5912-226">' AzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-226">'Get-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="f5912-227">' AzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="f5912-227">'Remove-AzVpnGatewayNatRule'</span></span>  
* <span data-ttu-id="f5912-228">已更新 Cmdlet，以在 VpnGateway 資源上設定 NATRule，並將其與 VpnSiteLinkConnection 資源建立關聯。</span><span class="sxs-lookup"><span data-stu-id="f5912-228">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="f5912-229">' AzVpnGateway '</span><span class="sxs-lookup"><span data-stu-id="f5912-229">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="f5912-230">' AzVpnGateway '</span><span class="sxs-lookup"><span data-stu-id="f5912-230">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="f5912-231">' AzVpnSiteLinkConnection '</span><span class="sxs-lookup"><span data-stu-id="f5912-231">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="f5912-232">已更新 Cmdlet，可讓您在虛擬網路閘道連線上設定 ConnectionMode。</span><span class="sxs-lookup"><span data-stu-id="f5912-232">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f5912-233">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-233">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f5912-234">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-234">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f5912-235">已更新 ' AzFirewallPolicyApplicationRule ' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-235">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="f5912-236">已新增參數 TargetUrl</span><span class="sxs-lookup"><span data-stu-id="f5912-236">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="f5912-237">已新增參數 TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="f5912-237">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="f5912-238">已新增 Azure 防火牆 Premium 功能的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-238">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="f5912-239">' AzFirewallPolicyIntrusionDetection '</span><span class="sxs-lookup"><span data-stu-id="f5912-239">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="f5912-240">' AzFirewallPolicyIntrusionDetectionBypassTraffic '</span><span class="sxs-lookup"><span data-stu-id="f5912-240">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="f5912-241">' AzFirewallPolicyIntrusionDetectionSignatureOverride '</span><span class="sxs-lookup"><span data-stu-id="f5912-241">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="f5912-242">已更新 New-AzFirewallPolicy Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-242">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="f5912-243">已新增參數-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f5912-243">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="f5912-244">已新增參數-身分識別</span><span class="sxs-lookup"><span data-stu-id="f5912-244">Added parameter -Identity</span></span>
    - <span data-ttu-id="f5912-245">已新增參數-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f5912-245">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="f5912-246">已新增參數-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="f5912-246">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="f5912-247">已新增參數-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="f5912-247">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="f5912-248">已新增參數-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="f5912-248">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="f5912-249">已新增新的 Cmdlet，以提取虛擬網路閘道連線的 IKE 安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="f5912-249">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f5912-250">' AzVirtualNetworkGatewayConnectionIkeSa '</span><span class="sxs-lookup"><span data-stu-id="f5912-250">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="f5912-251">為 p2sVpnGateway 新增了多個驗證支援</span><span class="sxs-lookup"><span data-stu-id="f5912-251">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="f5912-252">已更新 New-AzVpnServerConfiguration 和 Update-AzVpnServerConfiguration，以允許設定多個驗證參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-252">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="f5912-253">已更新 ' AzVpnGateway ' 和 ' AzP2sVpnGateway ' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-253">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="f5912-254">已新增參數 EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="f5912-254">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-255">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-256">已新增跨區域還原功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-256">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="f5912-257">當目標專案為可用性群組時，封鎖取得工作負載設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-257">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-258">Az.Resources</span></span>
* <span data-ttu-id="f5912-259">在新的 Az \* 部署 Cmdlet 中新增-QueryString 參數的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-259">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-260">Az.Sql</span></span>
* <span data-ttu-id="f5912-261">已將 ' AzSqlInstanceDatabaseLogReplay ' Cmdlet 設為同步，已新增-AsJob 旗標</span><span class="sxs-lookup"><span data-stu-id="f5912-261">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-262">Az.Storage</span></span>
* <span data-ttu-id="f5912-263">修正當清單 blob 與-IncludeVersion 時，ContinuationToken 絕不會是 null</span><span class="sxs-lookup"><span data-stu-id="f5912-263">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="f5912-264">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f5912-264">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-265">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-265">Az.Websites</span></span>
* <span data-ttu-id="f5912-266">已新增 App Service 受控憑證的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-266">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="f5912-267">' AzWebAppCertificate '</span><span class="sxs-lookup"><span data-stu-id="f5912-267">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="f5912-268">' AzWebAppCertificate '</span><span class="sxs-lookup"><span data-stu-id="f5912-268">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="f5912-269">已修正導致 Docker 密碼從 ' Set-azwebapp ' 和 ' Set-azwebappslot ' 中的 appsettings 中移除的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-269">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-270">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-270">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-271">Ivan Akcheurov (@ivanakcheurov) ，Update Set-AzSecurityWorkspaceSetting.md ( # 13877) </span><span class="sxs-lookup"><span data-stu-id="f5912-271">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="f5912-272">@javiermarasco，更新範例 ( # 13837) </span><span class="sxs-lookup"><span data-stu-id="f5912-272">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="f5912-273">@jhaprakash26，Update Set-AzVirtualNetwork.md ( # 13857) </span><span class="sxs-lookup"><span data-stu-id="f5912-273">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="f5912-274">Michael Holmes (@MichaelHolmesWP) 、Update New-AzStorageTableStoredAccessPolicy.md ( # 13871) </span><span class="sxs-lookup"><span data-stu-id="f5912-274">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="f5912-275">Michael James (@mikejwhat) ，可讓 Get-AzLogicAppTriggerHistory 和 Get-AzLogicAppRunAction 傳回超過30個結果 ( # 13846) </span><span class="sxs-lookup"><span data-stu-id="f5912-275">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="f5912-276">@Willem-J-an，修正導致 Docker 密碼從 appsettings 中的 Set-azwebapp (位置)  ( # 13866 中移除的 bug) </span><span class="sxs-lookup"><span data-stu-id="f5912-276">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="f5912-277">5.3.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f5912-277">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-278">Az.Accounts</span></span>
* <span data-ttu-id="f5912-279">已修正 Windows PowerShell 中不會遵守 Http Proxy 的問題 [#13647]</span><span class="sxs-lookup"><span data-stu-id="f5912-279">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="f5912-280">已改善所產生模組中長時間執行作業的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="f5912-280">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-281">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-281">Az.Automation</span></span>
* <span data-ttu-id="f5912-282">已修正 'Start-AzAutomationRunbook' 參數無法將 PSObject 所包裝的字串轉換為 JSON 字串的問題 [#13240]</span><span class="sxs-lookup"><span data-stu-id="f5912-282">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="f5912-283">已修正 New-AzAutomationUpdateManagementAzureQuery Cmdlet 的 Location 完成碼</span><span class="sxs-lookup"><span data-stu-id="f5912-283">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-284">Az.Compute</span></span>
* <span data-ttu-id="f5912-285">已將新參數集 'VMParameterSet' 中的新參數 'VM' 新增至 'Get-AzVMDscExtensionStatus' 和 'Get-AzVMDscExtension' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-285">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="f5912-286">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="f5912-286">Az.Databricks</span></span>
* <span data-ttu-id="f5912-287">已修正可能導致 'New-AzDatabricksVNetPeering' 在完全佈建之前就傳回的問題 (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="f5912-287">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-288">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-288">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-289">已修正 SupportsShouldProcess 問題的 'Invoke-AzDataFactoryV2Pipeline' 命令</span><span class="sxs-lookup"><span data-stu-id="f5912-289">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f5912-290">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f5912-290">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f5912-291">已將 StartVMOnConnect 屬性新增至 hostpool。</span><span class="sxs-lookup"><span data-stu-id="f5912-291">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-292">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-292">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-293">已新增屬性：AzureHDInsightHostInfo 類別中的 Fqdn 和 EffectiveDiskEncryptionKeyUrl。</span><span class="sxs-lookup"><span data-stu-id="f5912-293">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-294">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-295">已將新的參數 '-AsPlainText' 新增至 'Get-AzKeyVaultSecret'，以直接以純文字傳回祕密 [#13630]</span><span class="sxs-lookup"><span data-stu-id="f5912-295">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="f5912-296">已支援從受管理的 HSM 完整備份中選擇性地還原金鑰 [#13526]</span><span class="sxs-lookup"><span data-stu-id="f5912-296">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="f5912-297">已修正一些小問題 [#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="f5912-297">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="f5912-298">已在 SecretManagement 模組中新增遺失的 'Get-Secret' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="f5912-298">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="f5912-299">已修正可能導致不使用預設存取原則來建立保存庫的問題 [#13687]</span><span class="sxs-lookup"><span data-stu-id="f5912-299">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="f5912-300">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="f5912-300">Az.Kusto</span></span>
* <span data-ttu-id="f5912-301">已將 API 版本更新為 2020-09-18。</span><span class="sxs-lookup"><span data-stu-id="f5912-301">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-302">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-302">Az.Network</span></span>
* <span data-ttu-id="f5912-303">已修正在 ExpressRouteCircuit 案例中移除對等互連和連線 Cmdlet 時所發生的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-303">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="f5912-304">'Remove-AzExpressRouteCircuitPeeringConfig' 和 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-304">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-305">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-305">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-306">已針對 Get-AzPolicyState 新增可傳回編頁結果的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-306">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-307">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-307">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-308">已啟用 SQL 的 softdelete 功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-308">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="f5912-309">已修正 SQL AG 還原並移除容器名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="f5912-309">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="f5912-310">已變更 Azure 檔案儲存體備份項目的容器名稱格式。</span><span class="sxs-lookup"><span data-stu-id="f5912-310">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="f5912-311">已新增復原服務保存庫的 CMK 功能支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-311">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-312">Az.Resources</span></span>
* <span data-ttu-id="f5912-313">已修正 'New-AzureManagedApplication' 和 'Set-AzureManagedApplication' 中的 NullRef 例外狀況問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-313">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="f5912-314">已將 Azure Resource Manager SDK 更新為使用最新的 DeploymentScripts 正式發行 API 版本：2020-10-01。</span><span class="sxs-lookup"><span data-stu-id="f5912-314">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-315">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-316">已修正 'Add-AzServiceFabricNodeType'。</span><span class="sxs-lookup"><span data-stu-id="f5912-316">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="f5912-317">已在建立虛擬機器擴展集之前，將節點類型新增至 Service Fabric 叢集。</span><span class="sxs-lookup"><span data-stu-id="f5912-317">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-318">Az.Sql</span></span>
* <span data-ttu-id="f5912-319">已修正 'InstanceFailoverGroup' 命令的參數描述。</span><span class="sxs-lookup"><span data-stu-id="f5912-319">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="f5912-320">已更新用來從 SQL 資料分類命令的識別碼中擷取 schemaName、tableName 和 columnName 的邏輯。</span><span class="sxs-lookup"><span data-stu-id="f5912-320">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="f5912-321">已修正 'Get-AzSqlDatabaseImportExportStatus' 中的 Status 和 StatusMessage 欄位以符合文件</span><span class="sxs-lookup"><span data-stu-id="f5912-321">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="f5912-322">已新增 Microsoft 支援作業 (DevOps) 稽核 Cmdlet：Get-AzSqlServerMSSupportAudit、Set-AzSqlServerMSSupportAudit、Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-322">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-323">Az.Storage</span></span>
* <span data-ttu-id="f5912-324">已支援儲存體帳戶的建立/更新/取得/列出 EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f5912-324">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="f5912-325">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-325">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="f5912-326">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-326">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="f5912-327">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-327">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="f5912-328">已支援使用 [加密範圍] 設定來建立容器和上傳 Blob</span><span class="sxs-lookup"><span data-stu-id="f5912-328">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="f5912-329">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-329">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="f5912-330">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-330">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="f5912-331">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-331">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-332">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-332">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-333">Andreas Wolter (@AndreasWolter)，移除行銷語言，提供更好的篩選範例 (#13671)</span><span class="sxs-lookup"><span data-stu-id="f5912-333">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="f5912-334">Tidjani Belmansour (@BelRarr)，更新 Get-AzBillingInvoice.md (#13634)</span><span class="sxs-lookup"><span data-stu-id="f5912-334">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="f5912-335">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="f5912-335">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="f5912-336">修正拼字錯誤 (#13677)</span><span class="sxs-lookup"><span data-stu-id="f5912-336">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="f5912-337">更新 PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="f5912-337">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="f5912-338">@kilobyte97，「remove Cmdlet」的錯誤修正以刪除設定 (#13655)</span><span class="sxs-lookup"><span data-stu-id="f5912-338">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="f5912-339">@kongou-ae，更新 Set-AzFirewall.md (#13727)</span><span class="sxs-lookup"><span data-stu-id="f5912-339">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="f5912-340">@MasterKuat，修正文件中標題和程式碼之間的交換 (#13666)</span><span class="sxs-lookup"><span data-stu-id="f5912-340">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="f5912-341">NickT (@nukeulis)，更新 Set-AzContext.md (#13702)</span><span class="sxs-lookup"><span data-stu-id="f5912-341">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="f5912-342">@PaulHCode，更新 Start-AzJitNetworkAccessPolicy.md - 修正範例以顯示所示範的適當 Cmdlet (#13713)</span><span class="sxs-lookup"><span data-stu-id="f5912-342">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="f5912-343">Ryan Borstelmann (@ryanborMSFT)，移除了訂用帳戶識別碼 (#13715)</span><span class="sxs-lookup"><span data-stu-id="f5912-343">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="f5912-344">Shashikant Shakya (@shshakya)，更新 Set-AzSqlDatabase.md (#13674)</span><span class="sxs-lookup"><span data-stu-id="f5912-344">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="f5912-345">Sebastian Olsen (@Spacebjorn)，更新 Get-AzRecoveryServicesBackupItem.md (#13719)</span><span class="sxs-lookup"><span data-stu-id="f5912-345">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="f5912-346">5.2.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f5912-346">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-347">Az.Accounts</span></span>
* <span data-ttu-id="f5912-348">如果無法從基礎程式庫取得，則會受控以剖析原始權杖中的 ExpiresOn 時間</span><span class="sxs-lookup"><span data-stu-id="f5912-348">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="f5912-349">已改善互動式驗證無法使用時的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-349">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-350">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-350">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-351">[重大變更] 根據預設，'New-AzApiManagementProduct' 沒有訂用帳戶限制。</span><span class="sxs-lookup"><span data-stu-id="f5912-351">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-352">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-352">Az.Compute</span></span>
* <span data-ttu-id="f5912-353">已編輯 Get-AzVm，以在檢查節流之前，先依據 '-Name' 進行篩選，因為資源太多。</span><span class="sxs-lookup"><span data-stu-id="f5912-353">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="f5912-354">新的 Cmdlet 'Start-AzVmssRollingExtensionUpgrade'。</span><span class="sxs-lookup"><span data-stu-id="f5912-354">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5912-355">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5912-355">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5912-356">支援 'Get-AzContainerRegistryUsage' 的管線輸入參數 'Name' 與管線輸入中的值 [#13605]</span><span class="sxs-lookup"><span data-stu-id="f5912-356">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="f5912-357">改善 'Connect-AzContainerRegistry' 的例外狀況</span><span class="sxs-lookup"><span data-stu-id="f5912-357">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-358">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-358">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-359">已將 ADF .Net SDK 版本更新為 4.13.0</span><span class="sxs-lookup"><span data-stu-id="f5912-359">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5912-360">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5912-360">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5912-361">已新增客戶管理金鑰的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-361">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-362">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-362">Az.IotHub</span></span>
* <span data-ttu-id="f5912-363">已修正 SAS 權杖的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-363">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-364">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-364">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-365">在設定金鑰保存庫存取原則時，支援 'all' 做為選項</span><span class="sxs-lookup"><span data-stu-id="f5912-365">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="f5912-366">支援 SecretManagement 模組的新版本 [#13366]</span><span class="sxs-lookup"><span data-stu-id="f5912-366">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="f5912-367">支援 SecretManagementModule 中 'SecretValue' 的 ByteArray、String、PSCredential 和 Hashtable [#12190]</span><span class="sxs-lookup"><span data-stu-id="f5912-367">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="f5912-368">[重大變更] 重新設計與受控 HSM 相關 Cmdlet 的 API 介面。</span><span class="sxs-lookup"><span data-stu-id="f5912-368">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-369">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-369">Az.Monitor</span></span>
* <span data-ttu-id="f5912-370">已將 'New-AzAutoscaleProfile' 的參數 'Rule' 變更為接受空白清單。</span><span class="sxs-lookup"><span data-stu-id="f5912-370">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="f5912-371">[#12903]</span><span class="sxs-lookup"><span data-stu-id="f5912-371">[#12903]</span></span>
* <span data-ttu-id="f5912-372">已新增新的 Cmdlet，以支援建立更有彈性的診斷設定：</span><span class="sxs-lookup"><span data-stu-id="f5912-372">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="f5912-373">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="f5912-373">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="f5912-374">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="f5912-374">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="f5912-375">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="f5912-375">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-376">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-376">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-377">將說明文字和參數集名稱變更為 'Restore-AzRecoveryServicesBackupItem' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-377">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-378">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-378">Az.Resources</span></span>
* <span data-ttu-id="f5912-379">已將 '-Tag' 參數支援新增至 'Set-AzTemplateSpec' 和 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="f5912-379">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="f5912-380">已將標籤顯示支援新增至範本規格的預設格式器</span><span class="sxs-lookup"><span data-stu-id="f5912-380">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-381">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-381">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-382">已將範例新增至具有 SettingsSectionDescription param 的 'Set-AzServiceFabricSetting'</span><span class="sxs-lookup"><span data-stu-id="f5912-382">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="f5912-383">已將應用程式相關的 Cmdlet 更新為呼叫支援僅適用於 ARM 部署的資源</span><span class="sxs-lookup"><span data-stu-id="f5912-383">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="f5912-384">標示為已淘汰的叢集憑證 Cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 和 'Remove-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-384">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-385">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-385">Az.Sql</span></span>
* <span data-ttu-id="f5912-386">已將 SecondaryType 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="f5912-386">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="f5912-387">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-387">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="f5912-388">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-388">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="f5912-389">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="f5912-389">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="f5912-390">已將 HighAvailabilityReplicaCount 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="f5912-390">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="f5912-391">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-391">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="f5912-392">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-392">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="f5912-393">使 ReadReplicaCount 成為下列內容中的 HighAvailabilityReplicaCount 別名：</span><span class="sxs-lookup"><span data-stu-id="f5912-393">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="f5912-394">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-394">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="f5912-395">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-395">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-396">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-396">Az.Storage</span></span>
* <span data-ttu-id="f5912-397">支援上傳 Azure 檔案大小上限至 4 TiB</span><span class="sxs-lookup"><span data-stu-id="f5912-397">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="f5912-398">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-398">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="f5912-399">已將 Azure.Storage.Blobs 升級至 12.7.0</span><span class="sxs-lookup"><span data-stu-id="f5912-399">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="f5912-400">已將 Azure.Storage.Files.Shares 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="f5912-400">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="f5912-401">已將 Azure.Storage.Files.DataLake 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="f5912-401">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-402">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-402">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-403">已新增具有下載原則和本機快取模式的同步階層處理原則功能</span><span class="sxs-lookup"><span data-stu-id="f5912-403">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-404">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-404">Az.Websites</span></span>
* <span data-ttu-id="f5912-405">防止重複存取限制規則</span><span class="sxs-lookup"><span data-stu-id="f5912-405">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-406">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-406">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-407">Andrew Dawson (@dawsonar802)，升級 Get-AzKeyVaultCertificate.md - 取得憑證並將其另存為 pfx 區段，以使用 PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="f5912-407">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="f5912-408">@iviark，醫療保健 APIs Powershell BYOK 更新 (#13518)</span><span class="sxs-lookup"><span data-stu-id="f5912-408">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="f5912-409">John Duckmanton (@johnduckmanton)，修正 TagPatchOperation 的拼寫 (#13508)</span><span class="sxs-lookup"><span data-stu-id="f5912-409">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="f5912-410">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="f5912-410">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="f5912-411">Get-AzLogicAppRunHistory Help Tidy (#13513)</span><span class="sxs-lookup"><span data-stu-id="f5912-411">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="f5912-412">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="f5912-412">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="f5912-413">更新 Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="f5912-413">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="f5912-414">更新 New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="f5912-414">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="f5912-415">@SteppingRazor，New-AzApiManagementProduct：將 SubscriptionsLimit 參數的預設值變更為 None (#13457)</span><span class="sxs-lookup"><span data-stu-id="f5912-415">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="f5912-416">Steve Burkett (@SteveBurkettNZ)，修正範例中 WorkspaceResourceId 參數的打字錯誤 (#13589)</span><span class="sxs-lookup"><span data-stu-id="f5912-416">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="f5912-417">5.1.0 - 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f5912-417">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-418">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-418">Az.Accounts</span></span>
* <span data-ttu-id="f5912-419">已修正使用 ''Connect-AzAccount -DeviceCode' 時，可能不會遵守 TenantId 的問題 [#13477]</span><span class="sxs-lookup"><span data-stu-id="f5912-419">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="f5912-420">已新增 Cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="f5912-420">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="f5912-421">已修正無法存取使用者設定檔路徑時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-421">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="f5912-422">已修正 Connect-AzAccount 期間發生 Write-Object 錯誤的問題 [#13419]</span><span class="sxs-lookup"><span data-stu-id="f5912-422">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="f5912-423">已將參數 'ContainerRegistryEndpointSuffix' 新增至：'Add-AzEnvironment'、'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="f5912-423">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="f5912-424">支援點擊 <kbd>CTRL</kbd>+<kbd>C</kbd> 來中斷登入</span><span class="sxs-lookup"><span data-stu-id="f5912-424">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="f5912-425">已修正導致 'Connect-AzAccount -KeyVaultAccessToken' 無法運作的問題 [#13127]</span><span class="sxs-lookup"><span data-stu-id="f5912-425">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="f5912-426">已修正 'Invoke-AzRestMethod' 中 Null 參考和方法不區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-426">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-427">Az.Aks</span></span>
* <span data-ttu-id="f5912-428">已修正使用者無法使用服務主體建立新 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-428">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="f5912-429">[#13012]</span><span class="sxs-lookup"><span data-stu-id="f5912-429">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="f5912-430">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-430">Az.AppConfiguration</span></span>
* <span data-ttu-id="f5912-431">'Az.AppConfiguration' 模組的正式推出</span><span class="sxs-lookup"><span data-stu-id="f5912-431">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-432">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-432">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-433">已改善 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 命令的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-433">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-434">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-435">已將 ADLS 資料平面 SDK 更新為 1.2.4-alpha。</span><span class="sxs-lookup"><span data-stu-id="f5912-435">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="f5912-436">變更： https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="f5912-436">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f5912-437">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f5912-437">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f5912-438">已新增 MSIX Package Cmdlet 和更新應用程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-438">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-439">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-439">Az.EventHub</span></span>
* <span data-ttu-id="f5912-440">已修正 EventHub 叢集沒有標記時的叢集命令</span><span class="sxs-lookup"><span data-stu-id="f5912-440">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="f5912-441">已更新 AzEventHubGeoDRConfiguration 的 PartnerNamespace 命令解說文字</span><span class="sxs-lookup"><span data-stu-id="f5912-441">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-442">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-442">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-443">已將 'ResourceProviderConnection' 和 'PrivateLink' 參數新增至 'New-AzHDInsightCluster' Cmdlet 以支援轉送輸出和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="f5912-443">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="f5912-444">已將 'AmbariDatabase' 參數新增至 'New-AzHDInsightCluster' Cmdlet，以支援自訂 Ambari 資料庫功能</span><span class="sxs-lookup"><span data-stu-id="f5912-444">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="f5912-445">將接受值 'AmbariDatabase' 新增至 'Add-AzHDInsightMetastore' Cmdlet 的 'MetastoreType' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-445">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-446">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-446">Az.IotHub</span></span>
* <span data-ttu-id="f5912-447">允許在 IoT 中樞建立 Cmdlet 中使用標記。</span><span class="sxs-lookup"><span data-stu-id="f5912-447">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-448">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-449">支援更新金鑰保存庫標記</span><span class="sxs-lookup"><span data-stu-id="f5912-449">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-450">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-450">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-451">已修正 Get-AzLogicAppRunHistory 只會取得結果第一頁的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-451">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-452">Az.Network</span></span>
* <span data-ttu-id="f5912-453">已更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-453">Updated below cmdlet</span></span> 
    - <span data-ttu-id="f5912-454">'New-AzLoadBalancerFrontendIpConfigCommand'、'Set-AzLoadBalancerFrontendIpConfigCommand'、'Add-AzLoadBalancerFrontendIpConfigCommand'：</span><span class="sxs-lookup"><span data-stu-id="f5912-454">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="f5912-455">已新增 PublicIpAddressPrefix 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-455">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="f5912-456">已新增 PublicIpAddressPrefixId 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-456">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="f5912-457">已將新屬性新增至下列 Cmdlet，以允許進行全域負載平衡</span><span class="sxs-lookup"><span data-stu-id="f5912-457">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="f5912-458">'New-AzLoadBalancer'：</span><span class="sxs-lookup"><span data-stu-id="f5912-458">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="f5912-459">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-459">Added Sku Tier property</span></span>
    - <span data-ttu-id="f5912-460">'New-AzPuplicIpAddress'：</span><span class="sxs-lookup"><span data-stu-id="f5912-460">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="f5912-461">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-461">Added Sku Tier property</span></span>
    - <span data-ttu-id="f5912-462">'New-AzPublicIpPrefix'：</span><span class="sxs-lookup"><span data-stu-id="f5912-462">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="f5912-463">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-463">Added Sku Tier property</span></span>
    - <span data-ttu-id="f5912-464">'New-AzLoadBalancerBackendAddressConfig'：</span><span class="sxs-lookup"><span data-stu-id="f5912-464">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="f5912-465">已新增 LoadBalancerFrontendIPConfigurationId 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-465">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="f5912-466">已更新規劃來取代下列 Cmdlet 的警告   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-466">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="f5912-467">已新增規劃來取代下列 Cmdlet 的 'RouteTable' 引數警告   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="f5912-467">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f5912-468">已將 '-MinScaleUnits' 和 '-MaxScaleUnits' 引數設為 'Set-AzExpressRouteGateway' 中的選擇性項目</span><span class="sxs-lookup"><span data-stu-id="f5912-468">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="f5912-469">已新增 Cmdlet 來支援應用程式閘道的相互驗證和 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="f5912-469">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="f5912-470">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-470">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="f5912-471">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-471">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="f5912-472">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-472">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="f5912-473">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-473">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="f5912-474">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-474">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="f5912-475">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-475">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="f5912-476">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-476">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="f5912-477">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-477">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="f5912-478">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-478">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="f5912-479">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-479">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="f5912-480">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-480">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="f5912-481">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-481">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="f5912-482">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-482">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="f5912-483">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-483">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="f5912-484">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-484">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="f5912-485">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-485">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="f5912-486">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-486">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-487">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-487">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-488">指定原則 BackupTime 的格式為 UTC。</span><span class="sxs-lookup"><span data-stu-id="f5912-488">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="f5912-489">修改 Get-AzRecoveryServicesBackupJobDetails Cmdlet 中的中斷性變更警告。</span><span class="sxs-lookup"><span data-stu-id="f5912-489">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="f5912-490">更新 Set-AzRecoveryServicesBackupProtectionPolicy Cmdlet 的範例指令碼解說文字。</span><span class="sxs-lookup"><span data-stu-id="f5912-490">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-491">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-491">Az.Resources</span></span>
* <span data-ttu-id="f5912-492">已修正 What-If 會顯示兩個大小寫不同的資源群組範圍的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-492">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="f5912-493">已將 'Export-AzResourceGroup' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-493">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="f5912-494">已將文化特性資訊新增至 parse 方法</span><span class="sxs-lookup"><span data-stu-id="f5912-494">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-495">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-495">Az.Sql</span></span>
* <span data-ttu-id="f5912-496">已修正 Set-AzSqlDatabaseAudit 不支援超大規模資料庫資料庫和資料庫版本無法判斷的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-496">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="f5912-497">已將 MaintenanceConfigurationId 新增至 New-AzSqlInstance' 和 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="f5912-497">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="f5912-498">已修正 GetAzureSqlDatabaseReplicationLink.cs 中的錯誤 (bug)：PartnerServerName 參數會以值進行檢查，而非索引鍵</span><span class="sxs-lookup"><span data-stu-id="f5912-498">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-499">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-499">Az.Websites</span></span>
* <span data-ttu-id="f5912-500">新增最新存取限制功能的支援：ServiceTag、multi-ip 和 http-headers</span><span class="sxs-lookup"><span data-stu-id="f5912-500">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-501">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-501">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-502">John Q. Martin (@johnmart82)，新增防火牆必要條件資訊 (#13385)</span><span class="sxs-lookup"><span data-stu-id="f5912-502">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="f5912-503">Manikandan Duraisamy (@madurais-msft)，修正 PublicSubnetName 引數 (#13417)</span><span class="sxs-lookup"><span data-stu-id="f5912-503">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="f5912-504">@mahortas，更新 -HostNames 參數值 (#13349)</span><span class="sxs-lookup"><span data-stu-id="f5912-504">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="f5912-505">@MariachiForHire，新增支援的 TrafficAnalyticsInterval 值 (#13304)</span><span class="sxs-lookup"><span data-stu-id="f5912-505">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="f5912-506">Michael James (@mikejwhat)，允許 Get-AzLogicAppRunHistory 傳回超過 30 個項目 (#13393)</span><span class="sxs-lookup"><span data-stu-id="f5912-506">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="f5912-507">Shashikant Shakya (@shshakya)，更新 Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="f5912-507">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="f5912-508">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f5912-508">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-509">Az.Accounts</span></span>
* <span data-ttu-id="f5912-510">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="f5912-510">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="f5912-511">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="f5912-511">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-512">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-512">Az.Aks</span></span>
* <span data-ttu-id="f5912-513">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="f5912-513">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="f5912-514">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="f5912-514">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="f5912-515">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="f5912-515">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="f5912-516">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="f5912-516">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f5912-517">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5912-517">Az.Billing</span></span>
* <span data-ttu-id="f5912-518">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-518">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="f5912-519">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-519">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="f5912-520">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-520">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="f5912-521">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="f5912-521">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="f5912-522">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="f5912-522">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-523">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-523">Az.Cdn</span></span>
* <span data-ttu-id="f5912-524">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="f5912-524">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-525">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-525">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-526">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="f5912-526">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-527">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-527">Az.Compute</span></span>
* <span data-ttu-id="f5912-528">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="f5912-528">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="f5912-529">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-529">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="f5912-530">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="f5912-530">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="f5912-531">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-531">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="f5912-532">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-532">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5912-533">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5912-533">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5912-534">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="f5912-534">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="f5912-535">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="f5912-535">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="f5912-536">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="f5912-536">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="f5912-537">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="f5912-537">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="f5912-538">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="f5912-538">Az.Databricks</span></span>
* <span data-ttu-id="f5912-539">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-539">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-540">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-540">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-541">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="f5912-541">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="f5912-542">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="f5912-542">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="f5912-543">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="f5912-543">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f5912-544">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f5912-544">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f5912-545">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="f5912-545">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="f5912-546">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="f5912-546">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="f5912-547">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="f5912-547">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="f5912-548">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="f5912-548">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5912-549">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5912-549">Az.Functions</span></span>
* <span data-ttu-id="f5912-550">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-550">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="f5912-551">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="f5912-551">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="f5912-552">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="f5912-552">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="f5912-553">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="f5912-553">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="f5912-554">[#12728]</span><span class="sxs-lookup"><span data-stu-id="f5912-554">[#12728]</span></span>
  - <span data-ttu-id="f5912-555">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-555">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="f5912-556">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="f5912-556">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="f5912-557">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="f5912-557">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="f5912-558">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="f5912-558">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-559">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-559">Az.HDInsight</span></span>
 * <span data-ttu-id="f5912-560">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-560">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="f5912-561">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="f5912-561">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="f5912-562">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f5912-562">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="f5912-563">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="f5912-563">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="f5912-564">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="f5912-564">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="f5912-565">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="f5912-565">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="f5912-566">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="f5912-566">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="f5912-567">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="f5912-567">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="f5912-568">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="f5912-568">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="f5912-569">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-569">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="f5912-570">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="f5912-570">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="f5912-571">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f5912-571">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="f5912-572">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="f5912-572">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="f5912-573">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="f5912-573">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="f5912-574">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="f5912-574">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="f5912-575">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-575">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="f5912-576">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="f5912-576">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="f5912-577">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-577">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="f5912-578">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="f5912-578">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="f5912-579">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="f5912-579">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-580">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-581">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-581">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="f5912-582">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="f5912-582">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="f5912-583">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="f5912-583">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="f5912-584">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-584">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="f5912-585">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="f5912-585">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f5912-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f5912-586">Az.ManagedServices</span></span>
* <span data-ttu-id="f5912-587">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="f5912-587">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-588">Az.Network</span></span>
* <span data-ttu-id="f5912-589">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="f5912-589">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="f5912-590">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-590">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="f5912-591">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="f5912-591">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="f5912-592">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="f5912-592">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="f5912-593">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-593">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="f5912-594">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="f5912-594">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="f5912-595">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="f5912-595">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="f5912-596">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="f5912-596">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="f5912-597">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="f5912-597">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="f5912-598">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="f5912-598">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="f5912-599">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="f5912-599">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="f5912-600">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-600">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="f5912-601">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="f5912-601">Added parameter '-Type'</span></span>
    - <span data-ttu-id="f5912-602">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="f5912-602">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="f5912-603">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="f5912-603">Added parameter '-Scope'</span></span>
* <span data-ttu-id="f5912-604">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-604">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-605">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-605">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-606">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="f5912-606">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="f5912-607">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-607">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-608">Az.Resources</span></span>
* <span data-ttu-id="f5912-609">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-609">Fixed parsing bug</span></span>
* <span data-ttu-id="f5912-610">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-610">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="f5912-611">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="f5912-611">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="f5912-612">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-612">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="f5912-613">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-613">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="f5912-614">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-614">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="f5912-615">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="f5912-615">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="f5912-616">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-616">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="f5912-617">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-617">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-618">Az.Sql</span></span>
* <span data-ttu-id="f5912-619">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="f5912-619">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="f5912-620">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="f5912-620">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="f5912-621">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-621">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="f5912-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-622">Az.Storage</span></span>
* <span data-ttu-id="f5912-623">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="f5912-623">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="f5912-624">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-624">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-625">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-625">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-626">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-626">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="f5912-627">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-627">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f5912-628">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="f5912-628">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="f5912-629">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-629">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="f5912-630">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-630">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="f5912-631">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="f5912-631">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="f5912-632">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="f5912-632">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="f5912-633">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="f5912-633">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="f5912-634">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-634">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="f5912-635">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-635">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="f5912-636">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="f5912-636">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="f5912-637">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="f5912-637">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="f5912-638">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="f5912-638">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="f5912-639">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="f5912-639">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="f5912-640">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="f5912-640">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="f5912-641">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-641">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="f5912-642">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-642">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="f5912-643">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="f5912-643">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="f5912-644">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-644">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="f5912-645">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-645">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="f5912-646">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="f5912-646">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="f5912-647">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-647">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-648">Az.Websites</span></span>
* <span data-ttu-id="f5912-649">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-649">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="f5912-650">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="f5912-650">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-651">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-651">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-652">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="f5912-652">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="f5912-653">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="f5912-653">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="f5912-654">(#13249)</span><span class="sxs-lookup"><span data-stu-id="f5912-654">(#13249)</span></span>
* <span data-ttu-id="f5912-655">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="f5912-655">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="f5912-656">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="f5912-656">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="f5912-657">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="f5912-657">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="f5912-658">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-658">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="f5912-659">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-659">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="f5912-660">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-660">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="f5912-661">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="f5912-661">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="f5912-662">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-662">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="f5912-663">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-663">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="f5912-664">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f5912-664">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-665">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-665">Az.Accounts</span></span>
* <span data-ttu-id="f5912-666">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="f5912-666">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-668">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-668">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="f5912-669">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-669">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-670">Az.Compute</span></span>
* <span data-ttu-id="f5912-671">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-671">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="f5912-672">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-672">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="f5912-673">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="f5912-673">Az.Databricks</span></span>
* <span data-ttu-id="f5912-674">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="f5912-674">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="f5912-675">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-675">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-676">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-677">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-677">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-678">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-678">Az.EventHub</span></span>
* <span data-ttu-id="f5912-679">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-679">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-680">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-680">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-681">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-681">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="f5912-682">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-682">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="f5912-683">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-683">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="f5912-684">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-684">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="f5912-685">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-685">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="f5912-686">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-686">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-687">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-687">Az.IotHub</span></span>
* <span data-ttu-id="f5912-688">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-688">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-689">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-689">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-690">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="f5912-690">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f5912-691">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f5912-691">Az.ManagedServices</span></span>
* <span data-ttu-id="f5912-692">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="f5912-692">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-693">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-693">Az.Monitor</span></span>
* <span data-ttu-id="f5912-694">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-694">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="f5912-695">[#12889]</span><span class="sxs-lookup"><span data-stu-id="f5912-695">[#12889]</span></span>
* <span data-ttu-id="f5912-696">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-696">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="f5912-697">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="f5912-697">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-698">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-698">Az.Network</span></span>
* <span data-ttu-id="f5912-699">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="f5912-699">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="f5912-700">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-700">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-702">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-702">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5912-703">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5912-703">Az.RedisCache</span></span>
* <span data-ttu-id="f5912-704">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="f5912-704">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-705">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-705">Az.Sql</span></span>
* <span data-ttu-id="f5912-706">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="f5912-706">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="f5912-707">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-707">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="f5912-708">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="f5912-708">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="f5912-709">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="f5912-709">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="f5912-710">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="f5912-710">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="f5912-711">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-711">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-712">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-712">Az.Storage</span></span>
* <span data-ttu-id="f5912-713">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-713">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="f5912-714">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-714">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="f5912-715">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-715">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="f5912-716">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="f5912-716">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="f5912-717">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-717">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="f5912-718">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="f5912-718">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="f5912-719">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-719">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="f5912-720">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5912-720">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="f5912-721">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-721">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="f5912-722">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-722">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="f5912-723">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-723">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-724">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-724">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-725">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-725">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f5912-726">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="f5912-726">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="f5912-727">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="f5912-727">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="f5912-728">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="f5912-728">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-729">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-729">Az.Accounts</span></span>
* <span data-ttu-id="f5912-730">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-730">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="f5912-731">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="f5912-731">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-732">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-732">Az.Aks</span></span>
* <span data-ttu-id="f5912-733">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="f5912-733">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="f5912-734">[#12372]</span><span class="sxs-lookup"><span data-stu-id="f5912-734">[#12372]</span></span>
* <span data-ttu-id="f5912-735">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-735">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="f5912-736">[#11239]</span><span class="sxs-lookup"><span data-stu-id="f5912-736">[#11239]</span></span>
* <span data-ttu-id="f5912-737">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="f5912-737">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="f5912-738">[#11239]</span><span class="sxs-lookup"><span data-stu-id="f5912-738">[#11239]</span></span>
* <span data-ttu-id="f5912-739">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="f5912-739">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="f5912-740">[#12371]</span><span class="sxs-lookup"><span data-stu-id="f5912-740">[#12371]</span></span>
* <span data-ttu-id="f5912-741">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="f5912-741">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-742">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-742">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-743">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="f5912-743">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-744">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-744">Az.Compute</span></span>
* <span data-ttu-id="f5912-745">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-745">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="f5912-746">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="f5912-746">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="f5912-747">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-747">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="f5912-748">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-748">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="f5912-749">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="f5912-749">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="f5912-750">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="f5912-750">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="f5912-751">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="f5912-751">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="f5912-752">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f5912-752">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="f5912-753">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="f5912-753">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="f5912-754">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="f5912-754">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-755">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-756">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="f5912-756">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-757">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-757">Az.EventHub</span></span>
* <span data-ttu-id="f5912-758">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="f5912-758">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="f5912-759">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-759">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5912-760">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5912-760">Az.Functions</span></span>
* <span data-ttu-id="f5912-761">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-761">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="f5912-762">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="f5912-762">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="f5912-763">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5912-763">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-764">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-765">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="f5912-765">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="f5912-766">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-766">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="f5912-767">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="f5912-767">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="f5912-768">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-768">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="f5912-769">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-769">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="f5912-770">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-770">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="f5912-771">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-771">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="f5912-772">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="f5912-772">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-773">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-773">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-774">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="f5912-774">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="f5912-775">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="f5912-775">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="f5912-776">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="f5912-776">Az.Kusto</span></span>
* <span data-ttu-id="f5912-777">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="f5912-777">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-778">Az.Network</span></span>
* <span data-ttu-id="f5912-779">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="f5912-779">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="f5912-780">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="f5912-780">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="f5912-781">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="f5912-781">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="f5912-782">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="f5912-782">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="f5912-783">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="f5912-783">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="f5912-784">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="f5912-784">Added subscription level parameter set</span></span>
    - <span data-ttu-id="f5912-785">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="f5912-785">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="f5912-786">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="f5912-786">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="f5912-787">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="f5912-787">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="f5912-788">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="f5912-788">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="f5912-789">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-789">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="f5912-790">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="f5912-790">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="f5912-791">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="f5912-791">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="f5912-792">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-792">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="f5912-793">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="f5912-793">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="f5912-794">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="f5912-794">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="f5912-795">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="f5912-795">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="f5912-796">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="f5912-796">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="f5912-797">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="f5912-797">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="f5912-798">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="f5912-798">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="f5912-799">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="f5912-799">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="f5912-800">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="f5912-800">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="f5912-801">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-801">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="f5912-802">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="f5912-802">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-804">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="f5912-804">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-805">Az.Resources</span></span>
* <span data-ttu-id="f5912-806">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="f5912-806">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="f5912-807">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-807">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="f5912-808">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="f5912-808">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="f5912-809">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="f5912-809">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-810">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-810">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-811">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-811">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="f5912-812">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-812">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="f5912-813">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-813">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="f5912-814">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-814">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="f5912-815">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-815">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="f5912-816">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-816">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="f5912-817">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-817">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="f5912-818">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="f5912-818">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="f5912-819">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="f5912-819">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="f5912-820">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="f5912-820">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="f5912-821">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="f5912-821">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="f5912-822">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-822">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="f5912-823">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="f5912-823">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="f5912-824">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-824">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="f5912-825">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="f5912-825">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="f5912-826">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="f5912-826">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-827">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-827">Az.Sql</span></span>
* <span data-ttu-id="f5912-828">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="f5912-828">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="f5912-829">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-829">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-830">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-830">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-831">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="f5912-831">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="f5912-832">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-832">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="f5912-833">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="f5912-833">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="f5912-834">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="f5912-834">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="f5912-835">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="f5912-835">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="f5912-836">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="f5912-836">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="f5912-837">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-837">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-838">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-838">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-839">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-839">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-840">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="f5912-840">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="f5912-841">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="f5912-841">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="f5912-842">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="f5912-842">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="f5912-843">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="f5912-843">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="f5912-844">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="f5912-844">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="f5912-845">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="f5912-845">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-846">Az.Storage</span></span>
* <span data-ttu-id="f5912-847">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="f5912-847">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="f5912-848">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="f5912-848">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="f5912-849">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-849">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-850">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-850">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="f5912-851">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="f5912-851">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="f5912-852">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="f5912-852">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="f5912-853">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="f5912-853">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="f5912-854">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-854">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="f5912-855">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-855">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="f5912-856">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-856">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="f5912-857">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-857">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="f5912-858">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-858">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="f5912-859">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-859">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="f5912-860">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="f5912-860">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="f5912-861">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="f5912-861">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="f5912-862">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="f5912-862">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="f5912-863">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="f5912-863">Thanks to our community contributors</span></span>
* <span data-ttu-id="f5912-864">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="f5912-864">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="f5912-865">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="f5912-865">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="f5912-866">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="f5912-866">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="f5912-867">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="f5912-867">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="f5912-868">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="f5912-868">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="f5912-869">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="f5912-869">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="f5912-870">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="f5912-870">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="f5912-871">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="f5912-871">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="f5912-872">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="f5912-872">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="f5912-873">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="f5912-873">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="f5912-874">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="f5912-874">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="f5912-875">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="f5912-875">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="f5912-876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-876">Az.Compute</span></span>
* <span data-ttu-id="f5912-877">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="f5912-877">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="f5912-878">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="f5912-878">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-879">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-879">Az.Accounts</span></span>
* <span data-ttu-id="f5912-880">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="f5912-880">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="f5912-881">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="f5912-881">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-882">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-882">Az.Automation</span></span>
* <span data-ttu-id="f5912-883">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="f5912-883">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-884">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-884">Az.Compute</span></span>
* <span data-ttu-id="f5912-885">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="f5912-885">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="f5912-886">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="f5912-886">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="f5912-887">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="f5912-887">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="f5912-888">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-888">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-889">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-890">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="f5912-890">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-891">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-891">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-892">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="f5912-892">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-893">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-894">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-894">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="f5912-895">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-895">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f5912-896">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f5912-896">Az.Maintenance</span></span>
* <span data-ttu-id="f5912-897">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-897">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="f5912-898">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-898">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f5912-899">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f5912-899">Az.ManagedServices</span></span>
* <span data-ttu-id="f5912-900">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="f5912-900">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-901">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-901">Az.Monitor</span></span>
* <span data-ttu-id="f5912-902">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="f5912-902">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="f5912-903">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-903">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-904">Az.Resources</span></span>
* <span data-ttu-id="f5912-905">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="f5912-905">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="f5912-906">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-906">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="f5912-907">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="f5912-907">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="f5912-908">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="f5912-908">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="f5912-909">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="f5912-909">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f5912-910">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="f5912-910">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="f5912-911">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="f5912-911">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="f5912-912">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-912">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5912-913">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5912-913">Az.SignalR</span></span>
* <span data-ttu-id="f5912-914">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-914">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="f5912-915">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-915">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-916">Az.Storage</span></span>
* <span data-ttu-id="f5912-917">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="f5912-917">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="f5912-918">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="f5912-918">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="f5912-919">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-919">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="f5912-920">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-920">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="f5912-921">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="f5912-921">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="f5912-922">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-922">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="f5912-923">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="f5912-923">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="f5912-924">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-924">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="f5912-925">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="f5912-925">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="f5912-926">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="f5912-926">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="f5912-927">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-927">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f5912-928">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-928">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f5912-929">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-929">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="f5912-930">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="f5912-930">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f5912-931">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-931">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="f5912-932">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="f5912-932">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-933">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-933">Az.Accounts</span></span>
* <span data-ttu-id="f5912-934">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="f5912-934">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="f5912-935">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="f5912-935">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="f5912-936">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-936">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="f5912-937">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-937">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="f5912-938">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="f5912-938">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-939">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-939">Az.Aks</span></span>
* <span data-ttu-id="f5912-940">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="f5912-940">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="f5912-941">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="f5912-941">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-942">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-942">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-943">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-943">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-944">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-944">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-945">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-945">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5912-946">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-946">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="f5912-947">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-947">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-948">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-948">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5912-949">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-949">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="f5912-950">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-950">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-951">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-951">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-952">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-952">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5912-953">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-953">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5912-954">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-954">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-956">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="f5912-956">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-957">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-958">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="f5912-958">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-959">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-959">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-960">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="f5912-960">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="f5912-961">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-961">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f5912-962">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-962">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f5912-963">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="f5912-963">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="f5912-964">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="f5912-964">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f5912-965">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-965">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f5912-966">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-966">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-967">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-967">Az.Network</span></span>
* <span data-ttu-id="f5912-968">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-968">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f5912-969">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-969">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="f5912-970">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="f5912-970">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="f5912-971">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-971">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-972">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-972">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-973">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="f5912-973">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="f5912-974">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f5912-974">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="f5912-975">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f5912-975">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-977">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="f5912-977">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-978">Az.Resources</span></span>
* <span data-ttu-id="f5912-979">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="f5912-979">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="f5912-980">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="f5912-980">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-981">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-981">Az.Sql</span></span>
* <span data-ttu-id="f5912-982">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-982">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f5912-983">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-983">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-984">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-984">Az.Storage</span></span>
* <span data-ttu-id="f5912-985">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-985">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="f5912-986">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="f5912-986">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="f5912-987">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="f5912-987">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="f5912-988">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-988">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="f5912-989">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="f5912-989">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="f5912-990">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="f5912-990">Supported get single file share usage</span></span>
    - <span data-ttu-id="f5912-991">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-991">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="f5912-992">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="f5912-992">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-993">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-993">Az.Accounts</span></span>
* <span data-ttu-id="f5912-994">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="f5912-994">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="f5912-995">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="f5912-995">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-996">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-996">Az.Aks</span></span>
* <span data-ttu-id="f5912-997">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="f5912-997">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-998">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-998">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5912-999">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="f5912-999">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-1000">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-1000">Az.Automation</span></span>
* <span data-ttu-id="f5912-1001">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1001">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1002">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1002">Az.Compute</span></span>
* <span data-ttu-id="f5912-1003">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="f5912-1003">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1004">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1004">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1005">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="f5912-1005">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5912-1006">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5912-1006">Az.EventGrid</span></span>
* <span data-ttu-id="f5912-1007">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f5912-1007">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="f5912-1008">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="f5912-1008">Added new features:</span></span>
    - <span data-ttu-id="f5912-1009">輸入對應</span><span class="sxs-lookup"><span data-stu-id="f5912-1009">Input mapping</span></span>
    - <span data-ttu-id="f5912-1010">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-1010">Event Delivery Schema</span></span>
    - <span data-ttu-id="f5912-1011">私人連結</span><span class="sxs-lookup"><span data-stu-id="f5912-1011">Private Link</span></span>
    - <span data-ttu-id="f5912-1012">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-1012">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="f5912-1013">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="f5912-1013">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="f5912-1014">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="f5912-1014">Azure Function As Destination</span></span>
    - <span data-ttu-id="f5912-1015">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="f5912-1015">WebHook Batching</span></span>
    - <span data-ttu-id="f5912-1016">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="f5912-1016">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="f5912-1017">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="f5912-1017">IpFiltering</span></span>
* <span data-ttu-id="f5912-1018">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1018">Updated cmdlets:</span></span>
    - <span data-ttu-id="f5912-1019">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="f5912-1019">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="f5912-1020">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="f5912-1020">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="f5912-1021">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="f5912-1021">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="f5912-1022">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="f5912-1022">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="f5912-1023">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1023">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="f5912-1024">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="f5912-1024">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f5912-1025">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="f5912-1025">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="f5912-1026">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="f5912-1026">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f5912-1027">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="f5912-1027">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-1028">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-1028">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-1029">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="f5912-1029">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="f5912-1030">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1030">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1031">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1031">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1032">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="f5912-1032">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1033">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1034">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="f5912-1034">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1035">Az.Network</span></span>
* <span data-ttu-id="f5912-1036">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="f5912-1036">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="f5912-1037">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1037">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="f5912-1038">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f5912-1038">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5912-1039">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f5912-1039">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5912-1040">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f5912-1040">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5912-1041">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f5912-1041">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5912-1042">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-1042">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="f5912-1043">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1043">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="f5912-1044">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f5912-1044">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5912-1045">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f5912-1045">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5912-1046">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f5912-1046">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5912-1047">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f5912-1047">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5912-1048">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="f5912-1048">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="f5912-1049">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-1049">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="f5912-1050">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1050">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f5912-1051">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1051">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f5912-1052">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1052">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1053">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1054">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="f5912-1054">Removed project reference to Authentication</span></span>
* <span data-ttu-id="f5912-1055">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="f5912-1055">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="f5912-1056">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1056">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1057">Az.Resources</span></span>
* <span data-ttu-id="f5912-1058">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-1058">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="f5912-1059">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1059">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1060">Az.Sql</span></span>
* <span data-ttu-id="f5912-1061">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1061">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="f5912-1062">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-1062">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="f5912-1063">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="f5912-1063">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1064">Az.Storage</span></span>
* <span data-ttu-id="f5912-1065">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1065">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="f5912-1066">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1066">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="f5912-1067">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1067">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f5912-1068">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1068">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1069">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="f5912-1069">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f5912-1070">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f5912-1070">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f5912-1071">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="f5912-1071">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="f5912-1072">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f5912-1072">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="f5912-1073">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1073">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="f5912-1074">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f5912-1074">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="f5912-1075">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f5912-1075">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="f5912-1076">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="f5912-1076">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="f5912-1077">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1077">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f5912-1078">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="f5912-1078">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="f5912-1079">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f5912-1079">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="f5912-1080">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1080">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f5912-1081">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="f5912-1081">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-1082">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-1082">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-1083">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="f5912-1083">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="f5912-1084">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1084">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="f5912-1085">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="f5912-1085">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="f5912-1086">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1086">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1087">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1087">Az.Websites</span></span>
* <span data-ttu-id="f5912-1088">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="f5912-1088">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="f5912-1089">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1089">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-1090">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1090">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1091">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="f5912-1091">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="f5912-1092">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="f5912-1092">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="f5912-1093">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="f5912-1093">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="f5912-1094">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="f5912-1094">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-1095">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-1095">Az.Aks</span></span>
* <span data-ttu-id="f5912-1096">透過對 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="f5912-1096">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-1097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-1097">Az.Batch</span></span>
* <span data-ttu-id="f5912-1098">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1098">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="f5912-1099">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="f5912-1099">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-1100">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1100">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-1101">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-1101">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="f5912-1102">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="f5912-1102">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1103">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1103">Az.Compute</span></span>
* <span data-ttu-id="f5912-1104">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1104">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="f5912-1105">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="f5912-1105">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="f5912-1106">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="f5912-1106">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="f5912-1107">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="f5912-1107">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="f5912-1108">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-1108">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1109">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1109">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1110">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1110">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-1111">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1111">Az.EventHub</span></span>
* <span data-ttu-id="f5912-1112">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1112">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5912-1113">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5912-1113">Az.Functions</span></span>
* <span data-ttu-id="f5912-1114">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1114">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1115">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1115">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1116">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="f5912-1116">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5912-1117">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5912-1117">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5912-1118">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1118">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="f5912-1119">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1119">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1120">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1120">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1121">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1121">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="f5912-1122">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="f5912-1122">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1123">Az.Network</span></span>
* <span data-ttu-id="f5912-1124">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1124">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f5912-1125">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1125">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f5912-1126">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="f5912-1126">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="f5912-1127">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="f5912-1127">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="f5912-1128">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1128">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="f5912-1129">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1129">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="f5912-1130">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f5912-1130">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5912-1131">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f5912-1131">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5912-1132">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f5912-1132">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5912-1133">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f5912-1133">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="f5912-1134">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-1134">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="f5912-1135">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1135">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f5912-1136">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="f5912-1136">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="f5912-1137">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5912-1137">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="f5912-1138">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="f5912-1138">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="f5912-1139">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="f5912-1139">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="f5912-1140">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1140">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="f5912-1141">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="f5912-1141">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="f5912-1142">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="f5912-1142">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="f5912-1143">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="f5912-1143">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="f5912-1144">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="f5912-1144">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="f5912-1145">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-1145">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="f5912-1146">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="f5912-1146">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="f5912-1147">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1147">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="f5912-1148">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5912-1148">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f5912-1149">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5912-1149">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f5912-1150">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1150">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="f5912-1151">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="f5912-1151">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="f5912-1152">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1152">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5912-1153">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1153">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5912-1154">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1154">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5912-1155">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1155">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5912-1156">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1156">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5912-1157">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1157">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="f5912-1158">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1158">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="f5912-1159">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="f5912-1159">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="f5912-1160">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1160">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5912-1161">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1161">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5912-1162">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1162">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5912-1163">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1163">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="f5912-1164">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1164">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="f5912-1165">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1165">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f5912-1166">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1166">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f5912-1167">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1167">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5912-1168">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1168">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5912-1169">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1169">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="f5912-1170">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1170">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="f5912-1171">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1171">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="f5912-1172">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1172">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-1173">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1173">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-1174">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="f5912-1174">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="f5912-1175">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="f5912-1175">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="f5912-1176">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="f5912-1176">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="f5912-1177">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f5912-1177">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f5912-1178">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f5912-1178">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1179">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1180">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1180">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="f5912-1181">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="f5912-1181">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1182">Az.Resources</span></span>
* <span data-ttu-id="f5912-1183">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="f5912-1183">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="f5912-1184">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="f5912-1184">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="f5912-1185">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f5912-1185">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="f5912-1186">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1186">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="f5912-1187">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1187">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="f5912-1188">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1188">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1189">Az.Sql</span></span>
* <span data-ttu-id="f5912-1190">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1190">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="f5912-1191">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1191">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="f5912-1192">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="f5912-1192">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1193">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1193">Az.Storage</span></span>
* <span data-ttu-id="f5912-1194">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1194">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="f5912-1195">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1195">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1196">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1196">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1197">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1197">Az.Websites</span></span>
* <span data-ttu-id="f5912-1198">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="f5912-1198">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f5912-1199">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="f5912-1199">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="f5912-1200">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-1200">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="f5912-1201">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-1201">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="f5912-1202">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1202">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="f5912-1203">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="f5912-1203">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="f5912-1204">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1204">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-1205">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1205">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1206">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="f5912-1206">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-1207">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1207">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5912-1208">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1208">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-1209">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-1209">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-1210">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1210">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f5912-1211">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5912-1211">Az.Billing</span></span>
* <span data-ttu-id="f5912-1212">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1212">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-1213">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1213">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-1214">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="f5912-1214">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1215">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1215">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1216">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1216">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="f5912-1217">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="f5912-1217">Az.DataShare</span></span>
* <span data-ttu-id="f5912-1218">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="f5912-1218">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f5912-1219">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f5912-1219">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f5912-1220">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="f5912-1220">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-1221">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1221">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-1222">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1222">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="f5912-1223">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="f5912-1223">Added optional parameters to</span></span> 
    - <span data-ttu-id="f5912-1224">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f5912-1224">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f5912-1225">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f5912-1225">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-1226">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1226">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-1227">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="f5912-1227">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f5912-1228">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f5912-1228">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f5912-1229">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1229">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f5912-1230">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f5912-1230">Az.PrivateDns</span></span>
* <span data-ttu-id="f5912-1231">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="f5912-1231">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1232">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1232">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1233">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="f5912-1233">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="f5912-1234">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1234">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1235">Az.Resources</span></span>
* <span data-ttu-id="f5912-1236">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1236">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="f5912-1237">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="f5912-1237">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="f5912-1238">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f5912-1238">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="f5912-1239">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-1239">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="f5912-1240">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1240">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1241">Az.Sql</span></span>
* <span data-ttu-id="f5912-1242">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="f5912-1242">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f5912-1243">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="f5912-1243">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f5912-1244">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1244">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1245">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1245">Az.Storage</span></span>
* <span data-ttu-id="f5912-1246">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1246">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="f5912-1247">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1247">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f5912-1248">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-1248">Highlights since the last release</span></span>
* <span data-ttu-id="f5912-1249">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f5912-1249">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="f5912-1250">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="f5912-1250">General availability of Az.Functions</span></span> 
* <span data-ttu-id="f5912-1251">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1251">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-1252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1252">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1253">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1253">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="f5912-1254">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="f5912-1254">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-1255">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-1255">Az.Aks</span></span>
* <span data-ttu-id="f5912-1256">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f5912-1256">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="f5912-1257">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="f5912-1257">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="f5912-1258">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="f5912-1258">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-1259">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-1259">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-1260">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="f5912-1260">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="f5912-1261">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="f5912-1261">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="f5912-1262">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1262">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5912-1263">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="f5912-1263">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5912-1264">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1264">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5912-1265">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="f5912-1265">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="f5912-1266">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1266">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5912-1267">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="f5912-1267">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5912-1268">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1268">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5912-1269">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="f5912-1269">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5912-1270">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="f5912-1270">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="f5912-1271">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="f5912-1271">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="f5912-1272">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="f5912-1272">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="f5912-1273">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5912-1273">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="f5912-1274">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5912-1274">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="f5912-1275">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5912-1275">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f5912-1276">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1276">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f5912-1277">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="f5912-1277">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="f5912-1278">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="f5912-1278">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="f5912-1279">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1279">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-1280">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-1280">Az.Batch</span></span>
* <span data-ttu-id="f5912-1281">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="f5912-1281">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="f5912-1282">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="f5912-1282">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="f5912-1283">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1283">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="f5912-1284">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="f5912-1284">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="f5912-1285">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1285">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="f5912-1286">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="f5912-1286">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="f5912-1287">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="f5912-1287">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="f5912-1288">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1288">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="f5912-1289">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1289">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1290">Az.Compute</span></span>
* <span data-ttu-id="f5912-1291">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1291">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="f5912-1292">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="f5912-1292">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="f5912-1293">重大變更</span><span class="sxs-lookup"><span data-stu-id="f5912-1293">Breaking changes</span></span>
    - <span data-ttu-id="f5912-1294">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1294">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="f5912-1295">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1295">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="f5912-1296">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="f5912-1296">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="f5912-1297">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="f5912-1297">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="f5912-1298">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1298">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="f5912-1299">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="f5912-1299">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="f5912-1300">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="f5912-1300">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1301">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1301">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1302">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="f5912-1302">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-1304">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1304">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f5912-1305">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1305">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f5912-1306">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="f5912-1306">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="f5912-1307">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="f5912-1307">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5912-1308">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5912-1308">Az.Functions</span></span>
* <span data-ttu-id="f5912-1309">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="f5912-1309">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1310">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1310">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1311">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="f5912-1311">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5912-1312">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5912-1312">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5912-1313">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="f5912-1313">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-1314">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1314">Az.IotHub</span></span>
* <span data-ttu-id="f5912-1315">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="f5912-1315">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="f5912-1316">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="f5912-1316">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="f5912-1317">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="f5912-1317">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="f5912-1318">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="f5912-1318">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="f5912-1319">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="f5912-1319">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="f5912-1320">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1320">New cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1321">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1321">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5912-1322">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1322">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5912-1323">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1323">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5912-1324">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1324">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="f5912-1325">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="f5912-1325">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="f5912-1326">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="f5912-1326">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1327">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1327">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1328">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="f5912-1328">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="f5912-1329">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="f5912-1329">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="f5912-1330">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="f5912-1330">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="f5912-1331">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1331">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="f5912-1332">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="f5912-1332">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="f5912-1333">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="f5912-1333">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="f5912-1334">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="f5912-1334">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1335">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1336">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="f5912-1336">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="f5912-1337">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="f5912-1337">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="f5912-1338">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="f5912-1338">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="f5912-1339">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="f5912-1339">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="f5912-1340">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="f5912-1340">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="f5912-1341">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="f5912-1341">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="f5912-1342">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="f5912-1342">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1343">Az.Network</span></span>
* <span data-ttu-id="f5912-1344">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="f5912-1344">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="f5912-1345">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="f5912-1345">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="f5912-1346">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="f5912-1346">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="f5912-1347">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1347">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="f5912-1348">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1348">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="f5912-1349">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1349">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-1350">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5912-1350">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5912-1351">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5912-1351">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5912-1352">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5912-1352">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5912-1353">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5912-1353">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="f5912-1354">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="f5912-1354">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="f5912-1355">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="f5912-1355">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="f5912-1356">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="f5912-1356">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="f5912-1357">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="f5912-1357">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="f5912-1358">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="f5912-1358">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="f5912-1359">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="f5912-1359">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="f5912-1360">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1360">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="f5912-1361">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f5912-1361">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5912-1362">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f5912-1362">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5912-1363">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f5912-1363">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5912-1364">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f5912-1364">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="f5912-1365">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="f5912-1365">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="f5912-1366">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="f5912-1366">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="f5912-1367">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1367">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5912-1368">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f5912-1368">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-1369">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1369">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-1370">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="f5912-1370">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="f5912-1371">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1371">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="f5912-1372">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="f5912-1372">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="f5912-1373">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="f5912-1373">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="f5912-1374">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="f5912-1374">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="f5912-1375">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1375">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="f5912-1376">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1376">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="f5912-1377">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1377">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1378">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1379">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="f5912-1379">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="f5912-1380">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="f5912-1380">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="f5912-1381">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1381">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="f5912-1382">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="f5912-1382">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="f5912-1383">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="f5912-1383">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1384">Az.Resources</span></span>
* <span data-ttu-id="f5912-1385">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="f5912-1385">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="f5912-1386">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="f5912-1386">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="f5912-1387">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="f5912-1387">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="f5912-1388">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="f5912-1388">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="f5912-1389">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f5912-1389">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="f5912-1390">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f5912-1390">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="f5912-1391">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="f5912-1391">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="f5912-1392">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="f5912-1392">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f5912-1393">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1393">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="f5912-1394">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="f5912-1394">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="f5912-1395">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="f5912-1395">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="f5912-1396">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="f5912-1396">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="f5912-1397">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="f5912-1397">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="f5912-1398">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="f5912-1398">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="f5912-1399">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="f5912-1399">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="f5912-1400">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="f5912-1400">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="f5912-1401">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1401">'New-AzDeployment'</span></span>
    - <span data-ttu-id="f5912-1402">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1402">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="f5912-1403">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1403">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f5912-1404">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="f5912-1404">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-1405">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-1405">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-1406">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="f5912-1406">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1407">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1407">Az.Sql</span></span>
* <span data-ttu-id="f5912-1408">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="f5912-1408">Enhance performance of:</span></span>
    - <span data-ttu-id="f5912-1409">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f5912-1409">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5912-1410">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f5912-1410">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5912-1411">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f5912-1411">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5912-1412">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f5912-1412">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5912-1413">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f5912-1413">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5912-1414">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f5912-1414">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5912-1415">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f5912-1415">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5912-1416">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f5912-1416">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="f5912-1417">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-1417">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="f5912-1418">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-1418">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1419">Az.Storage</span></span>
* <span data-ttu-id="f5912-1420">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1420">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1421">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="f5912-1421">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="f5912-1422">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1422">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1423">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-1423">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="f5912-1424">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f5912-1424">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f5912-1425">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="f5912-1425">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="f5912-1426">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="f5912-1426">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="f5912-1427">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="f5912-1427">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="f5912-1428">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="f5912-1428">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="f5912-1429">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="f5912-1429">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="f5912-1430">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="f5912-1430">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="f5912-1431">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="f5912-1431">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="f5912-1432">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f5912-1432">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="f5912-1433">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1433">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="f5912-1434">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1434">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f5912-1435">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1435">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1436">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="f5912-1436">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="f5912-1437">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f5912-1437">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="f5912-1438">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f5912-1438">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f5912-1439">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1439">Supported failover Storage account</span></span>
    - <span data-ttu-id="f5912-1440">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="f5912-1440">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="f5912-1441">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-1441">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="f5912-1442">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-1442">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="f5912-1443">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1443">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="f5912-1444">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1444">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5912-1445">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="f5912-1445">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="f5912-1446">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="f5912-1446">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="f5912-1447">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1447">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f5912-1448">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1448">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f5912-1449">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="f5912-1449">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="f5912-1450">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1450">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5912-1451">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f5912-1451">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="f5912-1452">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f5912-1452">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f5912-1453">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1453">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5912-1454">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-1454">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="f5912-1455">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-1455">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="f5912-1456">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-1456">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="f5912-1457">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1457">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="f5912-1458">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="f5912-1458">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f5912-1459">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f5912-1459">Az.TrafficManager</span></span>
* <span data-ttu-id="f5912-1460">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-1460">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1461">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1461">Az.Websites</span></span>
* <span data-ttu-id="f5912-1462">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="f5912-1462">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f5912-1463">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1463">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f5912-1464">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-1464">Highlights since the last release</span></span>
* <span data-ttu-id="f5912-1465">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f5912-1465">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1466">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1467">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="f5912-1467">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-1468">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-1468">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-1469">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="f5912-1469">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f5912-1470">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1470">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-1471">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-1471">Az.Cdn</span></span>
* <span data-ttu-id="f5912-1472">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="f5912-1472">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-1473">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1473">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-1474">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="f5912-1474">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1475">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1475">Az.Compute</span></span>
* <span data-ttu-id="f5912-1476">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1476">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f5912-1477">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="f5912-1477">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-1478">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1478">Az.IotHub</span></span>
* <span data-ttu-id="f5912-1479">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1479">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1480">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f5912-1480">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f5912-1481">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f5912-1481">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f5912-1482">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="f5912-1482">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f5912-1483">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1483">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1484">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f5912-1484">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f5912-1485">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f5912-1485">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f5912-1486">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-1486">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f5912-1487">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1487">New cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1488">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1488">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5912-1489">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1489">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5912-1490">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1490">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5912-1491">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f5912-1491">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f5912-1492">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="f5912-1492">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1493">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1493">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1494">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="f5912-1494">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f5912-1495">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="f5912-1495">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f5912-1496">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="f5912-1496">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f5912-1497">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="f5912-1497">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f5912-1498">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f5912-1498">Az.Maintenance</span></span>
* <span data-ttu-id="f5912-1499">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1499">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1500">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1500">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1501">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1501">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f5912-1502">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-1502">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5912-1503">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-1503">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5912-1504">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-1504">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5912-1505">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f5912-1505">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5912-1506">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f5912-1506">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f5912-1507">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f5912-1507">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f5912-1508">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f5912-1508">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1509">Az.Network</span></span>
* <span data-ttu-id="f5912-1510">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="f5912-1510">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f5912-1511">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1511">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f5912-1512">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1512">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f5912-1513">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1513">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f5912-1514">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1514">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f5912-1515">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="f5912-1515">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f5912-1516">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f5912-1516">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f5912-1517">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="f5912-1517">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f5912-1518">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="f5912-1518">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f5912-1519">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1519">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f5912-1520">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f5912-1520">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f5912-1521">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f5912-1521">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f5912-1522">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="f5912-1522">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f5912-1523">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-1523">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f5912-1524">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-1524">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f5912-1525">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-1525">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-1526">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1526">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-1527">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1527">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f5912-1528">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="f5912-1528">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-1529">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-1529">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-1530">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-1530">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1531">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1531">Az.Sql</span></span>
* <span data-ttu-id="f5912-1532">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1532">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f5912-1533">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="f5912-1533">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1534">Az.Storage</span></span>
* <span data-ttu-id="f5912-1535">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="f5912-1535">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f5912-1536">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="f5912-1536">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f5912-1537">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1537">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f5912-1538">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1538">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5912-1539">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="f5912-1539">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f5912-1540">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-1540">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5912-1541">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-1541">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5912-1542">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f5912-1542">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f5912-1543">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-1543">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5912-1544">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="f5912-1544">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f5912-1545">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-1545">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5912-1546">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1546">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f5912-1547">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f5912-1547">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f5912-1548">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1548">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f5912-1549">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-1549">General</span></span>
* <span data-ttu-id="f5912-1550">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="f5912-1550">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f5912-1551">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1551">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f5912-1552">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="f5912-1552">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="f5912-1553">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="f5912-1553">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f5912-1554">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5912-1554">Az.Billing</span></span>
  - <span data-ttu-id="f5912-1555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1555">Az.Compute</span></span>
  - <span data-ttu-id="f5912-1556">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5912-1556">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f5912-1557">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1557">Az.EventHub</span></span>
  - <span data-ttu-id="f5912-1558">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1558">Az.IotHub</span></span>
  - <span data-ttu-id="f5912-1559">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1559">Az.KeyVault</span></span>
  - <span data-ttu-id="f5912-1560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1560">Az.Monitor</span></span>
  - <span data-ttu-id="f5912-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1561">Az.Network</span></span>
  - <span data-ttu-id="f5912-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1562">Az.Resources</span></span>
  - <span data-ttu-id="f5912-1563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1563">Az.Storage</span></span>
  - <span data-ttu-id="f5912-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1564">Az.Websites</span></span>
* <span data-ttu-id="f5912-1565">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1565">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f5912-1566">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="f5912-1566">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f5912-1567">您可以在[這裡](/azure-stack/operator/powershell-install-az-module)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="f5912-1567">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f5912-1568">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1568">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-1569">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1569">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1570">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="f5912-1570">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1571">Az.Compute</span></span>
* <span data-ttu-id="f5912-1572">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1572">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f5912-1573">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f5912-1573">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f5912-1574">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1574">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f5912-1575">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1575">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f5912-1576">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f5912-1576">[#11354]</span></span>
* <span data-ttu-id="f5912-1577">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1577">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f5912-1578">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-1578">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5912-1579">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-1579">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5912-1580">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-1580">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5912-1581">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f5912-1581">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f5912-1582">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-1582">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f5912-1583">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="f5912-1583">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f5912-1584">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="f5912-1584">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f5912-1585">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f5912-1585">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1586">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1587">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1587">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f5912-1588">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="f5912-1588">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-1589">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-1589">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-1590">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="f5912-1590">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f5912-1591">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="f5912-1591">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1592">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1592">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1593">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="f5912-1593">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-1594">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1594">Az.IotHub</span></span>
* <span data-ttu-id="f5912-1595">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1595">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f5912-1596">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1596">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1597">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="f5912-1597">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f5912-1598">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="f5912-1598">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1599">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1600">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="f5912-1600">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1601">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1601">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1602">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="f5912-1602">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1603">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1603">Az.Network</span></span>
* <span data-ttu-id="f5912-1604">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="f5912-1604">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f5912-1605">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1605">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5912-1606">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f5912-1606">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5912-1607">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="f5912-1607">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f5912-1608">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="f5912-1608">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f5912-1609">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-1609">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-1610">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1610">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-1611">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1611">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1612">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1612">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1613">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-1613">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f5912-1614">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="f5912-1614">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f5912-1615">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1615">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f5912-1616">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1616">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f5912-1617">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1617">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f5912-1618">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1618">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1619">Az.Resources</span></span>
* <span data-ttu-id="f5912-1620">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="f5912-1620">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f5912-1621">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="f5912-1621">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f5912-1622">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1622">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f5912-1623">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="f5912-1623">Added example.</span></span>
* <span data-ttu-id="f5912-1624">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="f5912-1624">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f5912-1625">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1625">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1626">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1626">Az.Sql</span></span>
* <span data-ttu-id="f5912-1627">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="f5912-1627">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f5912-1628">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="f5912-1628">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5912-1629">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="f5912-1629">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f5912-1630">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f5912-1630">Az.Support</span></span>
* <span data-ttu-id="f5912-1631">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-1631">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1632">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1632">Az.Websites</span></span>
* <span data-ttu-id="f5912-1633">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1633">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f5912-1634">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f5912-1634">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5912-1635">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f5912-1635">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5912-1636">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f5912-1636">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5912-1637">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f5912-1637">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f5912-1638">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1638">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-1639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1639">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1640">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="f5912-1640">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f5912-1641">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="f5912-1641">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f5912-1642">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1642">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-1643">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-1643">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-1644">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="f5912-1644">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f5912-1645">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="f5912-1645">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f5912-1646">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1646">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f5912-1647">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="f5912-1647">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-1648">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-1648">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-1649">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="f5912-1649">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-1650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1650">Az.IotHub</span></span>
* <span data-ttu-id="f5912-1651">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1651">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f5912-1652">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1652">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1653">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1653">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1654">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1654">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1655">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1655">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1656">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1656">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f5912-1657">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1657">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f5912-1658">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1658">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1659">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f5912-1659">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5912-1660">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f5912-1660">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5912-1661">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f5912-1661">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5912-1662">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f5912-1662">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f5912-1663">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="f5912-1663">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f5912-1664">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="f5912-1664">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f5912-1665">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1665">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f5912-1666">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1666">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1667">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1667">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f5912-1668">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f5912-1668">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f5912-1669">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1669">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1670">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1670">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1671">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="f5912-1671">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1672">Az.Network</span></span>
* <span data-ttu-id="f5912-1673">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-1673">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f5912-1674">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1674">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f5912-1675">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="f5912-1675">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f5912-1676">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1676">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1677">Az.Resources</span></span>
* <span data-ttu-id="f5912-1678">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-1678">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f5912-1679">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="f5912-1679">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f5912-1680">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="f5912-1680">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f5912-1681">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="f5912-1681">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f5912-1682">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-1682">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f5912-1683">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1683">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f5912-1684">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="f5912-1684">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f5912-1685">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5912-1685">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f5912-1686">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5912-1686">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f5912-1687">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5912-1687">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f5912-1688">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5912-1688">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f5912-1689">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1689">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f5912-1690">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5912-1690">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f5912-1691">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="f5912-1691">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1692">Az.Sql</span></span>
* <span data-ttu-id="f5912-1693">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1693">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f5912-1694">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1694">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f5912-1695">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="f5912-1695">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f5912-1696">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="f5912-1696">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f5912-1697">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="f5912-1697">Remove an LTR backup</span></span>
    - <span data-ttu-id="f5912-1698">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="f5912-1698">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f5912-1699">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f5912-1699">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f5912-1700">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-1700">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f5912-1701">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-1701">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1702">Az.Storage</span></span>
* <span data-ttu-id="f5912-1703">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="f5912-1703">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f5912-1704">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-1704">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f5912-1705">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1705">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f5912-1706">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1706">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f5912-1707">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f5912-1707">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1708">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1708">Az.Websites</span></span>
* <span data-ttu-id="f5912-1709">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1709">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f5912-1710">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1710">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f5912-1711">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="f5912-1711">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f5912-1712">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="f5912-1712">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f5912-1713">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-1713">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f5912-1714">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1714">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-1715">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-1715">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-1716">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="f5912-1716">Updated client side telemetry.</span></span>
* <span data-ttu-id="f5912-1717">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="f5912-1717">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f5912-1718">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1718">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1719">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1720">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="f5912-1720">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-1721">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-1721">Az.Automation</span></span>
* <span data-ttu-id="f5912-1722">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-1722">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-1723">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1723">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-1724">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1724">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f5912-1725">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1725">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1726">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1726">Az.Compute</span></span>
* <span data-ttu-id="f5912-1727">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="f5912-1727">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-1728">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-1728">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-1729">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="f5912-1729">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-1730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1730">Az.IotHub</span></span>
* <span data-ttu-id="f5912-1731">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1731">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f5912-1732">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-1732">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5912-1733">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1733">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1734">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1734">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1735">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1735">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5912-1736">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f5912-1736">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1737">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1738">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="f5912-1738">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1739">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1739">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1740">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="f5912-1740">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f5912-1741">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="f5912-1741">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f5912-1742">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="f5912-1742">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1743">Az.Network</span></span>
* <span data-ttu-id="f5912-1744">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="f5912-1744">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f5912-1745">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="f5912-1745">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f5912-1746">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="f5912-1746">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f5912-1747">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="f5912-1747">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f5912-1748">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1748">No new cmdlets are added.</span></span> <span data-ttu-id="f5912-1749">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="f5912-1749">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1751">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1751">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1752">Az.Resources</span></span>
* <span data-ttu-id="f5912-1753">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1753">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f5912-1754">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f5912-1754">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f5912-1755">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f5912-1755">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f5912-1756">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="f5912-1756">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f5912-1757">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="f5912-1757">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f5912-1758">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="f5912-1758">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f5912-1759">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="f5912-1759">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f5912-1760">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="f5912-1760">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1761">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1761">Az.Sql</span></span>
* <span data-ttu-id="f5912-1762">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1762">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f5912-1763">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1763">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f5912-1764">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f5912-1764">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f5912-1765">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f5912-1765">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f5912-1766">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1766">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-1767">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-1767">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-1768">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="f5912-1768">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f5912-1769">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1769">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-1770">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-1770">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-1771">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="f5912-1771">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f5912-1772">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="f5912-1772">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-1773">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1773">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1774">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="f5912-1774">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f5912-1775">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="f5912-1775">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-1776">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-1776">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-1777">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f5912-1777">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f5912-1778">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="f5912-1778">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="f5912-1779"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="f5912-1779">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f5912-1780">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f5912-1780">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1781">Az.Compute</span></span>
* <span data-ttu-id="f5912-1782">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="f5912-1782">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f5912-1783">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1783">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f5912-1784">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1784">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f5912-1785">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-1785">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f5912-1786">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1786">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1787">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1787">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1788">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1788">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f5912-1789">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f5912-1789">Az.DeploymentManager</span></span>
* <span data-ttu-id="f5912-1790">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="f5912-1790">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f5912-1791">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="f5912-1791">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1792">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1792">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1793">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-1793">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1794">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1795">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="f5912-1795">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1796">Az.Network</span></span>
* <span data-ttu-id="f5912-1797">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="f5912-1797">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f5912-1798">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="f5912-1798">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f5912-1799">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1799">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f5912-1800">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="f5912-1800">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f5912-1801">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="f5912-1801">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f5912-1802">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="f5912-1802">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f5912-1803">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="f5912-1803">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f5912-1804">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1804">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f5912-1805">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-1805">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f5912-1807">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1807">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f5912-1808">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5912-1808">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f5912-1809">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1809">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-1810">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-1810">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-1811">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="f5912-1811">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f5912-1812">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f5912-1812">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f5912-1813">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="f5912-1813">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f5912-1814">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="f5912-1814">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1815">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1815">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1816">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="f5912-1816">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f5912-1817">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1817">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1818">Az.Resources</span></span>
* <span data-ttu-id="f5912-1819">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="f5912-1819">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f5912-1820">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-1820">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1821">Az.Sql</span></span>
<span data-ttu-id="f5912-1822">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="f5912-1822">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1823">Az.Storage</span></span>
* <span data-ttu-id="f5912-1824">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="f5912-1824">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f5912-1825">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-1825">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5912-1826">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="f5912-1826">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f5912-1827">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="f5912-1827">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-1828">Az.Websites</span></span>
* <span data-ttu-id="f5912-1829">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1829">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f5912-1830">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-1830">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f5912-1831">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1831">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-1832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1832">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1833">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-1833">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-1834">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-1834">Az.Cdn</span></span>
* <span data-ttu-id="f5912-1835">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="f5912-1835">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1836">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1836">Az.Compute</span></span>
* <span data-ttu-id="f5912-1837">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-1837">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f5912-1838">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-1838">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5912-1839">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-1839">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f5912-1840">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5912-1840">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f5912-1841">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1841">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5912-1842">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="f5912-1842">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f5912-1843">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1843">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5912-1844">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="f5912-1844">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f5912-1845">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1845">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5912-1846">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="f5912-1846">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f5912-1847">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f5912-1847">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5912-1848">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="f5912-1848">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f5912-1849">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1849">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5912-1850">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1850">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f5912-1851">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1851">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5912-1852">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1852">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f5912-1853">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f5912-1853">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5912-1854">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-1854">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f5912-1855">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="f5912-1855">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f5912-1856">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="f5912-1856">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f5912-1857">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="f5912-1857">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f5912-1858">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="f5912-1858">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1859">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1859">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1860">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-1860">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f5912-1861">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1861">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f5912-1862">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="f5912-1862">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f5912-1863">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f5912-1863">Az.DevTestLabs</span></span>
* <span data-ttu-id="f5912-1864">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="f5912-1864">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-1865">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1865">Az.EventHub</span></span>
* <span data-ttu-id="f5912-1866">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="f5912-1866">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-1867">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-1867">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-1868">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-1868">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f5912-1869">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5912-1869">Az.MachineLearning</span></span>
* <span data-ttu-id="f5912-1870">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1870">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f5912-1871">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5912-1871">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5912-1872">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f5912-1872">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f5912-1873">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5912-1873">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5912-1874">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5912-1874">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5912-1875">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5912-1875">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5912-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f5912-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f5912-1877">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f5912-1877">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1878">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1878">Az.Network</span></span>
* <span data-ttu-id="f5912-1879">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f5912-1879">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1880">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1881">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="f5912-1881">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f5912-1882">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="f5912-1882">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f5912-1883">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="f5912-1883">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f5912-1884">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="f5912-1884">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1885">Az.Resources</span></span>
* <span data-ttu-id="f5912-1886">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-1886">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1887">Az.Sql</span></span>
* <span data-ttu-id="f5912-1888">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="f5912-1888">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f5912-1889">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-1889">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f5912-1890">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f5912-1890">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f5912-1891">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="f5912-1891">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1892">Az.Storage</span></span>
* <span data-ttu-id="f5912-1893">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1893">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f5912-1894">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-1894">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f5912-1895">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="f5912-1895">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f5912-1896">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-1896">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f5912-1897">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1897">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f5912-1898">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-1898">General</span></span>
* <span data-ttu-id="f5912-1899">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="f5912-1899">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-1900">Az.Accounts</span></span>
* <span data-ttu-id="f5912-1901">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="f5912-1901">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f5912-1902">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-1902">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-1903">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-1903">Az.Batch</span></span>
* <span data-ttu-id="f5912-1904">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5912-1904">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1905">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1905">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1906">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1906">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-1907">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-1907">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-1908">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1908">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f5912-1909">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="f5912-1909">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5912-1910">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5912-1910">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5912-1911">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="f5912-1911">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-1912">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-1912">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-1913">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-1913">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f5912-1914">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="f5912-1914">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f5912-1915">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1915">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-1916">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-1916">Az.Monitor</span></span>
* <span data-ttu-id="f5912-1917">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1917">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f5912-1918">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="f5912-1918">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f5912-1919">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="f5912-1919">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1920">Az.Network</span></span>
* <span data-ttu-id="f5912-1921">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="f5912-1921">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-1922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-1922">Az.Resources</span></span>
* <span data-ttu-id="f5912-1923">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1923">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f5912-1924">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-1924">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-1925">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-1925">Az.Sql</span></span>
* <span data-ttu-id="f5912-1926">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="f5912-1926">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-1927">Az.Storage</span></span>
* <span data-ttu-id="f5912-1928">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-1928">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f5912-1929">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f5912-1929">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f5912-1930">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5912-1930">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f5912-1931">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-1931">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f5912-1932">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f5912-1932">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f5912-1933">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="f5912-1933">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f5912-1934">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="f5912-1934">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f5912-1935">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-1935">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f5912-1936">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-1936">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f5912-1937">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="f5912-1937">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f5912-1938">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f5912-1938">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f5912-1939">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-1939">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f5912-1940">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f5912-1940">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f5912-1941">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f5912-1941">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-1942">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-1942">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-1943">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1943">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f5912-1944">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1944">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-1945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-1945">Az.Compute</span></span>
* <span data-ttu-id="f5912-1946">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="f5912-1946">VM Reapply feature</span></span>
    - <span data-ttu-id="f5912-1947">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1947">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f5912-1948">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="f5912-1948">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f5912-1949">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f5912-1949">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f5912-1950">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="f5912-1950">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f5912-1951">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="f5912-1951">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5912-1952">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1952">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f5912-1953">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="f5912-1953">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f5912-1954">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1954">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f5912-1955">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1955">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f5912-1956">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-1956">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f5912-1957">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5912-1957">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f5912-1958">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="f5912-1958">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5912-1959">取得訂單</span><span class="sxs-lookup"><span data-stu-id="f5912-1959">Get the Order</span></span>
* <span data-ttu-id="f5912-1960">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="f5912-1960">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5912-1961">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="f5912-1961">Create new Order</span></span>
* <span data-ttu-id="f5912-1962">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="f5912-1962">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5912-1963">移除訂單</span><span class="sxs-lookup"><span data-stu-id="f5912-1963">Remove the Order</span></span>
* <span data-ttu-id="f5912-1964">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="f5912-1964">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f5912-1965">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="f5912-1965">Now creates Local Share</span></span>
* <span data-ttu-id="f5912-1966">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="f5912-1966">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f5912-1967">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="f5912-1967">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f5912-1968">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="f5912-1968">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f5912-1969">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="f5912-1969">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f5912-1970">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="f5912-1970">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5912-1971">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-1971">Gets the information about Triggers</span></span>
* <span data-ttu-id="f5912-1972">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="f5912-1972">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5912-1973">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="f5912-1973">Create new Triggers</span></span>
* <span data-ttu-id="f5912-1974">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="f5912-1974">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5912-1975">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="f5912-1975">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-1976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-1976">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-1977">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="f5912-1977">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f5912-1978">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="f5912-1978">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-1980">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="f5912-1980">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-1981">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-1981">Az.EventHub</span></span>
* <span data-ttu-id="f5912-1982">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="f5912-1982">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-1983">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-1983">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-1984">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f5912-1984">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f5912-1985">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f5912-1985">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f5912-1986">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="f5912-1986">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f5912-1987">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f5912-1987">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-1988">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-1988">Az.Network</span></span>
* <span data-ttu-id="f5912-1989">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="f5912-1989">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f5912-1990">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f5912-1990">Az.PrivateDns</span></span>
* <span data-ttu-id="f5912-1991">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="f5912-1991">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-1992">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-1993">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="f5912-1993">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f5912-1994">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="f5912-1994">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f5912-1995">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="f5912-1995">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5912-1996">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5912-1996">Az.RedisCache</span></span>
* <span data-ttu-id="f5912-1997">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-1997">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f5912-1998">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="f5912-1998">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f5912-1999">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-1999">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2000">Az.Resources</span></span>
- <span data-ttu-id="f5912-2001">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2001">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f5912-2002">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2002">Updated create policy definition help example</span></span>
- <span data-ttu-id="f5912-2003">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="f5912-2003">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f5912-2004">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="f5912-2004">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f5912-2005">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5912-2005">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2006">Az.Sql</span></span>
* <span data-ttu-id="f5912-2007">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2007">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f5912-2008">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5912-2008">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f5912-2009">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2009">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f5912-2010">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-2010">General</span></span>
* <span data-ttu-id="f5912-2011">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2011">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2012">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2013">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-2013">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f5912-2014">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f5912-2014">Az.Advisor</span></span>
* <span data-ttu-id="f5912-2015">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="f5912-2015">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-2016">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-2016">Az.Batch</span></span>
* <span data-ttu-id="f5912-2017">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2017">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f5912-2018">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2018">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f5912-2019">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="f5912-2019">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f5912-2020">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="f5912-2020">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f5912-2021">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="f5912-2021">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f5912-2022">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="f5912-2022">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f5912-2023">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="f5912-2023">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f5912-2024">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="f5912-2024">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f5912-2025">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="f5912-2025">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f5912-2026">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2026">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f5912-2027">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="f5912-2027">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f5912-2028">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="f5912-2028">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f5912-2029">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2029">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f5912-2030">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2030">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f5912-2031">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2031">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f5912-2032">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2032">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f5912-2033">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2033">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f5912-2034">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2034">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f5912-2035">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="f5912-2035">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f5912-2036">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="f5912-2036">This operation is no longer supported.</span></span>
* <span data-ttu-id="f5912-2037">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2037">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f5912-2038">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2038">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f5912-2039">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="f5912-2039">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f5912-2040">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="f5912-2040">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f5912-2041">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="f5912-2041">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f5912-2042">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="f5912-2042">New non-verified images are also now returned.</span></span> <span data-ttu-id="f5912-2043">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f5912-2043">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f5912-2044">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="f5912-2044">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f5912-2045">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="f5912-2045">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f5912-2046">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="f5912-2046">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f5912-2047">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="f5912-2047">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f5912-2048">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="f5912-2048">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f5912-2049">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="f5912-2049">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f5912-2050">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="f5912-2050">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f5912-2051">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2051">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f5912-2052">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2052">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-2053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-2053">Az.Cdn</span></span>
* <span data-ttu-id="f5912-2054">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="f5912-2054">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f5912-2055">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="f5912-2055">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2056">Az.Compute</span></span>
* <span data-ttu-id="f5912-2057">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="f5912-2057">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f5912-2058">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f5912-2058">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f5912-2059">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5912-2059">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f5912-2060">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2060">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5912-2061">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2061">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f5912-2062">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="f5912-2062">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f5912-2063">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2063">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5912-2064">重大變更</span><span class="sxs-lookup"><span data-stu-id="f5912-2064">Breaking changes</span></span>
    - <span data-ttu-id="f5912-2065">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f5912-2065">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f5912-2066">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="f5912-2066">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2067">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2067">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2068">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2068">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-2069">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-2070">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="f5912-2070">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f5912-2071">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f5912-2071">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f5912-2072">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="f5912-2072">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f5912-2073">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="f5912-2073">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f5912-2074">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-2074">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f5912-2075">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-2075">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-2076">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-2076">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-2077">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2077">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-2078">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-2078">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-2079">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2079">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f5912-2080">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="f5912-2080">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f5912-2081">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2081">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f5912-2082">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2082">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f5912-2083">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5912-2083">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5912-2084">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5912-2084">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5912-2085">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5912-2085">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5912-2086">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5912-2086">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f5912-2087">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5912-2087">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f5912-2088">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2088">Added three cmdlets:</span></span>
    - <span data-ttu-id="f5912-2089">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="f5912-2089">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f5912-2090">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="f5912-2090">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f5912-2091">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="f5912-2091">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f5912-2092">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="f5912-2092">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f5912-2093">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="f5912-2093">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f5912-2094">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="f5912-2094">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f5912-2095">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="f5912-2095">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f5912-2096">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="f5912-2096">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f5912-2097">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="f5912-2097">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f5912-2098">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="f5912-2098">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f5912-2099">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="f5912-2099">Added some scenario test cases.</span></span>
* <span data-ttu-id="f5912-2100">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="f5912-2100">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-2101">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2101">Az.IotHub</span></span>
* <span data-ttu-id="f5912-2102">重大變更：</span><span class="sxs-lookup"><span data-stu-id="f5912-2102">Breaking changes:</span></span>
    - <span data-ttu-id="f5912-2103">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2103">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5912-2104">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2104">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5912-2105">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2105">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5912-2106">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2106">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5912-2107">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2107">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f5912-2108">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2108">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f5912-2109">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2109">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f5912-2110">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2110">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f5912-2111">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2111">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5912-2112">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2112">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5912-2113">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2113">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5912-2114">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2114">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2115">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2116">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="f5912-2116">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2117">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="f5912-2117">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f5912-2118">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="f5912-2118">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f5912-2119">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="f5912-2119">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2120">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="f5912-2120">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2121">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="f5912-2121">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2122">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="f5912-2122">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2123">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2123">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2124">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="f5912-2124">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2125">Az.Resources</span></span>
* <span data-ttu-id="f5912-2126">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="f5912-2126">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2127">Az.Network</span></span>
* <span data-ttu-id="f5912-2128">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f5912-2128">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f5912-2129">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5912-2130">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2130">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2131">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2131">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2132">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2132">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2133">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2133">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2134">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f5912-2135">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f5912-2135">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f5912-2136">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2136">New cmdlet:</span></span>
        - <span data-ttu-id="f5912-2137">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f5912-2137">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f5912-2138">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2138">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f5912-2139">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="f5912-2139">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f5912-2140">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="f5912-2140">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f5912-2141">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="f5912-2141">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f5912-2142">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2142">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f5912-2143">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="f5912-2143">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f5912-2144">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2144">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f5912-2145">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2145">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-2146">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f5912-2146">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f5912-2147">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-2147">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5912-2148">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-2148">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5912-2149">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-2149">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5912-2150">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2150">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f5912-2151">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2151">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f5912-2152">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2152">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5912-2153">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="f5912-2153">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f5912-2154">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="f5912-2154">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f5912-2155">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f5912-2155">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f5912-2156">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="f5912-2156">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f5912-2157">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2157">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f5912-2158">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-2159">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2159">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f5912-2160">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2160">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5912-2161">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5912-2161">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5912-2162">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5912-2162">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5912-2163">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5912-2163">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5912-2164">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5912-2164">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5912-2165">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5912-2165">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f5912-2166">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2166">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f5912-2167">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2167">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-2168">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f5912-2168">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f5912-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f5912-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f5912-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f5912-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f5912-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f5912-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f5912-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f5912-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f5912-2174">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2174">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5912-2175">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2175">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f5912-2176">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2176">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f5912-2177">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="f5912-2177">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f5912-2178">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2178">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f5912-2179">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2179">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5912-2180">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f5912-2180">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f5912-2181">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f5912-2181">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f5912-2182">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="f5912-2182">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f5912-2183">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="f5912-2183">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f5912-2184">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2184">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f5912-2185">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2185">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-2186">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2186">New-AzIpGroup</span></span>
        - <span data-ttu-id="f5912-2187">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2187">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f5912-2188">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2188">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f5912-2189">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2189">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-2190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2190">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-2191">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="f5912-2191">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2192">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2192">Az.Sql</span></span>
* <span data-ttu-id="f5912-2193">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2193">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f5912-2194">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-2194">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f5912-2195">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="f5912-2195">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f5912-2196">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="f5912-2196">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f5912-2197">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="f5912-2197">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f5912-2198">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2198">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f5912-2199">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="f5912-2199">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f5912-2200">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2200">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f5912-2201">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="f5912-2201">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2202">Az.Storage</span></span>
* <span data-ttu-id="f5912-2203">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="f5912-2203">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f5912-2204">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2204">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f5912-2205">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2205">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f5912-2206">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="f5912-2206">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f5912-2207">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5912-2207">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f5912-2208">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5912-2208">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f5912-2209">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="f5912-2209">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f5912-2210">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-2210">General</span></span>
* <span data-ttu-id="f5912-2211">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-2211">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2212">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2213">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="f5912-2213">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-2214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-2214">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-2215">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2215">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f5912-2216">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2216">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-2217">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-2217">Az.Automation</span></span>
* <span data-ttu-id="f5912-2218">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-2218">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-2219">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-2219">Az.Batch</span></span>
* <span data-ttu-id="f5912-2220">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="f5912-2220">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2221">Az.Compute</span></span>
* <span data-ttu-id="f5912-2222">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2222">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5912-2223">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="f5912-2223">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f5912-2224">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="f5912-2224">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f5912-2225">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="f5912-2225">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2226">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2226">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2227">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="f5912-2227">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f5912-2228">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="f5912-2228">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f5912-2229">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2229">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-2230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-2230">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-2231">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-2231">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5912-2232">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5912-2232">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5912-2233">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2233">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f5912-2234">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f5912-2234">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f5912-2235">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-2235">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f5912-2236">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="f5912-2236">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2237">Az.IotHub</span></span>
* <span data-ttu-id="f5912-2238">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f5912-2238">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f5912-2239">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5912-2239">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-2240">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-2240">Az.Monitor</span></span>
* <span data-ttu-id="f5912-2241">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f5912-2241">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f5912-2242">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="f5912-2242">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f5912-2243">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="f5912-2243">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f5912-2244">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-2244">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2245">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2245">Az.Network</span></span>
* <span data-ttu-id="f5912-2246">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="f5912-2246">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f5912-2247">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2247">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f5912-2248">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2248">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-2249">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-2249">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f5912-2250">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2250">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f5912-2251">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2251">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f5912-2252">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2252">Updated cmdlets:</span></span>
        - <span data-ttu-id="f5912-2253">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2253">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5912-2254">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2254">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5912-2255">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2255">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f5912-2256">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="f5912-2256">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f5912-2257">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="f5912-2257">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f5912-2258">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="f5912-2258">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f5912-2259">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="f5912-2259">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5912-2260">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5912-2260">Az.RedisCache</span></span>
* <span data-ttu-id="f5912-2261">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="f5912-2261">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2262">Az.Sql</span></span>
* <span data-ttu-id="f5912-2263">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2263">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2264">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2264">Az.Storage</span></span>
* <span data-ttu-id="f5912-2265">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2265">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f5912-2266">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="f5912-2266">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f5912-2267">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f5912-2267">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f5912-2268">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="f5912-2268">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f5912-2269">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2269">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-2270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-2270">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-2271">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="f5912-2271">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2272">Az.Websites</span></span>
* <span data-ttu-id="f5912-2273">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="f5912-2273">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f5912-2274">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2274">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f5912-2275">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-2275">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-2276">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2276">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f5912-2277">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="f5912-2277">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f5912-2278">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2278">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-2279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-2279">Az.Automation</span></span>
* <span data-ttu-id="f5912-2280">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="f5912-2280">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f5912-2281">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="f5912-2281">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f5912-2282">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f5912-2282">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2283">Az.Compute</span></span>
* <span data-ttu-id="f5912-2284">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2284">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f5912-2285">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2285">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5912-2286">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="f5912-2286">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f5912-2287">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="f5912-2287">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f5912-2288">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="f5912-2288">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f5912-2289">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="f5912-2289">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f5912-2290">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f5912-2290">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f5912-2291">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="f5912-2291">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f5912-2292">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-2292">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2293">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2294">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f5912-2294">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f5912-2295">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="f5912-2295">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-2296">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-2296">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-2297">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="f5912-2297">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-2298">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2298">Az.IotHub</span></span>
* <span data-ttu-id="f5912-2299">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2299">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f5912-2300">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2300">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f5912-2301">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="f5912-2301">New cmdlets are:</span></span>
    - <span data-ttu-id="f5912-2302">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5912-2302">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5912-2303">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5912-2303">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5912-2304">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5912-2304">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5912-2305">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5912-2305">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-2306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-2306">Az.Monitor</span></span>
* <span data-ttu-id="f5912-2307">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="f5912-2307">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f5912-2308">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="f5912-2308">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f5912-2309">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="f5912-2309">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f5912-2310">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="f5912-2310">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f5912-2311">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="f5912-2311">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f5912-2312">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="f5912-2312">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f5912-2313">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="f5912-2313">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f5912-2314">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-2314">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f5912-2315">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-2315">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f5912-2316">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="f5912-2316">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f5912-2317">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-2317">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f5912-2318">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="f5912-2318">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f5912-2319">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="f5912-2319">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f5912-2320">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="f5912-2320">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f5912-2321">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="f5912-2321">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f5912-2322">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="f5912-2322">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f5912-2323">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="f5912-2323">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f5912-2324">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2324">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f5912-2325">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2325">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f5912-2326">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="f5912-2326">Overall improved help files</span></span>
* <span data-ttu-id="f5912-2327">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-2327">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2328">Az.Network</span></span>
* <span data-ttu-id="f5912-2329">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2329">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f5912-2330">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-2330">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f5912-2331">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="f5912-2331">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f5912-2332">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="f5912-2332">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f5912-2333">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="f5912-2333">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f5912-2334">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="f5912-2334">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f5912-2335">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="f5912-2335">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f5912-2336">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="f5912-2336">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f5912-2337">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="f5912-2337">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f5912-2338">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="f5912-2338">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f5912-2339">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="f5912-2339">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f5912-2340">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="f5912-2340">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f5912-2341">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2341">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2342">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f5912-2342">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f5912-2343">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2343">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f5912-2344">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2344">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5912-2345">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f5912-2345">New-VpnSite</span></span>
        - <span data-ttu-id="f5912-2346">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f5912-2346">Update-VpnSite</span></span>
        - <span data-ttu-id="f5912-2347">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2347">New-VpnConnection</span></span>
        - <span data-ttu-id="f5912-2348">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2348">Update-VpnConnection</span></span>
* <span data-ttu-id="f5912-2349">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2349">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2350">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2351">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="f5912-2351">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f5912-2352">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="f5912-2352">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2353">Az.Resources</span></span>
* <span data-ttu-id="f5912-2354">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2354">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-2355">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2355">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-2356">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2356">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f5912-2357">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="f5912-2357">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f5912-2358">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5912-2358">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5912-2359">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5912-2359">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5912-2360">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5912-2360">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5912-2361">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f5912-2361">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f5912-2362">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5912-2362">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5912-2363">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5912-2363">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5912-2364">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5912-2364">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5912-2365">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5912-2365">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5912-2366">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f5912-2366">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f5912-2367">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5912-2367">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5912-2368">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5912-2368">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5912-2369">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5912-2369">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5912-2370">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f5912-2370">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f5912-2371">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="f5912-2371">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5912-2372">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5912-2372">Az.SignalR</span></span>
* <span data-ttu-id="f5912-2373">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2373">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2374">Az.Sql</span></span>
* <span data-ttu-id="f5912-2375">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2375">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f5912-2376">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2376">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f5912-2377">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="f5912-2377">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f5912-2378">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-2378">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f5912-2379">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2379">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2380">Az.Storage</span></span>
* <span data-ttu-id="f5912-2381">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2381">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f5912-2382">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="f5912-2382">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f5912-2383">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5912-2383">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f5912-2384">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5912-2384">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f5912-2385">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-2385">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f5912-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5912-2386">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f5912-2387">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="f5912-2387">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f5912-2388">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-2388">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5912-2389">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-2389">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5912-2390">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-2390">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5912-2391">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5912-2391">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2392">Az.Websites</span></span>
* <span data-ttu-id="f5912-2393">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2393">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f5912-2394">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="f5912-2394">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f5912-2395">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2395">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f5912-2396">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2396">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f5912-2397">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-2397">General</span></span>
* <span data-ttu-id="f5912-2398">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2398">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-2399">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2399">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2400">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="f5912-2400">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-2401">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-2401">Az.Aks</span></span>
* <span data-ttu-id="f5912-2402">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2402">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f5912-2403">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f5912-2403">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-2404">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-2404">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-2405">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2405">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f5912-2406">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="f5912-2406">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f5912-2407">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2407">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f5912-2408">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f5912-2408">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f5912-2409">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f5912-2409">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-2410">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-2410">Az.Batch</span></span>
* <span data-ttu-id="f5912-2411">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="f5912-2411">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-2412">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-2412">Az.Cdn</span></span>
* <span data-ttu-id="f5912-2413">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2413">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2414">Az.Compute</span></span>
* <span data-ttu-id="f5912-2415">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2415">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f5912-2416">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="f5912-2416">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f5912-2417">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="f5912-2417">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f5912-2418">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="f5912-2418">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f5912-2419">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f5912-2419">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f5912-2420">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="f5912-2420">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f5912-2421">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-2421">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f5912-2422">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2422">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2423">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2423">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2424">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="f5912-2424">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f5912-2425">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="f5912-2425">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f5912-2426">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="f5912-2426">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f5912-2427">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="f5912-2427">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-2428">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-2428">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-2429">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f5912-2429">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-2430">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2430">Az.EventHub</span></span>
* <span data-ttu-id="f5912-2431">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2431">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f5912-2432">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="f5912-2432">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f5912-2433">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2433">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f5912-2434">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="f5912-2434">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f5912-2435">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f5912-2435">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f5912-2436">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2436">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-2437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-2437">Az.Monitor</span></span>
* <span data-ttu-id="f5912-2438">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-2438">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2439">Az.Network</span></span>
* <span data-ttu-id="f5912-2440">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2440">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f5912-2441">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2441">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f5912-2442">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="f5912-2442">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f5912-2443">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2443">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f5912-2444">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="f5912-2444">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f5912-2445">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="f5912-2445">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f5912-2446">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2446">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-2447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2447">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-2448">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="f5912-2448">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f5912-2449">新增了範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2449">Added example</span></span>
    - <span data-ttu-id="f5912-2450">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-2450">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f5912-2451">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2451">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f5912-2452">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2452">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2453">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2454">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2454">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2455">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2455">Az.Resources</span></span>
* <span data-ttu-id="f5912-2456">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2456">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f5912-2457">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2457">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f5912-2458">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="f5912-2458">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f5912-2459">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2459">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-2460">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-2460">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-2461">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2461">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f5912-2462">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="f5912-2462">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f5912-2463">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-2463">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-2464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2464">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-2465">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="f5912-2465">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f5912-2466">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2466">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f5912-2467">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f5912-2467">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f5912-2468">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2468">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f5912-2469">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f5912-2469">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f5912-2470">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2470">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2471">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2471">Az.Sql</span></span>
* <span data-ttu-id="f5912-2472">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="f5912-2472">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2473">Az.Storage</span></span>
* <span data-ttu-id="f5912-2474">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2474">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f5912-2475">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="f5912-2475">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f5912-2476">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5912-2476">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f5912-2477">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5912-2477">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f5912-2478">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="f5912-2478">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f5912-2479">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5912-2479">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2480">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2480">Az.Websites</span></span>
* <span data-ttu-id="f5912-2481">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="f5912-2481">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f5912-2482">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2482">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2483">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2484">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5912-2484">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f5912-2485">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2485">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f5912-2486">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2486">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-2487">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-2487">Az.Automation</span></span>
* <span data-ttu-id="f5912-2488">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2488">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-2490">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2490">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2491">Az.Compute</span></span>
* <span data-ttu-id="f5912-2492">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2492">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5912-2493">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5912-2493">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5912-2494">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2494">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f5912-2495">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f5912-2495">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2496">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2497">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f5912-2497">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f5912-2498">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2498">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-2499">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2499">Az.EventHub</span></span>
* <span data-ttu-id="f5912-2500">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f5912-2500">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f5912-2501">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-2501">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-2502">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-2502">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-2503">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2503">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-2504">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-2504">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-2505">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="f5912-2505">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f5912-2506">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2506">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f5912-2507">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2507">Az.ManagedServices</span></span>
* <span data-ttu-id="f5912-2508">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2508">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2509">Az.Network</span></span>
* <span data-ttu-id="f5912-2510">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2510">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f5912-2511">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2511">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2512">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5912-2512">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5912-2513">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2513">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5912-2514">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2514">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2515">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2515">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2516">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2516">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2517">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2517">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5912-2518">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f5912-2518">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f5912-2519">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2519">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f5912-2520">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="f5912-2520">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f5912-2521">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2521">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f5912-2522">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="f5912-2522">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f5912-2523">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="f5912-2523">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f5912-2524">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="f5912-2524">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f5912-2525">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="f5912-2525">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f5912-2526">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2526">Updated cmdlets</span></span>
        - <span data-ttu-id="f5912-2527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5912-2528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5912-2529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f5912-2530">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2530">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f5912-2531">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f5912-2531">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f5912-2532">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2532">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5912-2533">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2533">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f5912-2534">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2534">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f5912-2535">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2535">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f5912-2536">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="f5912-2536">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f5912-2537">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="f5912-2537">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f5912-2538">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="f5912-2538">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-2539">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2539">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-2540">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="f5912-2540">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f5912-2541">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="f5912-2541">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2542">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2542">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2543">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2543">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f5912-2544">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2544">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f5912-2545">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2545">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f5912-2546">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2546">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f5912-2547">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2547">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f5912-2548">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2548">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f5912-2549">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2549">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f5912-2550">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2550">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f5912-2551">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="f5912-2551">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f5912-2552">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="f5912-2552">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2553">Az.Resources</span></span>
- <span data-ttu-id="f5912-2554">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2554">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f5912-2555">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f5912-2555">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-2556">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-2556">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-2557">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f5912-2557">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f5912-2558">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-2558">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2559">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2559">Az.Sql</span></span>
* <span data-ttu-id="f5912-2560">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2560">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f5912-2561">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2561">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f5912-2562">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="f5912-2562">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2563">Az.Storage</span></span>
* <span data-ttu-id="f5912-2564">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-2564">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-2565">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-2565">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-2566">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-2566">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f5912-2567">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="f5912-2567">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2568">Az.Websites</span></span>
* <span data-ttu-id="f5912-2569">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-2569">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f5912-2570">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2570">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f5912-2571">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-2571">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f5912-2572">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2572">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-2573">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2573">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2574">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2574">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f5912-2575">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2575">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f5912-2576">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2576">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f5912-2577">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f5912-2577">Az.Advisor</span></span>
* <span data-ttu-id="f5912-2578">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="f5912-2578">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f5912-2579">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="f5912-2579">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5912-2580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-2580">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-2581">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2581">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f5912-2582">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f5912-2582">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f5912-2583">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2583">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f5912-2584">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2584">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f5912-2585">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2585">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f5912-2586">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f5912-2586">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f5912-2587">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2587">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-2588">Az.Automation</span></span>
* <span data-ttu-id="f5912-2589">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="f5912-2589">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2590">Az.Compute</span></span>
* <span data-ttu-id="f5912-2591">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2591">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2592">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2593">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="f5912-2593">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5912-2594">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5912-2594">Az.EventGrid</span></span>
* <span data-ttu-id="f5912-2595">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2595">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-2596">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2596">Az.IotHub</span></span>
* <span data-ttu-id="f5912-2597">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2597">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2598">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2598">Az.Network</span></span>
* <span data-ttu-id="f5912-2599">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="f5912-2599">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f5912-2600">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-2600">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-2601">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2601">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-2602">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2602">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f5912-2603">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f5912-2603">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-2604">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2604">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-2605">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="f5912-2605">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2606">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2606">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2607">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="f5912-2607">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2608">Az.Resources</span></span>
    - <span data-ttu-id="f5912-2609">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="f5912-2609">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f5912-2610">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2610">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f5912-2611">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="f5912-2611">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f5912-2612">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="f5912-2612">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-2613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-2613">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-2614">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f5912-2614">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2615">Az.Sql</span></span>
* <span data-ttu-id="f5912-2616">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="f5912-2616">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f5912-2617">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="f5912-2617">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f5912-2618">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2618">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5912-2619">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2619">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5912-2620">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2620">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5912-2621">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2621">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f5912-2622">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2622">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f5912-2623">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5912-2623">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f5912-2624">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="f5912-2624">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2625">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2625">Az.Storage</span></span>
* <span data-ttu-id="f5912-2626">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="f5912-2626">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f5912-2627">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5912-2627">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f5912-2628">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-2628">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f5912-2629">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-2629">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f5912-2630">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f5912-2630">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f5912-2631">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2631">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f5912-2632">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2632">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f5912-2633">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="f5912-2633">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f5912-2634">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5912-2634">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f5912-2635">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5912-2635">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5912-2636">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5912-2636">Az.StorageSync</span></span>
* <span data-ttu-id="f5912-2637">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="f5912-2637">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f5912-2638">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2638">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-2639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2639">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2640">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-2640">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f5912-2641">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f5912-2641">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f5912-2642">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2642">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f5912-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f5912-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f5912-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f5912-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2645">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2645">Az.Compute</span></span>
* <span data-ttu-id="f5912-2646">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2646">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f5912-2647">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2647">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f5912-2648">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f5912-2648">Az.Dns</span></span>
* <span data-ttu-id="f5912-2649">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="f5912-2649">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5912-2650">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5912-2650">Az.EventGrid</span></span>
* <span data-ttu-id="f5912-2651">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f5912-2651">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f5912-2652">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2652">New cmdlets:</span></span>
    - <span data-ttu-id="f5912-2653">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5912-2653">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5912-2654">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="f5912-2654">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5912-2655">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5912-2655">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5912-2656">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="f5912-2656">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f5912-2657">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5912-2657">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5912-2658">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="f5912-2658">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5912-2659">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f5912-2659">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f5912-2660">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5912-2660">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5912-2661">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f5912-2661">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f5912-2662">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f5912-2662">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f5912-2663">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="f5912-2663">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f5912-2664">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="f5912-2664">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f5912-2665">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f5912-2665">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f5912-2666">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="f5912-2666">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f5912-2667">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="f5912-2667">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f5912-2668">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="f5912-2668">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f5912-2669">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2669">Updated cmdlets:</span></span>
    - <span data-ttu-id="f5912-2670">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="f5912-2670">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f5912-2671">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5912-2671">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f5912-2672">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5912-2672">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f5912-2673">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="f5912-2673">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f5912-2674">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f5912-2674">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f5912-2675">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="f5912-2675">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f5912-2676">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2676">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f5912-2677">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="f5912-2677">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f5912-2678">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="f5912-2678">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f5912-2679">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="f5912-2679">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f5912-2680">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="f5912-2680">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f5912-2681">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f5912-2681">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f5912-2682">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5912-2682">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f5912-2683">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5912-2683">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-2684">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-2684">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-2685">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f5912-2685">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f5912-2686">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f5912-2686">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f5912-2687">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5912-2687">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f5912-2688">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="f5912-2688">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2689">Az.Network</span></span>
* <span data-ttu-id="f5912-2690">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2690">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f5912-2691">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2691">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f5912-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f5912-2693">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f5912-2693">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f5912-2694">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2694">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2695">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f5912-2695">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f5912-2696">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2696">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f5912-2697">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2697">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2698">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2698">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5912-2699">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2699">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5912-2700">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5912-2700">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5912-2701">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2701">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f5912-2702">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2702">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f5912-2703">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5912-2703">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f5912-2704">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2704">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2705">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5912-2705">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5912-2706">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5912-2706">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5912-2707">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5912-2707">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5912-2708">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f5912-2708">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f5912-2709">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="f5912-2709">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f5912-2710">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="f5912-2710">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f5912-2711">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="f5912-2711">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f5912-2712">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="f5912-2712">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f5912-2713">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="f5912-2713">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f5912-2714">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="f5912-2714">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f5912-2715">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-2715">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f5912-2716">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-2716">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f5912-2717">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2717">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f5912-2718">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="f5912-2718">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f5912-2719">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="f5912-2719">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f5912-2720">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2720">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f5912-2721">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f5912-2721">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f5912-2722">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2722">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f5912-2723">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2723">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f5912-2724">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="f5912-2724">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f5912-2725">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="f5912-2725">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f5912-2726">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="f5912-2726">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f5912-2727">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="f5912-2727">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f5912-2728">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="f5912-2728">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f5912-2729">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f5912-2729">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f5912-2730">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f5912-2730">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f5912-2731">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f5912-2731">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-2732">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2732">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-2733">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="f5912-2733">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2734">Az.Resources</span></span>
* <span data-ttu-id="f5912-2735">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="f5912-2735">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f5912-2736">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2736">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f5912-2737">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2737">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f5912-2738">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="f5912-2738">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-2740">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2740">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2741">Az.Sql</span></span>
* <span data-ttu-id="f5912-2742">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="f5912-2742">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f5912-2743">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="f5912-2743">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f5912-2744">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="f5912-2744">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f5912-2745">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5912-2745">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5912-2746">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5912-2746">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5912-2747">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5912-2747">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5912-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f5912-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f5912-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f5912-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2750">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2750">Az.Storage</span></span>
* <span data-ttu-id="f5912-2751">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="f5912-2751">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f5912-2752">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2752">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5912-2753">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-2753">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f5912-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2755">Az.Websites</span></span>
* <span data-ttu-id="f5912-2756">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="f5912-2756">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f5912-2757">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f5912-2757">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f5912-2758">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2758">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f5912-2759">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-2759">Az.Cdn</span></span>
* <span data-ttu-id="f5912-2760">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-2760">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2761">Az.Compute</span></span>
* <span data-ttu-id="f5912-2762">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="f5912-2762">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f5912-2763">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f5912-2763">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-2764">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-2764">Az.EventHub</span></span>
* <span data-ttu-id="f5912-2765">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="f5912-2765">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f5912-2766">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5912-2766">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2767">Az.Network</span></span>
* <span data-ttu-id="f5912-2768">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="f5912-2768">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f5912-2769">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="f5912-2769">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-2770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2770">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-2771">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2771">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2772">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2772">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2773">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="f5912-2773">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-2774">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-2774">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-2775">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5912-2775">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-2776">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2776">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-2777">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2777">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f5912-2778">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="f5912-2778">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2779">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2779">Az.Sql</span></span>
* <span data-ttu-id="f5912-2780">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="f5912-2780">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f5912-2781">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2781">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f5912-2782">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="f5912-2782">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f5912-2783">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2783">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2784">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2784">Az.Websites</span></span>
* <span data-ttu-id="f5912-2785">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2785">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f5912-2786">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2786">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f5912-2787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-2787">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-2788">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="f5912-2788">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f5912-2789">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="f5912-2789">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f5912-2790">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="f5912-2790">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f5912-2791">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="f5912-2791">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f5912-2792">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-2792">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f5912-2793">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="f5912-2793">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f5912-2794">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="f5912-2794">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f5912-2795">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="f5912-2795">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f5912-2796">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="f5912-2796">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f5912-2797">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="f5912-2797">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f5912-2798">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="f5912-2798">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f5912-2799">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="f5912-2799">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f5912-2800">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="f5912-2800">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f5912-2801">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2801">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f5912-2802">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2802">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f5912-2803">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2803">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f5912-2804">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2804">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f5912-2805">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f5912-2805">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f5912-2806">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="f5912-2806">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f5912-2807">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="f5912-2807">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f5912-2808">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="f5912-2808">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f5912-2809">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="f5912-2809">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f5912-2810">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="f5912-2810">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f5912-2811">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="f5912-2811">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f5912-2812">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2812">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f5912-2813">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2813">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f5912-2814">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="f5912-2814">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f5912-2815">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="f5912-2815">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f5912-2816">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2816">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f5912-2817">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="f5912-2817">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f5912-2818">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-2818">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f5912-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f5912-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f5912-2820">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="f5912-2820">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f5912-2821">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f5912-2821">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5912-2822">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="f5912-2822">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f5912-2823">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2823">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f5912-2824">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-2824">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f5912-2825">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="f5912-2825">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f5912-2826">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="f5912-2826">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f5912-2827">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f5912-2827">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5912-2828">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="f5912-2828">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f5912-2829">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="f5912-2829">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f5912-2830">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="f5912-2830">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f5912-2831">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2831">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f5912-2832">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f5912-2832">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5912-2833">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="f5912-2833">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f5912-2834">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="f5912-2834">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f5912-2835">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2835">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f5912-2836">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f5912-2836">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f5912-2837">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="f5912-2837">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f5912-2838">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2838">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f5912-2839">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="f5912-2839">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f5912-2840">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2840">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f5912-2841">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f5912-2841">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f5912-2842">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="f5912-2842">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f5912-2843">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="f5912-2843">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f5912-2844">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f5912-2844">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f5912-2845">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="f5912-2845">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f5912-2846">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="f5912-2846">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f5912-2847">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2847">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f5912-2848">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f5912-2848">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f5912-2849">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="f5912-2849">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f5912-2850">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="f5912-2850">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f5912-2851">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-2851">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f5912-2852">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="f5912-2852">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f5912-2853">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="f5912-2853">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f5912-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f5912-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f5912-2855">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="f5912-2855">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f5912-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f5912-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f5912-2857">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f5912-2857">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f5912-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f5912-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f5912-2859">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f5912-2859">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f5912-2860">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="f5912-2860">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f5912-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f5912-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f5912-2862">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-2862">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f5912-2863">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f5912-2863">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f5912-2864">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="f5912-2864">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-2865">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-2865">Az.Automation</span></span>
* <span data-ttu-id="f5912-2866">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="f5912-2866">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f5912-2867">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2867">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f5912-2868">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2868">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f5912-2869">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="f5912-2869">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f5912-2870">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2870">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f5912-2871">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-2871">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f5912-2872">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="f5912-2872">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2873">Az.Compute</span></span>
* <span data-ttu-id="f5912-2874">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-2874">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f5912-2875">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="f5912-2875">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-2876">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-2876">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-2877">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="f5912-2877">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-2878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-2878">Az.Monitor</span></span>
* <span data-ttu-id="f5912-2879">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-2879">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2880">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2880">Az.Network</span></span>
* <span data-ttu-id="f5912-2881">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="f5912-2881">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f5912-2882">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2882">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5912-2883">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-2883">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f5912-2884">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="f5912-2884">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-2885">Az.Resources</span></span>
* <span data-ttu-id="f5912-2886">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="f5912-2886">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-2887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-2887">Az.Sql</span></span>
* <span data-ttu-id="f5912-2888">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="f5912-2888">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f5912-2889">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2889">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-2890">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2890">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2891">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2891">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-2892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2892">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-2893">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="f5912-2893">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f5912-2894">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-2894">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2895">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2895">Az.Compute</span></span>
* <span data-ttu-id="f5912-2896">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-2896">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f5912-2897">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2897">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f5912-2898">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-2898">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f5912-2899">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="f5912-2899">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f5912-2900">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="f5912-2900">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f5912-2901">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f5912-2901">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f5912-2902">重大變更</span><span class="sxs-lookup"><span data-stu-id="f5912-2902">Breaking changes</span></span>
    - <span data-ttu-id="f5912-2903">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="f5912-2903">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f5912-2904">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="f5912-2904">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f5912-2905">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f5912-2905">Az.DeploymentManager</span></span>
* <span data-ttu-id="f5912-2906">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2906">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f5912-2907">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f5912-2907">Az.Dns</span></span>
* <span data-ttu-id="f5912-2908">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="f5912-2908">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f5912-2909">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-2909">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f5912-2910">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f5912-2910">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5912-2911">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-2911">Az.FrontDoor</span></span>
* <span data-ttu-id="f5912-2912">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2912">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f5912-2913">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="f5912-2913">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f5912-2914">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-2914">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-2915">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-2915">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f5912-2916">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5912-2916">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f5912-2917">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5912-2917">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f5912-2918">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5912-2918">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f5912-2919">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="f5912-2919">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f5912-2920">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5912-2920">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f5912-2921">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="f5912-2921">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-2922">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-2922">Az.Monitor</span></span>
* <span data-ttu-id="f5912-2923">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="f5912-2923">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f5912-2924">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f5912-2924">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f5912-2925">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f5912-2925">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f5912-2926">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f5912-2926">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f5912-2927">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f5912-2927">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f5912-2928">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f5912-2928">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f5912-2929">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f5912-2929">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f5912-2930">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2930">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5912-2931">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2931">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5912-2932">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2932">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5912-2933">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2933">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5912-2934">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5912-2934">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5912-2935">[更多](/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-2935">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f5912-2936">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2936">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-2937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-2937">Az.Network</span></span>
* <span data-ttu-id="f5912-2938">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2938">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f5912-2939">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2939">New cmdlets</span></span>
        - <span data-ttu-id="f5912-2940">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5912-2940">New-AzNatGateway</span></span>
        - <span data-ttu-id="f5912-2941">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5912-2941">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f5912-2942">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5912-2942">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f5912-2943">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5912-2943">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f5912-2944">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2944">Updated cmdlets</span></span>
        - <span data-ttu-id="f5912-2945">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f5912-2945">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f5912-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f5912-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f5912-2947">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f5912-2947">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f5912-2948">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f5912-2948">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f5912-2949">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f5912-2949">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-2950">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-2950">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-2951">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f5912-2951">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f5912-2952">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="f5912-2952">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f5912-2953">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="f5912-2953">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-2954">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2954">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-2955">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="f5912-2955">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f5912-2956">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="f5912-2956">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f5912-2957">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="f5912-2957">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f5912-2958">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="f5912-2958">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f5912-2959">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="f5912-2959">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f5912-2960">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="f5912-2960">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f5912-2961">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f5912-2961">Az.Relay</span></span>
* <span data-ttu-id="f5912-2962">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-2962">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-2963">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-2963">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-2964">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2964">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-2965">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-2965">Az.Storage</span></span>
* <span data-ttu-id="f5912-2966">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="f5912-2966">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f5912-2967">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="f5912-2967">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f5912-2968">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="f5912-2968">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f5912-2969">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2969">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5912-2970">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="f5912-2970">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f5912-2971">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2971">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f5912-2972">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2972">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f5912-2973">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-2973">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-2974">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-2974">Az.Websites</span></span>
* <span data-ttu-id="f5912-2975">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-2975">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f5912-2976">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="f5912-2976">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f5912-2977">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f5912-2977">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-2978">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-2978">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-2979">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-2979">General availability of `Az` module</span></span>
* <span data-ttu-id="f5912-2980">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5912-2980">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5912-2981">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5912-2981">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5912-2982">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2982">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5912-2983">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-2983">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5912-2984">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-2984">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5912-2985">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-2985">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-2986">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-2986">Az.Accounts</span></span>
* <span data-ttu-id="f5912-2987">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="f5912-2987">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5912-2988">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-2988">Az.Batch</span></span>
* <span data-ttu-id="f5912-2989">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-2989">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-2990">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-2990">Az.Cdn</span></span>
* <span data-ttu-id="f5912-2991">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-2991">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-2992">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-2992">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-2993">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-2993">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-2994">Az.Compute</span></span>
* <span data-ttu-id="f5912-2995">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="f5912-2995">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f5912-2996">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-2996">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-2997">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5912-2997">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-2998">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-2998">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-2999">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="f5912-2999">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3000">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3000">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3001">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3001">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5912-3002">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5912-3002">Az.EventGrid</span></span>
* <span data-ttu-id="f5912-3003">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-3003">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-3004">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-3004">Az.EventHub</span></span>
* <span data-ttu-id="f5912-3005">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3005">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5912-3006">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5912-3006">Az.HDInsight</span></span>
* <span data-ttu-id="f5912-3007">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3007">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-3008">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-3008">Az.IotHub</span></span>
* <span data-ttu-id="f5912-3009">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3009">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-3010">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-3010">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-3011">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-3012">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5912-3012">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f5912-3013">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5912-3013">Az.MachineLearning</span></span>
* <span data-ttu-id="f5912-3014">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3014">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f5912-3015">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f5912-3015">Az.Media</span></span>
* <span data-ttu-id="f5912-3016">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-3017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-3017">Az.Monitor</span></span>
  * <span data-ttu-id="f5912-3018">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3018">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f5912-3019">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f5912-3019">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f5912-3020">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f5912-3020">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f5912-3021">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5912-3021">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f5912-3022">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5912-3022">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f5912-3023">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5912-3023">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f5912-3024">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f5912-3024">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3025">Az.Network</span></span>
* <span data-ttu-id="f5912-3026">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-3027">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5912-3027">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f5912-3028">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f5912-3028">Az.NotificationHubs</span></span>
* <span data-ttu-id="f5912-3029">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-3030">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-3030">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-3031">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f5912-3032">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f5912-3032">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f5912-3033">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3033">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3034">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3034">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-3035">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3035">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-3036">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="f5912-3036">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f5912-3037">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="f5912-3037">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f5912-3038">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="f5912-3038">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5912-3039">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5912-3039">Az.RedisCache</span></span>
* <span data-ttu-id="f5912-3040">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3040">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3041">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3041">Az.Resources</span></span>
* <span data-ttu-id="f5912-3042">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5912-3042">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3043">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3043">Az.Sql</span></span>
* <span data-ttu-id="f5912-3044">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-3044">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f5912-3045">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3045">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-3046">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="f5912-3046">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f5912-3047">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="f5912-3047">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f5912-3048">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f5912-3048">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f5912-3049">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-3049">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f5912-3050">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f5912-3050">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3051">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3051">Az.Websites</span></span>
* <span data-ttu-id="f5912-3052">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="f5912-3052">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f5912-3053">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3053">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5912-3054">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="f5912-3054">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f5912-3055">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5912-3055">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f5912-3056">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3056">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-3057">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-3057">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-3058">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-3058">General availability of `Az` module</span></span>
* <span data-ttu-id="f5912-3059">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5912-3059">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5912-3060">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5912-3060">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5912-3061">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3061">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5912-3062">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-3062">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5912-3063">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3063">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5912-3064">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3064">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5912-3065">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3065">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3066">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-3066">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-3067">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3067">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5912-3068">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="f5912-3068">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f5912-3069">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="f5912-3069">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-3070">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3070">Az.Automation</span></span>
* <span data-ttu-id="f5912-3071">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f5912-3071">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f5912-3072">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="f5912-3072">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f5912-3073">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f5912-3073">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3074">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3074">Az.Compute</span></span>
* <span data-ttu-id="f5912-3075">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-3075">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5912-3076">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="f5912-3076">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f5912-3077">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3077">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5912-3078">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="f5912-3078">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-3079">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-3079">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-3080">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f5912-3080">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f5912-3081">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-3081">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3082">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3082">Az.Resources</span></span>
* <span data-ttu-id="f5912-3083">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="f5912-3083">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f5912-3084">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f5912-3084">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f5912-3085">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="f5912-3085">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f5912-3086">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f5912-3086">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f5912-3087">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="f5912-3087">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f5912-3088">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f5912-3088">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3089">Az.Sql</span></span>
* <span data-ttu-id="f5912-3090">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="f5912-3090">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-3091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3091">Az.Storage</span></span>
* <span data-ttu-id="f5912-3092">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="f5912-3092">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f5912-3093">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f5912-3093">New-AzStorageContext</span></span>
* <span data-ttu-id="f5912-3094">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-3094">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f5912-3095">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5912-3095">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f5912-3096">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5912-3096">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f5912-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f5912-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f5912-3099">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3099">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f5912-3100">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5912-3100">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f5912-3101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5912-3101">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f5912-3102">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5912-3102">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f5912-3103">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5912-3103">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f5912-3104">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3104">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5912-3105">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f5912-3105">Highlights since the last major release</span></span>
* <span data-ttu-id="f5912-3106">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f5912-3106">General availability of `Az` module</span></span>
* <span data-ttu-id="f5912-3107">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5912-3107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5912-3108">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5912-3108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5912-3109">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5912-3110">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-3110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5912-3111">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5912-3112">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-3113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3113">Az.Automation</span></span>
* <span data-ttu-id="f5912-3114">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="f5912-3114">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f5912-3115">動態分組</span><span class="sxs-lookup"><span data-stu-id="f5912-3115">Dynamic grouping</span></span>
    * <span data-ttu-id="f5912-3116">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="f5912-3116">Pre-Post script</span></span>
    * <span data-ttu-id="f5912-3117">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="f5912-3117">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3118">Az.Compute</span></span>
* <span data-ttu-id="f5912-3119">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3119">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f5912-3120">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="f5912-3120">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-3121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-3121">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-3122">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3122">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3123">Az.Network</span></span>
* <span data-ttu-id="f5912-3124">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3124">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f5912-3125">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="f5912-3125">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3126">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-3127">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="f5912-3127">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f5912-3128">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3128">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3129">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3129">Az.Resources</span></span>
* <span data-ttu-id="f5912-3130">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3130">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f5912-3131">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="f5912-3131">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3132">Az.Sql</span></span>
* <span data-ttu-id="f5912-3133">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-3133">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-3134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3134">Az.Storage</span></span>
* <span data-ttu-id="f5912-3135">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="f5912-3135">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f5912-3136">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3136">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5912-3137">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3137">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5912-3138">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3138">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5912-3139">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f5912-3139">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f5912-3140">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f5912-3140">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f5912-3141">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f5912-3141">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3142">Az.Websites</span></span>
* <span data-ttu-id="f5912-3143">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="f5912-3143">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f5912-3144">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3144">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-3145">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3145">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3146">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3146">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f5912-3147">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3147">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-3148">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3148">Az.Automation</span></span>
* <span data-ttu-id="f5912-3149">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3149">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f5912-3150">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3150">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f5912-3151">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="f5912-3151">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-3152">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-3152">Az.Cdn</span></span>
* <span data-ttu-id="f5912-3153">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3153">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3154">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3154">Az.Compute</span></span>
* <span data-ttu-id="f5912-3155">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3155">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-3156">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-3156">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-3157">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f5912-3157">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-3158">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-3158">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-3159">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="f5912-3159">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3160">Az.Network</span></span>
* <span data-ttu-id="f5912-3161">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3161">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3162">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-3163">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3163">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f5912-3164">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="f5912-3164">SDK Update</span></span>
* <span data-ttu-id="f5912-3165">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="f5912-3165">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f5912-3166">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="f5912-3166">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3167">Az.Resources</span></span>
* <span data-ttu-id="f5912-3168">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3168">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f5912-3169">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f5912-3169">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f5912-3170">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3170">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f5912-3171">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f5912-3171">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f5912-3172">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3172">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f5912-3173">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f5912-3173">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3174">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3174">Az.Sql</span></span>
* <span data-ttu-id="f5912-3175">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="f5912-3175">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f5912-3176">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="f5912-3176">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-3177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3177">Az.Storage</span></span>
* <span data-ttu-id="f5912-3178">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5912-3178">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f5912-3179">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3179">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-3180">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3180">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5912-3181">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3181">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-3182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3182">Az.Automation</span></span>
* <span data-ttu-id="f5912-3183">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-3183">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f5912-3184">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3184">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f5912-3185">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f5912-3185">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-3186">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3186">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-3187">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="f5912-3187">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3188">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3188">Az.Compute</span></span>
* <span data-ttu-id="f5912-3189">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3189">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f5912-3190">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="f5912-3190">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f5912-3191">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3191">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f5912-3192">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="f5912-3192">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3193">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3193">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3194">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3194">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5912-3195">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5912-3195">Az.EventHub</span></span>
* <span data-ttu-id="f5912-3196">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="f5912-3196">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-3197">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-3197">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-3198">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="f5912-3198">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-3199">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-3199">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-3200">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="f5912-3200">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f5912-3201">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="f5912-3201">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f5912-3202">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3202">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f5912-3203">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5912-3203">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5912-3204">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5912-3204">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5912-3205">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5912-3205">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5912-3206">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5912-3206">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f5912-3207">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3207">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f5912-3208">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-3208">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5912-3209">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-3209">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5912-3210">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-3210">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5912-3211">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-3211">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f5912-3212">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="f5912-3212">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5912-3213">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-3213">Az.Monitor</span></span>
* <span data-ttu-id="f5912-3214">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="f5912-3214">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3215">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3215">Az.Network</span></span>
* <span data-ttu-id="f5912-3216">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3216">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-3217">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-3217">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5912-3218">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-3218">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f5912-3219">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="f5912-3219">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f5912-3220">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="f5912-3220">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3221">Az.Resources</span></span>
* <span data-ttu-id="f5912-3222">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3222">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f5912-3223">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3223">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f5912-3224">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3224">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f5912-3225">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-3225">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3226">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3226">Az.Sql</span></span>
* <span data-ttu-id="f5912-3227">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3227">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f5912-3228">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="f5912-3228">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3229">Az.Websites</span></span>
* <span data-ttu-id="f5912-3230">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3230">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f5912-3231">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3231">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-3232">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3232">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3233">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5912-3233">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-3234">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3234">Az.AnalysisServices</span></span>
<span data-ttu-id="f5912-3235">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="f5912-3235">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3236">Az.Compute</span></span>
* <span data-ttu-id="f5912-3237">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3237">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f5912-3238">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="f5912-3238">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f5912-3239">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3239">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3240">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3240">Az.RecoveryServices</span></span>
<span data-ttu-id="f5912-3241">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="f5912-3241">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3242">Az.Resources</span></span>
* <span data-ttu-id="f5912-3243">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="f5912-3243">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f5912-3244">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f5912-3244">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f5912-3245">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3245">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f5912-3246">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f5912-3246">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3247">Az.Sql</span></span>
* <span data-ttu-id="f5912-3248">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5912-3248">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f5912-3249">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3249">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f5912-3250">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="f5912-3250">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f5912-3251">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3251">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-3252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3252">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3253">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="f5912-3253">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5912-3254">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3254">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5912-3255">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="f5912-3255">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3256">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5912-3257">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="f5912-3257">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f5912-3258">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3258">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-3259">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3259">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3260">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f5912-3260">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5912-3261">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5912-3262">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-3262">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5912-3263">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5912-3263">Az.Aks</span></span>
* <span data-ttu-id="f5912-3264">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3264">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5912-3265">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3265">Az.Automation</span></span>
* <span data-ttu-id="f5912-3266">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3266">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f5912-3267">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3267">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5912-3268">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5912-3268">Az.Cdn</span></span>
* <span data-ttu-id="f5912-3269">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3269">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3270">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3270">Az.Compute</span></span>
* <span data-ttu-id="f5912-3271">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3271">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f5912-3272">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f5912-3272">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f5912-3273">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-3273">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5912-3274">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5912-3274">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5912-3275">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3275">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5912-3276">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5912-3276">Az.DataFactory</span></span>
* <span data-ttu-id="f5912-3277">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f5912-3277">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3278">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3278">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3279">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3279">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f5912-3280">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f5912-3280">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f5912-3281">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3281">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-3282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-3282">Az.IotHub</span></span>
* <span data-ttu-id="f5912-3283">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-3283">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5912-3284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-3284">Az.KeyVault</span></span>
* <span data-ttu-id="f5912-3285">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3285">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3286">Az.Network</span></span>
* <span data-ttu-id="f5912-3287">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3287">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3288">Az.Resources</span></span>
* <span data-ttu-id="f5912-3289">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3289">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f5912-3290">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3290">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f5912-3291">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="f5912-3291">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f5912-3292">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3292">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f5912-3293">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3293">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f5912-3294">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3294">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f5912-3295">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f5912-3295">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-3296">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-3296">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-3297">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f5912-3297">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f5912-3298">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-3298">Fix some error messages.</span></span>
* <span data-ttu-id="f5912-3299">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3299">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f5912-3300">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3300">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5912-3301">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5912-3301">Az.SignalR</span></span>
* <span data-ttu-id="f5912-3302">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3302">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3303">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3303">Az.Sql</span></span>
* <span data-ttu-id="f5912-3304">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3304">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5912-3305">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="f5912-3305">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f5912-3306">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3306">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f5912-3307">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="f5912-3307">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-3308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3308">Az.Storage</span></span>
* <span data-ttu-id="f5912-3309">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3309">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5912-3310">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="f5912-3310">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f5912-3311">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f5912-3311">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f5912-3312">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f5912-3312">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f5912-3313">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f5912-3313">Az.TrafficManager</span></span>
* <span data-ttu-id="f5912-3314">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3314">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3315">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3315">Az.Websites</span></span>
* <span data-ttu-id="f5912-3316">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3316">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5912-3317">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="f5912-3317">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f5912-3318">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="f5912-3318">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f5912-3319">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3319">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5912-3320">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3320">Az.Accounts</span></span>
* <span data-ttu-id="f5912-3321">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f5912-3321">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3322">Az.Compute</span></span>
* <span data-ttu-id="f5912-3323">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="f5912-3323">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f5912-3324">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="f5912-3324">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f5912-3325">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3325">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3326">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3326">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3327">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3327">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f5912-3328">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="f5912-3328">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5912-3329">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5912-3329">Az.EventGrid</span></span>
* <span data-ttu-id="f5912-3330">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f5912-3330">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f5912-3331">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="f5912-3331">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f5912-3332">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f5912-3332">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f5912-3333">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="f5912-3333">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f5912-3334">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="f5912-3334">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f5912-3335">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="f5912-3335">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f5912-3336">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f5912-3336">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f5912-3337">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="f5912-3337">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f5912-3338">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="f5912-3338">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f5912-3339">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="f5912-3339">Dead letter endpoint.</span></span>
* <span data-ttu-id="f5912-3340">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="f5912-3340">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f5912-3341">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-3341">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5912-3342">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5912-3342">Az.IotHub</span></span>
* <span data-ttu-id="f5912-3343">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="f5912-3343">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5912-3344">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5912-3344">Az.LogicApp</span></span>
* <span data-ttu-id="f5912-3345">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-3345">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3346">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3346">Az.Resources</span></span>
* <span data-ttu-id="f5912-3347">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3347">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f5912-3348">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f5912-3348">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f5912-3349">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="f5912-3349">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f5912-3350">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-3350">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f5912-3351">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="f5912-3351">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f5912-3352">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f5912-3352">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5912-3353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5912-3353">Az.SignalR</span></span>
* <span data-ttu-id="f5912-3354">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3354">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3355">Az.Sql</span></span>
* <span data-ttu-id="f5912-3356">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="f5912-3356">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5912-3357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3357">Az.Storage</span></span>
* <span data-ttu-id="f5912-3358">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-3358">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f5912-3359">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f5912-3359">New-AzStorageContext</span></span>
* <span data-ttu-id="f5912-3360">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="f5912-3360">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f5912-3361">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5912-3361">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3362">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3362">Az.Websites</span></span>
* <span data-ttu-id="f5912-3363">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="f5912-3363">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f5912-3364">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3364">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f5912-3365">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3365">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f5912-3366">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-3366">General</span></span>

- <span data-ttu-id="f5912-3367">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="f5912-3367">General Availability of Az Module</span></span>
- <span data-ttu-id="f5912-3368">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="f5912-3368">Online help for each module</span></span>
- <span data-ttu-id="f5912-3369">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f5912-3369">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f5912-3370">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3370">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f5912-3371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3371">Az.Accounts</span></span>
- <span data-ttu-id="f5912-3372">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="f5912-3372">Changed from Az.Profile</span></span>
- <span data-ttu-id="f5912-3373">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="f5912-3373">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5912-3374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-3374">Az.ApiManagement</span></span>
- <span data-ttu-id="f5912-3375">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="f5912-3375">Fixes for #7002</span></span>
- <span data-ttu-id="f5912-3376">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3376">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f5912-3377">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5912-3377">Az.Batch</span></span>
- <span data-ttu-id="f5912-3378">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="f5912-3378">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f5912-3379">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="f5912-3379">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f5912-3380">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f5912-3381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5912-3381">Az.Billing</span></span>
- <span data-ttu-id="f5912-3382">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3382">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f5912-3383">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3383">Az.CognitivServices</span></span>
- <span data-ttu-id="f5912-3384">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="f5912-3384">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f5912-3385">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="f5912-3385">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5912-3386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3386">Az.ContainerInstance</span></span>
- <span data-ttu-id="f5912-3387">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3387">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f5912-3388">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f5912-3388">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f5912-3389">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3389">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3390">Az.DataLakeStore</span></span>
- <span data-ttu-id="f5912-3391">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f5912-3392">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5912-3392">Az.Monitor</span></span>
- <span data-ttu-id="f5912-3393">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3393">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f5912-3394">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5912-3394">Az.KeyVault</span></span>
- <span data-ttu-id="f5912-3395">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="f5912-3395">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f5912-3396">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5912-3396">Az.MachineLearning</span></span>
- <span data-ttu-id="f5912-3397">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3397">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f5912-3398">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f5912-3398">Az.Media</span></span>
- <span data-ttu-id="f5912-3399">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="f5912-3399">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5912-3400">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3400">Az.Network</span></span>
<span data-ttu-id="f5912-3401">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3401">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f5912-3402">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f5912-3402">New cmdlets added:</span></span>
        - <span data-ttu-id="f5912-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3408">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f5912-3408">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f5912-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f5912-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5912-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f5912-3411">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5912-3411">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f5912-3412">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5912-3412">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f5912-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5912-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5912-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5912-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5912-3415">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-3415">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f5912-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f5912-3417">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-3417">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f5912-3418">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3418">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f5912-3419">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5912-3419">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5912-3420">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5912-3420">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5912-3421">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5912-3421">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f5912-3422">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3422">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f5912-3423">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3423">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f5912-3424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-3424">Az.OperationalInsights</span></span>
- <span data-ttu-id="f5912-3425">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f5912-3426">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5912-3426">Az.Profile</span></span>
- <span data-ttu-id="f5912-3427">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5912-3427">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3428">Az.RecoveryServices</span></span>
- <span data-ttu-id="f5912-3429">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3429">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f5912-3430">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3430">Az.Resources</span></span>
- <span data-ttu-id="f5912-3431">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3431">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5912-3432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-3432">Az.ServiceFabric</span></span>
- <span data-ttu-id="f5912-3433">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="f5912-3433">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f5912-3434">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3434">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f5912-3435">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f5912-3435">Az.SIgnalR</span></span>
- <span data-ttu-id="f5912-3436">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="f5912-3436">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f5912-3437">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3437">Az.Sql</span></span>
- <span data-ttu-id="f5912-3438">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="f5912-3438">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f5912-3439">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3439">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f5912-3440">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5912-3441">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3441">Az.Storage</span></span>
- <span data-ttu-id="f5912-3442">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3442">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5912-3443">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3443">Az.Websites</span></span>
- <span data-ttu-id="f5912-3444">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5912-3444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f5912-3445">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3445">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f5912-3446">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-3446">General</span></span>

* <span data-ttu-id="f5912-3447">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="f5912-3447">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5912-3448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3448">Az.Compute</span></span>

* <span data-ttu-id="f5912-3449">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="f5912-3449">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3450">Az.DataLakeStore</span></span>

* <span data-ttu-id="f5912-3451">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="f5912-3451">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f5912-3452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5912-3452">Az.FrontDoor</span></span>

* <span data-ttu-id="f5912-3453">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="f5912-3453">Fixed some broken links</span></span>
    - <span data-ttu-id="f5912-3454">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="f5912-3454">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f5912-3455">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="f5912-3455">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5912-3456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3456">Az.RecoveryServices</span></span>

* <span data-ttu-id="f5912-3457">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-3457">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f5912-3458">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="f5912-3458">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5912-3459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3459">Az.Resources</span></span>

* <span data-ttu-id="f5912-3460">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f5912-3460">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f5912-3461">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="f5912-3461">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f5912-3462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3462">Az.Sql</span></span>

* <span data-ttu-id="f5912-3463">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="f5912-3463">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f5912-3464">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3464">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f5912-3465">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="f5912-3465">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5912-3466">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3466">Az.Storage</span></span>

* <span data-ttu-id="f5912-3467">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="f5912-3467">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f5912-3468">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="f5912-3468">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f5912-3469">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5912-3469">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5912-3470">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="f5912-3470">Support Static Website configuration</span></span>
    - <span data-ttu-id="f5912-3471">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5912-3471">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f5912-3472">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5912-3472">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5912-3473">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3473">Az.Websites</span></span>

* <span data-ttu-id="f5912-3474">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5912-3474">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f5912-3475">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="f5912-3475">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f5912-3476">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="f5912-3476">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f5912-3477">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3477">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5912-3478">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5912-3478">Az.ApiManagement</span></span>
* <span data-ttu-id="f5912-3479">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-3479">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f5912-3480">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5912-3480">Az.Automation</span></span>
* <span data-ttu-id="f5912-3481">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3481">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f5912-3482">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3482">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f5912-3483">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3483">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f5912-3484">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3484">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f5912-3485">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="f5912-3485">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5912-3486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3486">Az.Compute</span></span>
* <span data-ttu-id="f5912-3487">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3487">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f5912-3488">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-3488">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5912-3489">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3489">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5912-3490">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-3490">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f5912-3491">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f5912-3491">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f5912-3492">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="f5912-3492">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5912-3493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3493">Az.Network</span></span>
* <span data-ttu-id="f5912-3494">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f5912-3494">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f5912-3495">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="f5912-3495">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f5912-3496">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="f5912-3496">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f5912-3497">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3497">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f5912-3498">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f5912-3498">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f5912-3499">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="f5912-3499">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f5912-3500">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="f5912-3500">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f5912-3501">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f5912-3501">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f5912-3502">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3502">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f5912-3503">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f5912-3503">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f5912-3504">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f5912-3504">Az.Relay</span></span>
* <span data-ttu-id="f5912-3505">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="f5912-3505">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5912-3506">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3506">Az.Resources</span></span>
* <span data-ttu-id="f5912-3507">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="f5912-3507">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f5912-3508">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="f5912-3508">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f5912-3509">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="f5912-3509">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5912-3510">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-3510">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-3511">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="f5912-3511">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f5912-3512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3512">Az.Sql</span></span>
* <span data-ttu-id="f5912-3513">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3513">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f5912-3514">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3514">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5912-3515">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3515">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5912-3516">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3516">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5912-3517">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5912-3517">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5912-3518">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5912-3518">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5912-3519">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5912-3519">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5912-3520">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5912-3520">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5912-3521">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5912-3521">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f5912-3522">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="f5912-3522">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f5912-3523">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="f5912-3523">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f5912-3524">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="f5912-3524">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f5912-3525">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="f5912-3525">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5912-3526">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="f5912-3526">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5912-3527">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="f5912-3527">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f5912-3528">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="f5912-3528">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f5912-3529">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3529">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f5912-3530">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3530">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f5912-3531">一般</span><span class="sxs-lookup"><span data-stu-id="f5912-3531">General</span></span>
* <span data-ttu-id="f5912-3532">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="f5912-3532">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f5912-3533">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5912-3533">Az.Profile</span></span>
* <span data-ttu-id="f5912-3534">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5912-3534">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f5912-3535">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="f5912-3535">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f5912-3536">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="f5912-3536">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f5912-3537">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f5912-3537">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f5912-3538">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3538">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f5912-3539">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3539">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f5912-3540">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3540">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-3541">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3541">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-3542">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="f5912-3542">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3543">Az.Compute</span></span>
* <span data-ttu-id="f5912-3544">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3544">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f5912-3545">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f5912-3545">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f5912-3546">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3546">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3547">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3547">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3548">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="f5912-3548">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f5912-3549">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="f5912-3549">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f5912-3550">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f5912-3550">Az.Insights</span></span>
* <span data-ttu-id="f5912-3551">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="f5912-3551">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f5912-3552">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3552">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f5912-3553">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="f5912-3553">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f5912-3554">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="f5912-3554">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3555">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3555">Az.Network</span></span>
* <span data-ttu-id="f5912-3556">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="f5912-3556">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f5912-3557">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-3557">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f5912-3558">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f5912-3558">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f5912-3559">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5912-3559">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f5912-3560">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f5912-3560">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f5912-3561">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5912-3561">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f5912-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5912-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5912-3563">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5912-3563">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5912-3564">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3564">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3565">Az.Resources</span></span>
* <span data-ttu-id="f5912-3566">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f5912-3566">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f5912-3567">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="f5912-3567">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5912-3568">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5912-3568">Az.ServiceBus</span></span>
* <span data-ttu-id="f5912-3569">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="f5912-3569">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5912-3570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5912-3570">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5912-3571">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="f5912-3571">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f5912-3572">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5912-3572">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f5912-3573">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="f5912-3573">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f5912-3574">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="f5912-3574">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f5912-3575">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="f5912-3575">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f5912-3576">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3576">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f5912-3577">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5912-3577">Az.Profile</span></span>
* <span data-ttu-id="f5912-3578">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3578">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f5912-3579">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5912-3579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3580">Az.Compute</span></span>
* <span data-ttu-id="f5912-3581">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="f5912-3581">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f5912-3582">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-3582">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5912-3583">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5912-3583">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5912-3584">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="f5912-3584">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f5912-3585">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f5912-3585">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f5912-3586">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5912-3586">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5912-3587">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f5912-3587">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5912-3588">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f5912-3588">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3589">Az.Network</span></span>
* <span data-ttu-id="f5912-3590">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="f5912-3590">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f5912-3591">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5912-3591">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3592">Az.Resources</span></span>
* <span data-ttu-id="f5912-3593">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="f5912-3593">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f5912-3594">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="f5912-3594">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f5912-3595">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3595">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f5912-3596">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f5912-3596">Azure.Storage</span></span>
* <span data-ttu-id="f5912-3597">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3597">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f5912-3598">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5912-3598">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f5912-3599">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5912-3599">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5912-3600">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f5912-3600">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f5912-3601">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f5912-3601">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5912-3602">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5912-3602">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5912-3603">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="f5912-3603">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5912-3604">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5912-3604">Az.Compute</span></span>
* <span data-ttu-id="f5912-3605">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="f5912-3605">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f5912-3606">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="f5912-3606">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f5912-3607">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f5912-3607">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f5912-3608">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5912-3608">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f5912-3609">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="f5912-3609">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5912-3610">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5912-3610">Az.Network</span></span>
* <span data-ttu-id="f5912-3611">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="f5912-3611">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f5912-3612">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3612">new cmdlets added</span></span>
    - <span data-ttu-id="f5912-3613">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5912-3613">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5912-3614">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5912-3614">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5912-3615">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5912-3615">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5912-3616">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5912-3616">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5912-3617">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-3617">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f5912-3618">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5912-3618">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f5912-3619">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="f5912-3619">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f5912-3620">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3620">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f5912-3621">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5912-3621">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5912-3622">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5912-3622">Az.RedisCache</span></span>
* <span data-ttu-id="f5912-3623">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="f5912-3623">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f5912-3624">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="f5912-3624">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5912-3625">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5912-3625">Az.Resources</span></span>
* <span data-ttu-id="f5912-3626">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5912-3626">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f5912-3627">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="f5912-3627">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5912-3628">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5912-3628">Az.Sql</span></span>
* <span data-ttu-id="f5912-3629">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="f5912-3629">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5912-3630">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5912-3630">Az.Websites</span></span>
* <span data-ttu-id="f5912-3631">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="f5912-3631">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f5912-3632">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="f5912-3632">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f5912-3633">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="f5912-3633">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f5912-3634">初始版本</span><span class="sxs-lookup"><span data-stu-id="f5912-3634">Initial Release</span></span>
