---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002668"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ca0ab-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="ca0ab-104">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca0ab-105">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-105">Highlights since the last major release</span></span>
* <span data-ttu-id="ca0ab-106">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="ca0ab-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="ca0ab-107">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="ca0ab-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-108">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-109">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="ca0ab-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="ca0ab-110">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="ca0ab-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-111">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-112">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="ca0ab-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="ca0ab-113">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="ca0ab-114">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="ca0ab-115">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="ca0ab-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-116">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-117">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="ca0ab-118">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="ca0ab-119">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-120">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="ca0ab-121">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-122">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-123">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ca0ab-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ca0ab-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="ca0ab-125">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="ca0ab-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="ca0ab-126">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="ca0ab-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-127">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-128">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-129">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-130">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-131">Az.Network</span></span>
* <span data-ttu-id="ca0ab-132">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="ca0ab-133">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="ca0ab-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="ca0ab-134">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-135">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="ca0ab-136">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="ca0ab-137">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="ca0ab-138">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="ca0ab-139">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="ca0ab-140">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-140">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="ca0ab-142">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="ca0ab-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="ca0ab-144">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca0ab-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca0ab-146">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="ca0ab-147">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="ca0ab-148">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="ca0ab-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="ca0ab-149">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ca0ab-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-151">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="ca0ab-152">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-153">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-154">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="ca0ab-155">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-156">Az.Sql</span></span>
<span data-ttu-id="ca0ab-157">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-158">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-159">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="ca0ab-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="ca0ab-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="ca0ab-161">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="ca0ab-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="ca0ab-162">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="ca0ab-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-163">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-164">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="ca0ab-165">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="ca0ab-166">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-167">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-168">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-169">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-170">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="ca0ab-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-171">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-172">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ca0ab-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="ca0ab-174">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ca0ab-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ca0ab-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ca0ab-176">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ca0ab-177">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ca0ab-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="ca0ab-178">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ca0ab-179">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ca0ab-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="ca0ab-180">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ca0ab-181">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="ca0ab-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="ca0ab-182">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ca0ab-183">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="ca0ab-184">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ca0ab-185">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ca0ab-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="ca0ab-186">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ca0ab-187">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ca0ab-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="ca0ab-188">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ca0ab-189">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ca0ab-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="ca0ab-190">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="ca0ab-191">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="ca0ab-192">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="ca0ab-193">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-194">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-195">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="ca0ab-196">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="ca0ab-197">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="ca0ab-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ca0ab-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="ca0ab-199">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="ca0ab-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-200">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-201">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="ca0ab-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-202">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-203">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ca0ab-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca0ab-204">Az.MachineLearning</span></span>
* <span data-ttu-id="ca0ab-205">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="ca0ab-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ca0ab-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="ca0ab-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="ca0ab-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ca0ab-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="ca0ab-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ca0ab-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="ca0ab-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ca0ab-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="ca0ab-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ca0ab-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="ca0ab-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-213">Az.Network</span></span>
* <span data-ttu-id="ca0ab-214">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="ca0ab-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-216">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="ca0ab-217">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ca0ab-218">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ca0ab-219">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-220">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-221">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-222">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-223">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="ca0ab-224">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ca0ab-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ca0ab-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ca0ab-226">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-227">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-228">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="ca0ab-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="ca0ab-230">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="ca0ab-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="ca0ab-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="ca0ab-232">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="ca0ab-233">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-233">General</span></span>
* <span data-ttu-id="ca0ab-234">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="ca0ab-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-235">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-236">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="ca0ab-237">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca0ab-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-238">Az.Batch</span></span>
* <span data-ttu-id="ca0ab-239">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-240">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-241">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-242">Az.FrontDoor</span></span>
* <span data-ttu-id="ca0ab-243">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="ca0ab-244">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="ca0ab-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ca0ab-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ca0ab-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="ca0ab-246">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-247">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-248">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="ca0ab-249">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="ca0ab-250">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-251">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-252">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="ca0ab-253">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="ca0ab-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="ca0ab-254">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-255">Az.Network</span></span>
* <span data-ttu-id="ca0ab-256">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-257">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-258">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="ca0ab-259">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-260">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-261">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-262">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-263">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="ca0ab-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="ca0ab-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ca0ab-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="ca0ab-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca0ab-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="ca0ab-266">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="ca0ab-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="ca0ab-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="ca0ab-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="ca0ab-268">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="ca0ab-269">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="ca0ab-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="ca0ab-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="ca0ab-272">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="ca0ab-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ca0ab-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="ca0ab-274">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="ca0ab-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ca0ab-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="ca0ab-276">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca0ab-277">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-277">Highlights since the last major release</span></span>
* <span data-ttu-id="ca0ab-278">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="ca0ab-279">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-280">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-281">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="ca0ab-281">VM Reapply feature</span></span>
    - <span data-ttu-id="ca0ab-282">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="ca0ab-283">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="ca0ab-284">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca0ab-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="ca0ab-285">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="ca0ab-286">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ca0ab-287">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="ca0ab-288">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="ca0ab-289">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="ca0ab-290">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="ca0ab-291">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ca0ab-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ca0ab-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ca0ab-293">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ca0ab-294">取得訂單</span><span class="sxs-lookup"><span data-stu-id="ca0ab-294">Get the Order</span></span>
* <span data-ttu-id="ca0ab-295">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ca0ab-296">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="ca0ab-296">Create new Order</span></span>
* <span data-ttu-id="ca0ab-297">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ca0ab-298">移除訂單</span><span class="sxs-lookup"><span data-stu-id="ca0ab-298">Remove the Order</span></span>
* <span data-ttu-id="ca0ab-299">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="ca0ab-300">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="ca0ab-300">Now creates Local Share</span></span>
* <span data-ttu-id="ca0ab-301">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="ca0ab-302">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="ca0ab-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="ca0ab-303">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="ca0ab-304">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="ca0ab-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="ca0ab-305">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ca0ab-306">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="ca0ab-307">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ca0ab-308">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="ca0ab-308">Create new Triggers</span></span>
* <span data-ttu-id="ca0ab-309">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="ca0ab-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ca0ab-310">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="ca0ab-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-311">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-312">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="ca0ab-313">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-315">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-316">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-317">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-318">Az.FrontDoor</span></span>
* <span data-ttu-id="ca0ab-319">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="ca0ab-320">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="ca0ab-321">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="ca0ab-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="ca0ab-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-323">Az.Network</span></span>
* <span data-ttu-id="ca0ab-324">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="ca0ab-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="ca0ab-325">Az.PrivateDns</span></span>
* <span data-ttu-id="ca0ab-326">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="ca0ab-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-328">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="ca0ab-329">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="ca0ab-330">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="ca0ab-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca0ab-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca0ab-331">Az.RedisCache</span></span>
* <span data-ttu-id="ca0ab-332">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="ca0ab-333">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="ca0ab-334">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-335">Az.Resources</span></span>
- <span data-ttu-id="ca0ab-336">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="ca0ab-337">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="ca0ab-338">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="ca0ab-339">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="ca0ab-340">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-341">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-342">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="ca0ab-343">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ca0ab-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="ca0ab-344">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="ca0ab-345">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-345">General</span></span>
* <span data-ttu-id="ca0ab-346">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-347">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-348">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ca0ab-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-349">Az.Advisor</span></span>
* <span data-ttu-id="ca0ab-350">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca0ab-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-351">Az.Batch</span></span>
* <span data-ttu-id="ca0ab-352">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="ca0ab-353">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="ca0ab-354">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="ca0ab-355">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="ca0ab-356">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="ca0ab-357">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="ca0ab-358">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="ca0ab-359">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="ca0ab-360">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="ca0ab-361">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ca0ab-362">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="ca0ab-363">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="ca0ab-364">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ca0ab-365">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="ca0ab-366">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="ca0ab-367">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="ca0ab-368">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="ca0ab-369">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="ca0ab-370">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="ca0ab-371">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="ca0ab-372">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ca0ab-373">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ca0ab-374">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="ca0ab-375">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="ca0ab-376">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="ca0ab-377">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="ca0ab-378">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="ca0ab-379">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="ca0ab-380">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="ca0ab-381">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="ca0ab-382">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="ca0ab-383">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="ca0ab-384">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="ca0ab-385">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="ca0ab-386">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="ca0ab-387">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-388">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-389">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="ca0ab-390">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-391">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-392">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="ca0ab-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="ca0ab-393">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="ca0ab-394">DiskEncryptionSetId 參數已新增至下列 Cmdlet：Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="ca0ab-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca0ab-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="ca0ab-396">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ca0ab-397">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="ca0ab-398">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="ca0ab-399">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="ca0ab-400">重大變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-400">Breaking changes</span></span>
    - <span data-ttu-id="ca0ab-401">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ca0ab-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="ca0ab-402">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="ca0ab-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-403">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-404">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-406">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="ca0ab-407">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="ca0ab-408">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="ca0ab-409">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="ca0ab-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="ca0ab-410">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="ca0ab-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="ca0ab-411">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-412">Az.FrontDoor</span></span>
* <span data-ttu-id="ca0ab-413">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-414">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-415">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="ca0ab-416">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="ca0ab-417">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="ca0ab-418">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ca0ab-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ca0ab-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ca0ab-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ca0ab-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ca0ab-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ca0ab-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca0ab-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="ca0ab-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca0ab-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="ca0ab-424">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-425">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ca0ab-426">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ca0ab-427">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="ca0ab-428">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="ca0ab-429">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="ca0ab-430">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="ca0ab-431">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="ca0ab-432">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="ca0ab-433">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="ca0ab-434">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="ca0ab-435">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="ca0ab-436">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="ca0ab-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-437">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-438">重大變更：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-438">Breaking changes:</span></span>
    - <span data-ttu-id="ca0ab-439">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ca0ab-440">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ca0ab-441">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ca0ab-442">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ca0ab-443">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="ca0ab-444">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="ca0ab-445">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="ca0ab-446">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="ca0ab-447">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ca0ab-448">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ca0ab-449">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ca0ab-450">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-452">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-453">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="ca0ab-454">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="ca0ab-455">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-456">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-457">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-458">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-459">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-460">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="ca0ab-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-461">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-462">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-463">Az.Network</span></span>
* <span data-ttu-id="ca0ab-464">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="ca0ab-465">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ca0ab-471">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="ca0ab-472">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-472">New cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ca0ab-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="ca0ab-474">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="ca0ab-475">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="ca0ab-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="ca0ab-476">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="ca0ab-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="ca0ab-477">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="ca0ab-478">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="ca0ab-479">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="ca0ab-480">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="ca0ab-481">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-481">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="ca0ab-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ca0ab-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ca0ab-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ca0ab-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="ca0ab-487">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="ca0ab-488">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ca0ab-489">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="ca0ab-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ca0ab-490">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="ca0ab-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ca0ab-491">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="ca0ab-492">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="ca0ab-493">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="ca0ab-494">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-494">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="ca0ab-496">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ca0ab-497">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ca0ab-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ca0ab-498">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ca0ab-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ca0ab-499">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ca0ab-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ca0ab-500">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ca0ab-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ca0ab-501">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ca0ab-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="ca0ab-502">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="ca0ab-503">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-503">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="ca0ab-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="ca0ab-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="ca0ab-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="ca0ab-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ca0ab-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="ca0ab-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ca0ab-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="ca0ab-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="ca0ab-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="ca0ab-510">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ca0ab-511">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="ca0ab-512">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="ca0ab-513">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="ca0ab-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="ca0ab-514">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="ca0ab-515">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ca0ab-516">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ca0ab-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="ca0ab-517">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ca0ab-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="ca0ab-518">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="ca0ab-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="ca0ab-519">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="ca0ab-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="ca0ab-520">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="ca0ab-521">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-521">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="ca0ab-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="ca0ab-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="ca0ab-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-527">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-528">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-529">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="ca0ab-530">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="ca0ab-531">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="ca0ab-532">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="ca0ab-533">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="ca0ab-534">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ca0ab-535">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="ca0ab-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="ca0ab-536">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="ca0ab-537">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-538">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-539">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="ca0ab-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="ca0ab-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ca0ab-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ca0ab-542">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="ca0ab-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="ca0ab-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca0ab-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="ca0ab-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca0ab-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="ca0ab-545">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ca0ab-546">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-546">General</span></span>
* <span data-ttu-id="ca0ab-547">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-548">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-549">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-550">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-551">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ca0ab-552">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-553">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-554">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="ca0ab-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-555">Az.Batch</span></span>
* <span data-ttu-id="ca0ab-556">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-557">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-558">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ca0ab-559">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ca0ab-560">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="ca0ab-561">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-562">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-563">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ca0ab-564">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ca0ab-565">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-567">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="ca0ab-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ca0ab-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ca0ab-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="ca0ab-569">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ca0ab-570">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ca0ab-571">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ca0ab-572">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-573">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-574">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ca0ab-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ca0ab-575">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca0ab-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-576">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-577">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ca0ab-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ca0ab-578">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ca0ab-579">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="ca0ab-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ca0ab-580">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-581">Az.Network</span></span>
* <span data-ttu-id="ca0ab-582">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ca0ab-583">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ca0ab-584">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-584">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ca0ab-586">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ca0ab-587">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ca0ab-588">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="ca0ab-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca0ab-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca0ab-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ca0ab-592">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ca0ab-593">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="ca0ab-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ca0ab-594">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ca0ab-595">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca0ab-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca0ab-596">Az.RedisCache</span></span>
* <span data-ttu-id="ca0ab-597">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="ca0ab-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-598">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-599">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-600">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-601">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ca0ab-602">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="ca0ab-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ca0ab-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ca0ab-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ca0ab-604">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="ca0ab-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ca0ab-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ca0ab-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ca0ab-606">Az.StorageSync</span></span>
* <span data-ttu-id="ca0ab-607">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-608">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-609">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="ca0ab-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ca0ab-610">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-611">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-612">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ca0ab-613">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ca0ab-614">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-615">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-616">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ca0ab-617">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ca0ab-618">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-619">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-620">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ca0ab-621">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ca0ab-622">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ca0ab-623">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ca0ab-624">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ca0ab-625">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ca0ab-626">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ca0ab-627">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ca0ab-628">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-629">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-630">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ca0ab-631">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ca0ab-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-632">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-633">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-634">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-635">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ca0ab-636">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ca0ab-637">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-637">New cmdlets are:</span></span>
    - <span data-ttu-id="ca0ab-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca0ab-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca0ab-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca0ab-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca0ab-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca0ab-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ca0ab-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ca0ab-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-642">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-643">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="ca0ab-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ca0ab-644">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ca0ab-645">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ca0ab-646">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ca0ab-647">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ca0ab-648">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ca0ab-649">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ca0ab-650">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ca0ab-651">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ca0ab-652">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ca0ab-653">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ca0ab-654">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ca0ab-655">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ca0ab-656">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ca0ab-657">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ca0ab-658">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="ca0ab-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ca0ab-659">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ca0ab-660">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ca0ab-661">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ca0ab-662">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="ca0ab-662">Overall improved help files</span></span>
* <span data-ttu-id="ca0ab-663">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-664">Az.Network</span></span>
* <span data-ttu-id="ca0ab-665">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="ca0ab-666">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ca0ab-667">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="ca0ab-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ca0ab-668">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ca0ab-669">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ca0ab-670">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="ca0ab-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ca0ab-671">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="ca0ab-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ca0ab-672">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ca0ab-673">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ca0ab-674">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ca0ab-675">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ca0ab-676">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="ca0ab-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ca0ab-677">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-677">New cmdlets</span></span>
        - <span data-ttu-id="ca0ab-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ca0ab-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ca0ab-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ca0ab-680">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ca0ab-681">New-VpnSite</span></span>
        - <span data-ttu-id="ca0ab-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ca0ab-682">Update-VpnSite</span></span>
        - <span data-ttu-id="ca0ab-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-683">New-VpnConnection</span></span>
        - <span data-ttu-id="ca0ab-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-684">Update-VpnConnection</span></span>
* <span data-ttu-id="ca0ab-685">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-687">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ca0ab-688">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="ca0ab-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-689">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-690">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-692">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ca0ab-693">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ca0ab-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca0ab-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca0ab-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca0ab-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca0ab-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca0ab-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ca0ab-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca0ab-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca0ab-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca0ab-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca0ab-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca0ab-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca0ab-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca0ab-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ca0ab-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ca0ab-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ca0ab-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ca0ab-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ca0ab-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ca0ab-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ca0ab-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ca0ab-707">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca0ab-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca0ab-708">Az.SignalR</span></span>
* <span data-ttu-id="ca0ab-709">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-710">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-711">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ca0ab-712">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ca0ab-713">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="ca0ab-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ca0ab-714">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ca0ab-715">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-716">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-717">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ca0ab-718">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ca0ab-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ca0ab-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ca0ab-721">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ca0ab-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ca0ab-723">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="ca0ab-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ca0ab-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca0ab-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca0ab-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ca0ab-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ca0ab-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-728">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-729">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ca0ab-730">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ca0ab-731">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ca0ab-732">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ca0ab-733">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-733">General</span></span>
* <span data-ttu-id="ca0ab-734">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-735">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-736">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ca0ab-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ca0ab-737">Az.Aks</span></span>
* <span data-ttu-id="ca0ab-738">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ca0ab-739">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ca0ab-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-740">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-741">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ca0ab-742">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="ca0ab-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ca0ab-743">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ca0ab-744">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ca0ab-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ca0ab-745">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca0ab-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-746">Az.Batch</span></span>
* <span data-ttu-id="ca0ab-747">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="ca0ab-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-748">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-749">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-750">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-751">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ca0ab-752">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="ca0ab-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ca0ab-753">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="ca0ab-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ca0ab-754">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="ca0ab-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ca0ab-755">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ca0ab-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ca0ab-756">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="ca0ab-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ca0ab-757">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ca0ab-758">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-759">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-760">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="ca0ab-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ca0ab-761">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ca0ab-762">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ca0ab-763">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-765">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-766">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-767">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ca0ab-768">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="ca0ab-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ca0ab-769">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ca0ab-770">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ca0ab-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ca0ab-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ca0ab-772">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-773">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-774">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-775">Az.Network</span></span>
* <span data-ttu-id="ca0ab-776">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ca0ab-777">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ca0ab-778">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ca0ab-779">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ca0ab-780">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="ca0ab-781">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ca0ab-782">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-784">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ca0ab-785">新增了範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-785">Added example</span></span>
    - <span data-ttu-id="ca0ab-786">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ca0ab-787">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ca0ab-788">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-790">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-791">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-792">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ca0ab-793">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ca0ab-794">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="ca0ab-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ca0ab-795">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-796">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-797">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ca0ab-798">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ca0ab-799">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-801">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ca0ab-802">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ca0ab-803">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ca0ab-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ca0ab-804">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ca0ab-805">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ca0ab-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ca0ab-806">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-807">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-808">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-809">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-810">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ca0ab-811">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="ca0ab-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ca0ab-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ca0ab-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ca0ab-814">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="ca0ab-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ca0ab-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-816">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-817">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="ca0ab-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ca0ab-818">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-819">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-820">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca0ab-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ca0ab-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ca0ab-822">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-823">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-824">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-826">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-827">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-828">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ca0ab-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca0ab-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ca0ab-830">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ca0ab-831">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ca0ab-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-832">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-833">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ca0ab-834">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-835">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-836">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ca0ab-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ca0ab-837">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-838">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-839">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca0ab-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca0ab-840">Az.LogicApp</span></span>
* <span data-ttu-id="ca0ab-841">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ca0ab-842">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ca0ab-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-843">Az.ManagedServices</span></span>
* <span data-ttu-id="ca0ab-844">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-845">Az.Network</span></span>
* <span data-ttu-id="ca0ab-846">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ca0ab-847">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-847">New cmdlets</span></span>
        - <span data-ttu-id="ca0ab-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca0ab-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca0ab-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca0ab-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ca0ab-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ca0ab-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ca0ab-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ca0ab-856">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="ca0ab-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ca0ab-857">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ca0ab-858">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ca0ab-859">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ca0ab-860">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ca0ab-861">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ca0ab-862">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-862">Updated cmdlets</span></span>
        - <span data-ttu-id="ca0ab-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca0ab-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ca0ab-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ca0ab-866">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ca0ab-867">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ca0ab-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ca0ab-868">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ca0ab-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ca0ab-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ca0ab-872">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="ca0ab-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ca0ab-873">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ca0ab-874">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-876">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="ca0ab-877">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-879">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ca0ab-880">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ca0ab-881">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ca0ab-882">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ca0ab-883">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ca0ab-884">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ca0ab-885">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ca0ab-886">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ca0ab-887">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="ca0ab-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ca0ab-888">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-889">Az.Resources</span></span>
- <span data-ttu-id="ca0ab-890">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ca0ab-891">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ca0ab-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-892">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-893">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ca0ab-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ca0ab-894">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-895">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-896">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ca0ab-897">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ca0ab-898">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-899">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-900">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ca0ab-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ca0ab-901">Az.StorageSync</span></span>
* <span data-ttu-id="ca0ab-902">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ca0ab-903">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ca0ab-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-904">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-905">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ca0ab-906">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ca0ab-907">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ca0ab-908">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-909">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-910">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ca0ab-911">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ca0ab-912">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ca0ab-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-913">Az.Advisor</span></span>
* <span data-ttu-id="ca0ab-914">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ca0ab-915">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="ca0ab-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-916">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-917">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ca0ab-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ca0ab-919">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ca0ab-920">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ca0ab-921">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ca0ab-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ca0ab-923">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-924">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-925">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-926">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-927">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-928">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-929">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca0ab-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca0ab-930">Az.EventGrid</span></span>
* <span data-ttu-id="ca0ab-931">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-932">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-933">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-934">Az.Network</span></span>
* <span data-ttu-id="ca0ab-935">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ca0ab-936">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca0ab-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca0ab-938">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ca0ab-939">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ca0ab-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-941">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-943">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="ca0ab-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-944">Az.Resources</span></span>
    - <span data-ttu-id="ca0ab-945">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ca0ab-946">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ca0ab-947">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ca0ab-948">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="ca0ab-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-949">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-950">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="ca0ab-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-951">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-952">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ca0ab-953">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ca0ab-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca0ab-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca0ab-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ca0ab-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ca0ab-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ca0ab-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ca0ab-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ca0ab-960">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="ca0ab-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-961">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-962">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ca0ab-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca0ab-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ca0ab-964">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ca0ab-965">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ca0ab-966">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ca0ab-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ca0ab-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ca0ab-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ca0ab-969">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="ca0ab-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ca0ab-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca0ab-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ca0ab-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ca0ab-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ca0ab-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ca0ab-972">Az.StorageSync</span></span>
* <span data-ttu-id="ca0ab-973">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="ca0ab-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ca0ab-974">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-975">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-976">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ca0ab-977">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ca0ab-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ca0ab-978">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ca0ab-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ca0ab-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ca0ab-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ca0ab-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-981">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-982">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ca0ab-983">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ca0ab-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ca0ab-984">Az.Dns</span></span>
* <span data-ttu-id="ca0ab-985">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca0ab-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca0ab-986">Az.EventGrid</span></span>
* <span data-ttu-id="ca0ab-987">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ca0ab-988">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-988">New cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca0ab-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca0ab-990">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca0ab-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca0ab-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca0ab-992">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ca0ab-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ca0ab-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ca0ab-994">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca0ab-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ca0ab-996">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ca0ab-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ca0ab-998">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ca0ab-999">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ca0ab-1000">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ca0ab-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ca0ab-1002">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="ca0ab-1003">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ca0ab-1004">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ca0ab-1005">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ca0ab-1007">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ca0ab-1008">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ca0ab-1009">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ca0ab-1010">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ca0ab-1011">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ca0ab-1012">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ca0ab-1013">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ca0ab-1014">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="ca0ab-1015">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ca0ab-1016">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ca0ab-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ca0ab-1018">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ca0ab-1019">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="ca0ab-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ca0ab-1022">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ca0ab-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ca0ab-1024">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1025">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1026">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ca0ab-1027">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1027">New cmdlets</span></span>
        - <span data-ttu-id="ca0ab-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ca0ab-1029">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ca0ab-1030">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1030">New cmdlets</span></span> 
        - <span data-ttu-id="ca0ab-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ca0ab-1032">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ca0ab-1033">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1033">New cmdlets</span></span> 
        - <span data-ttu-id="ca0ab-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="ca0ab-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca0ab-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ca0ab-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ca0ab-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ca0ab-1039">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ca0ab-1040">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1040">New cmdlets</span></span>
        - <span data-ttu-id="ca0ab-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca0ab-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca0ab-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ca0ab-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ca0ab-1045">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ca0ab-1046">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ca0ab-1047">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ca0ab-1048">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ca0ab-1049">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ca0ab-1050">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ca0ab-1051">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ca0ab-1052">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ca0ab-1053">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ca0ab-1054">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ca0ab-1055">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ca0ab-1056">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ca0ab-1057">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ca0ab-1058">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ca0ab-1059">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-1060">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ca0ab-1061">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ca0ab-1062">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ca0ab-1063">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="ca0ab-1064">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="ca0ab-1065">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ca0ab-1066">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ca0ab-1067">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-1069">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1070">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1071">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ca0ab-1072">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ca0ab-1073">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ca0ab-1074">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-1076">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1077">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1078">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ca0ab-1079">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ca0ab-1080">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ca0ab-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca0ab-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca0ab-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ca0ab-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ca0ab-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1086">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1087">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ca0ab-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="ca0ab-1089">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ca0ab-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1091">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1092">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ca0ab-1093">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ca0ab-1094">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ca0ab-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1095">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-1096">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1097">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1098">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ca0ab-1099">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1100">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-1101">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ca0ab-1102">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1103">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1104">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ca0ab-1105">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca0ab-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca0ab-1107">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1109">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-1111">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-1113">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ca0ab-1114">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1115">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1116">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ca0ab-1117">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ca0ab-1118">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ca0ab-1119">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1120">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1121">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ca0ab-1122">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-1124">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ca0ab-1125">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ca0ab-1126">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ca0ab-1127">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ca0ab-1128">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ca0ab-1129">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ca0ab-1130">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ca0ab-1131">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ca0ab-1132">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ca0ab-1133">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ca0ab-1134">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ca0ab-1135">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ca0ab-1136">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ca0ab-1137">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ca0ab-1138">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ca0ab-1139">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ca0ab-1140">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ca0ab-1141">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ca0ab-1142">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="ca0ab-1143">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ca0ab-1144">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ca0ab-1145">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ca0ab-1146">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ca0ab-1147">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="ca0ab-1148">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ca0ab-1149">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ca0ab-1150">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ca0ab-1151">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ca0ab-1152">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ca0ab-1153">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ca0ab-1154">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="ca0ab-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ca0ab-1156">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ca0ab-1157">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ca0ab-1158">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ca0ab-1159">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ca0ab-1160">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ca0ab-1161">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ca0ab-1162">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ca0ab-1163">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="ca0ab-1164">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ca0ab-1165">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ca0ab-1166">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ca0ab-1167">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ca0ab-1168">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ca0ab-1169">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ca0ab-1170">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="ca0ab-1171">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ca0ab-1172">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ca0ab-1173">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ca0ab-1174">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ca0ab-1175">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ca0ab-1176">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ca0ab-1177">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ca0ab-1178">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ca0ab-1179">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ca0ab-1180">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ca0ab-1181">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ca0ab-1182">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ca0ab-1183">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ca0ab-1184">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ca0ab-1185">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ca0ab-1186">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ca0ab-1187">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ca0ab-1188">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ca0ab-1189">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ca0ab-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ca0ab-1191">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ca0ab-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ca0ab-1193">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ca0ab-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ca0ab-1195">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ca0ab-1196">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ca0ab-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ca0ab-1198">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="ca0ab-1199">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ca0ab-1200">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1201">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1202">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ca0ab-1203">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ca0ab-1204">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ca0ab-1205">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ca0ab-1206">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ca0ab-1207">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ca0ab-1208">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1209">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1210">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ca0ab-1211">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1213">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1214">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-1215">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1216">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1217">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ca0ab-1218">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="ca0ab-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ca0ab-1220">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1221">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1222">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1223">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1224">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ca0ab-1225">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1226">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1227">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-1229">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ca0ab-1230">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1231">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1232">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ca0ab-1233">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ca0ab-1234">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ca0ab-1235">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ca0ab-1236">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ca0ab-1237">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="ca0ab-1238">重大變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1238">Breaking changes</span></span>
    - <span data-ttu-id="ca0ab-1239">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ca0ab-1240">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ca0ab-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="ca0ab-1242">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ca0ab-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1243">Az.Dns</span></span>
* <span data-ttu-id="ca0ab-1244">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ca0ab-1245">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ca0ab-1246">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="ca0ab-1248">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ca0ab-1249">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1250">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-1251">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ca0ab-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ca0ab-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ca0ab-1254">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ca0ab-1255">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ca0ab-1256">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ca0ab-1257">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1258">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-1259">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="ca0ab-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ca0ab-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ca0ab-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ca0ab-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ca0ab-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ca0ab-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ca0ab-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca0ab-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca0ab-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca0ab-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca0ab-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ca0ab-1271">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ca0ab-1272">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1273">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1274">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ca0ab-1275">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1275">New cmdlets</span></span>
        - <span data-ttu-id="ca0ab-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="ca0ab-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ca0ab-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ca0ab-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ca0ab-1280">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="ca0ab-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ca0ab-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ca0ab-1283">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ca0ab-1284">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ca0ab-1285">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca0ab-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca0ab-1287">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ca0ab-1288">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ca0ab-1289">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1291">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ca0ab-1292">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ca0ab-1293">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ca0ab-1294">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ca0ab-1295">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ca0ab-1296">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ca0ab-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1297">Az.Relay</span></span>
* <span data-ttu-id="ca0ab-1298">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-1300">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1301">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1302">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ca0ab-1303">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ca0ab-1304">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ca0ab-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="ca0ab-1306">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ca0ab-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ca0ab-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ca0ab-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1310">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1311">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ca0ab-1312">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ca0ab-1313">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca0ab-1314">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="ca0ab-1315">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="ca0ab-1316">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca0ab-1317">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca0ab-1318">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca0ab-1319">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca0ab-1320">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1321">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1322">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1323">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ca0ab-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1324">Az.Batch</span></span>
* <span data-ttu-id="ca0ab-1325">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1326">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-1327">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-1329">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1330">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1331">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ca0ab-1332">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1333">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1334">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-1335">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1337">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca0ab-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1338">Az.EventGrid</span></span>
* <span data-ttu-id="ca0ab-1339">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1340">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-1341">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="ca0ab-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1342">Az.HDInsight</span></span>
* <span data-ttu-id="ca0ab-1343">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1344">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-1345">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1346">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-1347">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1348">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ca0ab-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="ca0ab-1350">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ca0ab-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1351">Az.Media</span></span>
* <span data-ttu-id="ca0ab-1352">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1353">Az.Monitor</span></span>
  * <span data-ttu-id="ca0ab-1354">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ca0ab-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ca0ab-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ca0ab-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ca0ab-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ca0ab-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ca0ab-1360">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1361">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1362">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1363">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ca0ab-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="ca0ab-1365">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-1367">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ca0ab-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ca0ab-1369">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1371">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1372">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ca0ab-1373">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ca0ab-1374">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca0ab-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1375">Az.RedisCache</span></span>
* <span data-ttu-id="ca0ab-1376">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1377">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1378">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1379">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1380">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ca0ab-1381">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1382">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ca0ab-1383">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ca0ab-1384">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ca0ab-1385">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ca0ab-1386">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1387">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1388">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ca0ab-1389">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ca0ab-1390">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ca0ab-1391">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ca0ab-1392">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca0ab-1393">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="ca0ab-1394">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="ca0ab-1395">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca0ab-1396">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca0ab-1397">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca0ab-1398">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca0ab-1399">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1400">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1401">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1402">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca0ab-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca0ab-1404">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ca0ab-1405">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1406">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1407">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ca0ab-1408">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ca0ab-1409">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1410">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1411">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ca0ab-1412">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ca0ab-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="ca0ab-1414">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1415">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-1416">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ca0ab-1417">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1418">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1419">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ca0ab-1420">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ca0ab-1421">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ca0ab-1422">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ca0ab-1423">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ca0ab-1424">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1425">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1426">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1427">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1428">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ca0ab-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="ca0ab-1430">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ca0ab-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ca0ab-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ca0ab-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ca0ab-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ca0ab-1435">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ca0ab-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ca0ab-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ca0ab-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ca0ab-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ca0ab-1440">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ca0ab-1441">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="ca0ab-1442">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="ca0ab-1443">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ca0ab-1444">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ca0ab-1445">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ca0ab-1446">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca0ab-1447">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1448">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1449">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1450">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ca0ab-1451">動態分組</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="ca0ab-1452">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1452">Pre-Post script</span></span>
    * <span data-ttu-id="ca0ab-1453">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1454">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1455">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ca0ab-1456">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1457">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-1458">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1459">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1460">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ca0ab-1461">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1463">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ca0ab-1464">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1465">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1466">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ca0ab-1467">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1468">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1469">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1470">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1471">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ca0ab-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca0ab-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca0ab-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ca0ab-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ca0ab-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ca0ab-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1478">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1479">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ca0ab-1480">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1481">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1482">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ca0ab-1483">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1484">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1485">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ca0ab-1486">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ca0ab-1487">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1488">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-1489">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1490">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1491">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1492">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-1493">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca0ab-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1494">Az.LogicApp</span></span>
* <span data-ttu-id="ca0ab-1495">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1496">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1497">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1499">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ca0ab-1500">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1500">SDK Update</span></span>
* <span data-ttu-id="ca0ab-1501">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ca0ab-1502">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1503">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1504">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ca0ab-1505">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ca0ab-1506">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ca0ab-1507">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ca0ab-1508">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ca0ab-1509">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1510">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1511">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ca0ab-1512">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1513">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1514">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ca0ab-1515">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ca0ab-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca0ab-1517">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1518">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1519">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ca0ab-1520">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ca0ab-1521">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-1523">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1524">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1525">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ca0ab-1526">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ca0ab-1527">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ca0ab-1528">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1530">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ca0ab-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1531">Az.EventHub</span></span>
* <span data-ttu-id="ca0ab-1532">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1533">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-1534">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca0ab-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1535">Az.LogicApp</span></span>
* <span data-ttu-id="ca0ab-1536">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ca0ab-1537">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ca0ab-1538">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ca0ab-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca0ab-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca0ab-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ca0ab-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ca0ab-1543">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ca0ab-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca0ab-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca0ab-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ca0ab-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ca0ab-1548">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ca0ab-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1549">Az.Monitor</span></span>
* <span data-ttu-id="ca0ab-1550">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1551">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1552">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="ca0ab-1554">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ca0ab-1555">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ca0ab-1556">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1557">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1558">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ca0ab-1559">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ca0ab-1560">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ca0ab-1561">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1562">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1563">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ca0ab-1564">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1565">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1566">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ca0ab-1567">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1568">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1569">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca0ab-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="ca0ab-1571">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1572">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1573">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ca0ab-1574">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ca0ab-1575">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="ca0ab-1577">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1578">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1579">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ca0ab-1580">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ca0ab-1581">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ca0ab-1582">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1583">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1584">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ca0ab-1585">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ca0ab-1586">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ca0ab-1587">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1588">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1589">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ca0ab-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="ca0ab-1591">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="ca0ab-1593">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ca0ab-1594">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1595">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1596">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ca0ab-1597">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca0ab-1598">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ca0ab-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1599">Az.Aks</span></span>
* <span data-ttu-id="ca0ab-1600">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ca0ab-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1601">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1602">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ca0ab-1603">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ca0ab-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1604">Az.Cdn</span></span>
* <span data-ttu-id="ca0ab-1605">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1606">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1607">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ca0ab-1608">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ca0ab-1609">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ca0ab-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ca0ab-1611">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ca0ab-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1612">Az.DataFactory</span></span>
* <span data-ttu-id="ca0ab-1613">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1615">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ca0ab-1616">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ca0ab-1617">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1618">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-1619">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1620">Az.KeyVault</span></span>
* <span data-ttu-id="ca0ab-1621">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1622">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1623">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1624">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1625">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ca0ab-1626">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ca0ab-1627">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ca0ab-1628">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ca0ab-1629">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ca0ab-1630">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ca0ab-1631">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-1633">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ca0ab-1634">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1634">Fix some error messages.</span></span>
* <span data-ttu-id="ca0ab-1635">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ca0ab-1636">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca0ab-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1637">Az.SignalR</span></span>
* <span data-ttu-id="ca0ab-1638">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1639">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1640">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca0ab-1641">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ca0ab-1642">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ca0ab-1643">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1644">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1645">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca0ab-1646">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ca0ab-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ca0ab-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ca0ab-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="ca0ab-1650">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1651">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1652">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ca0ab-1653">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ca0ab-1654">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ca0ab-1655">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1656">Az.Accounts</span></span>
* <span data-ttu-id="ca0ab-1657">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1658">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1659">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ca0ab-1660">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ca0ab-1661">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1663">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ca0ab-1664">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ca0ab-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1665">Az.EventGrid</span></span>
* <span data-ttu-id="ca0ab-1666">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ca0ab-1667">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ca0ab-1668">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ca0ab-1669">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ca0ab-1670">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ca0ab-1671">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ca0ab-1672">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ca0ab-1673">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ca0ab-1674">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ca0ab-1675">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="ca0ab-1676">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ca0ab-1677">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ca0ab-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1678">Az.IotHub</span></span>
* <span data-ttu-id="ca0ab-1679">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ca0ab-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1680">Az.LogicApp</span></span>
* <span data-ttu-id="ca0ab-1681">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1682">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1683">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ca0ab-1684">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ca0ab-1685">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ca0ab-1686">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ca0ab-1687">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ca0ab-1688">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ca0ab-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1689">Az.SignalR</span></span>
* <span data-ttu-id="ca0ab-1690">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1691">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1692">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ca0ab-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1693">Az.Storage</span></span>
* <span data-ttu-id="ca0ab-1694">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ca0ab-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="ca0ab-1696">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ca0ab-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1698">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1699">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ca0ab-1700">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ca0ab-1701">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ca0ab-1702">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1702">General</span></span>

- <span data-ttu-id="ca0ab-1703">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="ca0ab-1704">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1704">Online help for each module</span></span>
- <span data-ttu-id="ca0ab-1705">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ca0ab-1706">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ca0ab-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1707">Az.Accounts</span></span>
- <span data-ttu-id="ca0ab-1708">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="ca0ab-1709">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="ca0ab-1711">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1711">Fixes for #7002</span></span>
- <span data-ttu-id="ca0ab-1712">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ca0ab-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1713">Az.Batch</span></span>
- <span data-ttu-id="ca0ab-1714">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ca0ab-1715">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ca0ab-1716">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ca0ab-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1717">Az.Billing</span></span>
- <span data-ttu-id="ca0ab-1718">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ca0ab-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="ca0ab-1720">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ca0ab-1721">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ca0ab-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="ca0ab-1723">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ca0ab-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ca0ab-1725">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="ca0ab-1727">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ca0ab-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1728">Az.Monitor</span></span>
- <span data-ttu-id="ca0ab-1729">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ca0ab-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1730">Az.KeyVault</span></span>
- <span data-ttu-id="ca0ab-1731">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ca0ab-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="ca0ab-1733">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ca0ab-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1734">Az.Media</span></span>
- <span data-ttu-id="ca0ab-1735">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1736">Az.Network</span></span>
<span data-ttu-id="ca0ab-1737">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ca0ab-1738">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="ca0ab-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ca0ab-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ca0ab-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ca0ab-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ca0ab-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ca0ab-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ca0ab-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ca0ab-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ca0ab-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ca0ab-1753">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ca0ab-1754">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ca0ab-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ca0ab-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ca0ab-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ca0ab-1758">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ca0ab-1759">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ca0ab-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="ca0ab-1761">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ca0ab-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1762">Az.Profile</span></span>
- <span data-ttu-id="ca0ab-1763">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="ca0ab-1765">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ca0ab-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1766">Az.Resources</span></span>
- <span data-ttu-id="ca0ab-1767">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="ca0ab-1769">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ca0ab-1770">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ca0ab-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="ca0ab-1772">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ca0ab-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1773">Az.Sql</span></span>
- <span data-ttu-id="ca0ab-1774">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ca0ab-1775">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ca0ab-1776">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ca0ab-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1777">Az.Storage</span></span>
- <span data-ttu-id="ca0ab-1778">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1779">Az.Websites</span></span>
- <span data-ttu-id="ca0ab-1780">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ca0ab-1781">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ca0ab-1782">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1782">General</span></span>

* <span data-ttu-id="ca0ab-1783">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ca0ab-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1784">Az.Compute</span></span>

* <span data-ttu-id="ca0ab-1785">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="ca0ab-1787">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ca0ab-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="ca0ab-1789">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="ca0ab-1790">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ca0ab-1791">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ca0ab-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="ca0ab-1793">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ca0ab-1794">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ca0ab-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1795">Az.Resources</span></span>

* <span data-ttu-id="ca0ab-1796">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ca0ab-1797">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ca0ab-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1798">Az.Sql</span></span>

* <span data-ttu-id="ca0ab-1799">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ca0ab-1800">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ca0ab-1801">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ca0ab-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1802">Az.Storage</span></span>

* <span data-ttu-id="ca0ab-1803">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ca0ab-1804">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ca0ab-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ca0ab-1806">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="ca0ab-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ca0ab-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1809">Az.Websites</span></span>

* <span data-ttu-id="ca0ab-1810">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ca0ab-1811">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ca0ab-1812">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ca0ab-1813">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ca0ab-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="ca0ab-1815">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ca0ab-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1816">Az.Automation</span></span>
* <span data-ttu-id="ca0ab-1817">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ca0ab-1818">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ca0ab-1819">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ca0ab-1820">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ca0ab-1821">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ca0ab-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1822">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1823">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ca0ab-1824">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ca0ab-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="ca0ab-1826">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ca0ab-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ca0ab-1828">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1829">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1830">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ca0ab-1831">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ca0ab-1832">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ca0ab-1833">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ca0ab-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ca0ab-1835">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ca0ab-1836">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ca0ab-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ca0ab-1838">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ca0ab-1839">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ca0ab-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1840">Az.Relay</span></span>
* <span data-ttu-id="ca0ab-1841">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ca0ab-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1842">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1843">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ca0ab-1844">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ca0ab-1845">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-1847">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ca0ab-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1848">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1849">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ca0ab-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca0ab-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca0ab-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca0ab-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ca0ab-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca0ab-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca0ab-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ca0ab-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ca0ab-1858">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ca0ab-1859">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ca0ab-1860">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ca0ab-1861">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ca0ab-1862">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ca0ab-1863">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ca0ab-1864">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ca0ab-1865">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ca0ab-1866">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ca0ab-1867">一般</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1867">General</span></span>
* <span data-ttu-id="ca0ab-1868">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ca0ab-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1869">Az.Profile</span></span>
* <span data-ttu-id="ca0ab-1870">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ca0ab-1871">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ca0ab-1872">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ca0ab-1873">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ca0ab-1874">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ca0ab-1875">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ca0ab-1876">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-1878">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1879">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1880">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ca0ab-1881">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ca0ab-1882">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1884">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ca0ab-1885">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ca0ab-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1886">Az.Insights</span></span>
* <span data-ttu-id="ca0ab-1887">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ca0ab-1888">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ca0ab-1889">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ca0ab-1890">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1891">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1892">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ca0ab-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ca0ab-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ca0ab-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ca0ab-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ca0ab-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ca0ab-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ca0ab-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="ca0ab-1900">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1901">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1902">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ca0ab-1903">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ca0ab-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="ca0ab-1905">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ca0ab-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="ca0ab-1907">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ca0ab-1908">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ca0ab-1909">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ca0ab-1910">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ca0ab-1911">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ca0ab-1912">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ca0ab-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1913">Az.Profile</span></span>
* <span data-ttu-id="ca0ab-1914">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ca0ab-1915">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1916">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1917">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ca0ab-1918">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ca0ab-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="ca0ab-1920">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ca0ab-1921">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ca0ab-1922">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ca0ab-1923">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ca0ab-1924">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1925">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1926">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ca0ab-1927">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1928">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1929">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ca0ab-1930">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ca0ab-1931">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ca0ab-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1932">Azure.Storage</span></span>
* <span data-ttu-id="ca0ab-1933">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ca0ab-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ca0ab-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ca0ab-1936">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ca0ab-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ca0ab-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="ca0ab-1939">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ca0ab-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1940">Az.Compute</span></span>
* <span data-ttu-id="ca0ab-1941">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ca0ab-1942">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ca0ab-1943">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ca0ab-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ca0ab-1945">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ca0ab-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1946">Az.Network</span></span>
* <span data-ttu-id="ca0ab-1947">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ca0ab-1948">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1948">new cmdlets added</span></span>
    - <span data-ttu-id="ca0ab-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca0ab-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca0ab-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca0ab-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ca0ab-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ca0ab-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ca0ab-1955">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ca0ab-1956">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ca0ab-1957">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ca0ab-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1958">Az.RedisCache</span></span>
* <span data-ttu-id="ca0ab-1959">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ca0ab-1960">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ca0ab-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1961">Az.Resources</span></span>
* <span data-ttu-id="ca0ab-1962">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ca0ab-1963">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ca0ab-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1964">Az.Sql</span></span>
* <span data-ttu-id="ca0ab-1965">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ca0ab-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1966">Az.Websites</span></span>
* <span data-ttu-id="ca0ab-1967">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ca0ab-1968">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ca0ab-1969">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ca0ab-1970">初始版本</span><span class="sxs-lookup"><span data-stu-id="ca0ab-1970">Initial Release</span></span>
