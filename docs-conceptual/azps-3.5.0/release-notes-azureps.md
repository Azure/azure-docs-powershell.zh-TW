---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477228"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6eb0c-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="6eb0c-104">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-105">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-105">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-106">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="6eb0c-107">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="6eb0c-108">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-109">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-110">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="6eb0c-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-111">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-112">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-114">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="6eb0c-115">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-116">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-117">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="6eb0c-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-118">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-119">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="6eb0c-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-120">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-121">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6eb0c-122">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="6eb0c-123">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6eb0c-124">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6eb0c-125">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6eb0c-126">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-127">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-128">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-129">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-130">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="6eb0c-131">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="6eb0c-132">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-133">Az.Network</span></span>
* <span data-ttu-id="6eb0c-134">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="6eb0c-135">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6eb0c-136">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6eb0c-137">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="6eb0c-138">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-138">No new cmdlets are added.</span></span> <span data-ttu-id="6eb0c-139">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="6eb0c-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-141">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-142">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-143">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="6eb0c-144">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="6eb0c-145">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="6eb0c-146">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="6eb0c-147">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="6eb0c-148">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="6eb0c-149">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="6eb0c-150">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="6eb0c-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-151">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-152">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="6eb0c-153">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="6eb0c-154">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="6eb0c-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6eb0c-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6eb0c-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6eb0c-156">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6eb0c-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6eb0c-157">Az.StorageSync</span></span>
* <span data-ttu-id="6eb0c-158">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6eb0c-159">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-160">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-160">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-161">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="6eb0c-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6eb0c-162">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="6eb0c-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-163">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-164">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="6eb0c-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6eb0c-165">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="6eb0c-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-166">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-167">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6eb0c-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6eb0c-168">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="6eb0c-169">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6eb0c-170">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6eb0c-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-171">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-172">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6eb0c-173">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6eb0c-174">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-175">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6eb0c-176">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-177">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-178">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6eb0c-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6eb0c-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="6eb0c-180">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="6eb0c-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6eb0c-181">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="6eb0c-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-182">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-183">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-184">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-185">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-186">Az.Network</span></span>
* <span data-ttu-id="6eb0c-187">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6eb0c-188">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="6eb0c-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6eb0c-189">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-190">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6eb0c-191">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6eb0c-192">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6eb0c-193">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6eb0c-194">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6eb0c-195">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-195">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6eb0c-197">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6eb0c-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6eb0c-199">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6eb0c-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="6eb0c-201">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6eb0c-202">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6eb0c-203">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="6eb0c-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6eb0c-204">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6eb0c-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-206">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6eb0c-207">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-208">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-209">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6eb0c-210">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-211">Az.Sql</span></span>
<span data-ttu-id="6eb0c-212">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-213">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-214">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="6eb0c-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6eb0c-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="6eb0c-216">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="6eb0c-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6eb0c-217">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="6eb0c-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-218">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-219">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6eb0c-220">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6eb0c-221">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-222">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-223">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-224">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-225">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="6eb0c-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-226">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-227">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6eb0c-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="6eb0c-229">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6eb0c-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6eb0c-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6eb0c-231">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6eb0c-232">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6eb0c-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6eb0c-233">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6eb0c-234">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6eb0c-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6eb0c-235">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6eb0c-236">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6eb0c-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6eb0c-237">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6eb0c-238">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6eb0c-239">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6eb0c-240">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6eb0c-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6eb0c-241">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6eb0c-242">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6eb0c-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6eb0c-243">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6eb0c-244">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6eb0c-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6eb0c-245">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6eb0c-246">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6eb0c-247">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6eb0c-248">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-249">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-250">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6eb0c-251">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6eb0c-252">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6eb0c-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6eb0c-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="6eb0c-254">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="6eb0c-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-255">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-256">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="6eb0c-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-257">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-258">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6eb0c-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6eb0c-259">Az.MachineLearning</span></span>
* <span data-ttu-id="6eb0c-260">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6eb0c-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6eb0c-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6eb0c-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6eb0c-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6eb0c-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6eb0c-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6eb0c-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6eb0c-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6eb0c-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6eb0c-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6eb0c-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6eb0c-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-268">Az.Network</span></span>
* <span data-ttu-id="6eb0c-269">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="6eb0c-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-271">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6eb0c-272">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6eb0c-273">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6eb0c-274">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-275">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-276">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-277">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-278">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6eb0c-279">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6eb0c-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6eb0c-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6eb0c-281">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-282">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-283">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6eb0c-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6eb0c-285">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="6eb0c-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="6eb0c-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6eb0c-287">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6eb0c-288">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-288">General</span></span>
* <span data-ttu-id="6eb0c-289">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="6eb0c-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-290">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-291">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6eb0c-292">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6eb0c-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-293">Az.Batch</span></span>
* <span data-ttu-id="6eb0c-294">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-295">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-296">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-297">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-298">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6eb0c-299">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="6eb0c-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6eb0c-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6eb0c-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="6eb0c-301">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-302">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-303">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6eb0c-304">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6eb0c-305">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-306">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-307">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6eb0c-308">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="6eb0c-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6eb0c-309">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-310">Az.Network</span></span>
* <span data-ttu-id="6eb0c-311">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-312">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-313">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6eb0c-314">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-315">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-316">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-317">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-318">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="6eb0c-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6eb0c-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6eb0c-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6eb0c-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6eb0c-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6eb0c-321">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="6eb0c-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6eb0c-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6eb0c-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6eb0c-323">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6eb0c-324">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="6eb0c-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6eb0c-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6eb0c-327">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6eb0c-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6eb0c-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6eb0c-329">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6eb0c-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6eb0c-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6eb0c-331">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-332">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-332">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-333">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6eb0c-334">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-335">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-336">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="6eb0c-336">VM Reapply feature</span></span>
    - <span data-ttu-id="6eb0c-337">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6eb0c-338">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6eb0c-339">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6eb0c-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6eb0c-340">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6eb0c-341">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6eb0c-342">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6eb0c-343">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6eb0c-344">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6eb0c-345">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6eb0c-346">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6eb0c-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6eb0c-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6eb0c-348">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6eb0c-349">取得訂單</span><span class="sxs-lookup"><span data-stu-id="6eb0c-349">Get the Order</span></span>
* <span data-ttu-id="6eb0c-350">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6eb0c-351">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="6eb0c-351">Create new Order</span></span>
* <span data-ttu-id="6eb0c-352">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6eb0c-353">移除訂單</span><span class="sxs-lookup"><span data-stu-id="6eb0c-353">Remove the Order</span></span>
* <span data-ttu-id="6eb0c-354">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6eb0c-355">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="6eb0c-355">Now creates Local Share</span></span>
* <span data-ttu-id="6eb0c-356">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6eb0c-357">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="6eb0c-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6eb0c-358">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6eb0c-359">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="6eb0c-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6eb0c-360">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6eb0c-361">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="6eb0c-362">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6eb0c-363">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="6eb0c-363">Create new Triggers</span></span>
* <span data-ttu-id="6eb0c-364">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6eb0c-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6eb0c-365">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="6eb0c-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-366">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-367">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6eb0c-368">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-370">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-371">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-372">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-373">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-374">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6eb0c-375">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6eb0c-376">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="6eb0c-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6eb0c-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-378">Az.Network</span></span>
* <span data-ttu-id="6eb0c-379">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6eb0c-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6eb0c-380">Az.PrivateDns</span></span>
* <span data-ttu-id="6eb0c-381">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="6eb0c-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-383">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6eb0c-384">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6eb0c-385">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="6eb0c-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6eb0c-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6eb0c-386">Az.RedisCache</span></span>
* <span data-ttu-id="6eb0c-387">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6eb0c-388">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6eb0c-389">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-390">Az.Resources</span></span>
- <span data-ttu-id="6eb0c-391">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6eb0c-392">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="6eb0c-393">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6eb0c-394">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6eb0c-395">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-396">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-397">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6eb0c-398">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb0c-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6eb0c-399">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6eb0c-400">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-400">General</span></span>
* <span data-ttu-id="6eb0c-401">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-402">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-403">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6eb0c-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-404">Az.Advisor</span></span>
* <span data-ttu-id="6eb0c-405">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6eb0c-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-406">Az.Batch</span></span>
* <span data-ttu-id="6eb0c-407">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6eb0c-408">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6eb0c-409">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6eb0c-410">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6eb0c-411">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6eb0c-412">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6eb0c-413">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6eb0c-414">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6eb0c-415">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6eb0c-416">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6eb0c-417">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6eb0c-418">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6eb0c-419">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6eb0c-420">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6eb0c-421">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6eb0c-422">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6eb0c-423">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6eb0c-424">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6eb0c-425">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6eb0c-426">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="6eb0c-427">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6eb0c-428">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6eb0c-429">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6eb0c-430">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="6eb0c-431">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6eb0c-432">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="6eb0c-433">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6eb0c-434">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6eb0c-435">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6eb0c-436">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6eb0c-437">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6eb0c-438">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6eb0c-439">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6eb0c-440">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6eb0c-441">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6eb0c-442">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-443">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-444">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6eb0c-445">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-446">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-447">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="6eb0c-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6eb0c-448">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6eb0c-449">DiskEncryptionSetId 參數已新增至下列 Cmdlet：Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="6eb0c-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6eb0c-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6eb0c-451">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6eb0c-452">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6eb0c-453">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6eb0c-454">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6eb0c-455">重大變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-455">Breaking changes</span></span>
    - <span data-ttu-id="6eb0c-456">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6eb0c-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6eb0c-457">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="6eb0c-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-458">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-459">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-461">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6eb0c-462">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6eb0c-463">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6eb0c-464">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="6eb0c-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6eb0c-465">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="6eb0c-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6eb0c-466">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-467">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-468">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-469">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-470">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6eb0c-471">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6eb0c-472">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6eb0c-473">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6eb0c-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6eb0c-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6eb0c-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6eb0c-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6eb0c-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6eb0c-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6eb0c-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6eb0c-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6eb0c-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6eb0c-479">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-480">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6eb0c-481">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6eb0c-482">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6eb0c-483">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6eb0c-484">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6eb0c-485">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6eb0c-486">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6eb0c-487">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6eb0c-488">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6eb0c-489">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6eb0c-490">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="6eb0c-491">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="6eb0c-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-492">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-493">重大變更：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-493">Breaking changes:</span></span>
    - <span data-ttu-id="6eb0c-494">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6eb0c-495">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6eb0c-496">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6eb0c-497">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6eb0c-498">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6eb0c-499">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6eb0c-500">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6eb0c-501">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6eb0c-502">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6eb0c-503">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6eb0c-504">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6eb0c-505">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-507">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-508">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6eb0c-509">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6eb0c-510">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-511">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-512">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-513">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-514">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-515">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="6eb0c-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-516">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-517">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-518">Az.Network</span></span>
* <span data-ttu-id="6eb0c-519">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6eb0c-520">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6eb0c-526">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6eb0c-527">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-527">New cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6eb0c-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6eb0c-529">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6eb0c-530">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="6eb0c-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6eb0c-531">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="6eb0c-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6eb0c-532">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6eb0c-533">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6eb0c-534">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6eb0c-535">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6eb0c-536">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-536">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6eb0c-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6eb0c-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6eb0c-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6eb0c-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6eb0c-542">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6eb0c-543">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6eb0c-544">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="6eb0c-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6eb0c-545">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="6eb0c-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6eb0c-546">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6eb0c-547">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6eb0c-548">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6eb0c-549">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-549">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6eb0c-551">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6eb0c-552">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6eb0c-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6eb0c-553">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6eb0c-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6eb0c-554">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6eb0c-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6eb0c-555">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6eb0c-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6eb0c-556">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6eb0c-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6eb0c-557">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6eb0c-558">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-558">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6eb0c-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6eb0c-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6eb0c-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6eb0c-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6eb0c-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6eb0c-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6eb0c-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6eb0c-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6eb0c-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6eb0c-565">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6eb0c-566">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6eb0c-567">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6eb0c-568">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="6eb0c-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6eb0c-569">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6eb0c-570">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6eb0c-571">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6eb0c-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6eb0c-572">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6eb0c-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6eb0c-573">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="6eb0c-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6eb0c-574">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="6eb0c-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6eb0c-575">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6eb0c-576">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-576">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="6eb0c-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6eb0c-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6eb0c-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-582">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-583">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-584">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6eb0c-585">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6eb0c-586">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6eb0c-587">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6eb0c-588">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6eb0c-589">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6eb0c-590">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="6eb0c-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6eb0c-591">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="6eb0c-592">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-593">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-594">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="6eb0c-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6eb0c-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6eb0c-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6eb0c-597">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="6eb0c-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6eb0c-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6eb0c-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6eb0c-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6eb0c-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="6eb0c-600">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6eb0c-601">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-601">General</span></span>
* <span data-ttu-id="6eb0c-602">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-603">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-604">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-605">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-606">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6eb0c-607">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-608">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-609">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="6eb0c-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-610">Az.Batch</span></span>
* <span data-ttu-id="6eb0c-611">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-612">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-613">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6eb0c-614">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6eb0c-615">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="6eb0c-616">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-617">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-618">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6eb0c-619">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6eb0c-620">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-622">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="6eb0c-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6eb0c-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6eb0c-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="6eb0c-624">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6eb0c-625">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6eb0c-626">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6eb0c-627">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-628">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-629">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6eb0c-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6eb0c-630">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="6eb0c-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-631">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-632">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6eb0c-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6eb0c-633">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6eb0c-634">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="6eb0c-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6eb0c-635">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-636">Az.Network</span></span>
* <span data-ttu-id="6eb0c-637">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6eb0c-638">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6eb0c-639">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-639">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6eb0c-641">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6eb0c-642">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6eb0c-643">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="6eb0c-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6eb0c-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6eb0c-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6eb0c-647">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6eb0c-648">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="6eb0c-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6eb0c-649">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6eb0c-650">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6eb0c-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6eb0c-651">Az.RedisCache</span></span>
* <span data-ttu-id="6eb0c-652">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="6eb0c-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-653">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-654">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-655">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-656">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6eb0c-657">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="6eb0c-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6eb0c-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6eb0c-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6eb0c-659">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="6eb0c-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6eb0c-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6eb0c-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6eb0c-661">Az.StorageSync</span></span>
* <span data-ttu-id="6eb0c-662">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-663">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-664">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="6eb0c-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6eb0c-665">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-666">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-667">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6eb0c-668">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6eb0c-669">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-670">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-671">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6eb0c-672">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6eb0c-673">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-674">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-675">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6eb0c-676">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6eb0c-677">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6eb0c-678">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6eb0c-679">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6eb0c-680">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6eb0c-681">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6eb0c-682">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6eb0c-683">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-684">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-685">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6eb0c-686">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="6eb0c-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-687">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-688">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-689">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-690">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6eb0c-691">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6eb0c-692">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-692">New cmdlets are:</span></span>
    - <span data-ttu-id="6eb0c-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6eb0c-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6eb0c-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6eb0c-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6eb0c-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-697">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-698">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="6eb0c-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6eb0c-699">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6eb0c-700">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6eb0c-701">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6eb0c-702">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6eb0c-703">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6eb0c-704">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6eb0c-705">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6eb0c-706">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6eb0c-707">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6eb0c-708">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6eb0c-709">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6eb0c-710">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6eb0c-711">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6eb0c-712">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6eb0c-713">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="6eb0c-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6eb0c-714">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6eb0c-715">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6eb0c-716">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6eb0c-717">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="6eb0c-717">Overall improved help files</span></span>
* <span data-ttu-id="6eb0c-718">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-719">Az.Network</span></span>
* <span data-ttu-id="6eb0c-720">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="6eb0c-721">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6eb0c-722">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="6eb0c-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6eb0c-723">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6eb0c-724">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6eb0c-725">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="6eb0c-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6eb0c-726">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="6eb0c-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6eb0c-727">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6eb0c-728">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6eb0c-729">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6eb0c-730">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6eb0c-731">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="6eb0c-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6eb0c-732">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-732">New cmdlets</span></span>
        - <span data-ttu-id="6eb0c-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6eb0c-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6eb0c-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6eb0c-735">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6eb0c-736">New-VpnSite</span></span>
        - <span data-ttu-id="6eb0c-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6eb0c-737">Update-VpnSite</span></span>
        - <span data-ttu-id="6eb0c-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-738">New-VpnConnection</span></span>
        - <span data-ttu-id="6eb0c-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-739">Update-VpnConnection</span></span>
* <span data-ttu-id="6eb0c-740">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-742">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6eb0c-743">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="6eb0c-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-744">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-745">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-747">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6eb0c-748">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6eb0c-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6eb0c-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6eb0c-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6eb0c-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6eb0c-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6eb0c-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6eb0c-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6eb0c-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6eb0c-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6eb0c-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6eb0c-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6eb0c-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6eb0c-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6eb0c-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6eb0c-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6eb0c-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6eb0c-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6eb0c-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6eb0c-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6eb0c-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6eb0c-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6eb0c-762">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6eb0c-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6eb0c-763">Az.SignalR</span></span>
* <span data-ttu-id="6eb0c-764">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-765">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-766">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6eb0c-767">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6eb0c-768">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="6eb0c-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6eb0c-769">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6eb0c-770">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-771">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-772">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6eb0c-773">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6eb0c-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6eb0c-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6eb0c-776">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6eb0c-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6eb0c-778">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="6eb0c-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6eb0c-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6eb0c-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6eb0c-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6eb0c-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6eb0c-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-783">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-784">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6eb0c-785">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6eb0c-786">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6eb0c-787">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6eb0c-788">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-788">General</span></span>
* <span data-ttu-id="6eb0c-789">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-790">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-791">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6eb0c-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6eb0c-792">Az.Aks</span></span>
* <span data-ttu-id="6eb0c-793">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6eb0c-794">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="6eb0c-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-795">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-796">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6eb0c-797">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="6eb0c-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6eb0c-798">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6eb0c-799">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="6eb0c-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6eb0c-800">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6eb0c-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-801">Az.Batch</span></span>
* <span data-ttu-id="6eb0c-802">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="6eb0c-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-803">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-804">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-805">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-806">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6eb0c-807">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="6eb0c-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6eb0c-808">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="6eb0c-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6eb0c-809">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="6eb0c-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6eb0c-810">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6eb0c-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6eb0c-811">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="6eb0c-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6eb0c-812">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6eb0c-813">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-814">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-815">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="6eb0c-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6eb0c-816">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6eb0c-817">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6eb0c-818">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-820">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-821">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-822">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6eb0c-823">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="6eb0c-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6eb0c-824">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6eb0c-825">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6eb0c-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6eb0c-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6eb0c-827">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-828">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-829">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-830">Az.Network</span></span>
* <span data-ttu-id="6eb0c-831">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6eb0c-832">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6eb0c-833">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6eb0c-834">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6eb0c-835">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="6eb0c-836">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6eb0c-837">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-839">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6eb0c-840">新增了範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-840">Added example</span></span>
    - <span data-ttu-id="6eb0c-841">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6eb0c-842">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6eb0c-843">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-845">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-846">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-847">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6eb0c-848">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6eb0c-849">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="6eb0c-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6eb0c-850">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-851">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-852">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6eb0c-853">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6eb0c-854">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-856">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6eb0c-857">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6eb0c-858">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6eb0c-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6eb0c-859">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6eb0c-860">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6eb0c-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6eb0c-861">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-862">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-863">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-864">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-865">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6eb0c-866">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6eb0c-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6eb0c-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6eb0c-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6eb0c-869">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="6eb0c-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6eb0c-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-871">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-872">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="6eb0c-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6eb0c-873">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-874">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-875">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6eb0c-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6eb0c-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6eb0c-877">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-878">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-879">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-881">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-882">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-883">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6eb0c-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6eb0c-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6eb0c-885">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6eb0c-886">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="6eb0c-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-887">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-888">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6eb0c-889">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-890">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-891">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6eb0c-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6eb0c-892">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-893">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-894">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6eb0c-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6eb0c-895">Az.LogicApp</span></span>
* <span data-ttu-id="6eb0c-896">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6eb0c-897">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6eb0c-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-898">Az.ManagedServices</span></span>
* <span data-ttu-id="6eb0c-899">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-900">Az.Network</span></span>
* <span data-ttu-id="6eb0c-901">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6eb0c-902">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-902">New cmdlets</span></span>
        - <span data-ttu-id="6eb0c-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eb0c-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6eb0c-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6eb0c-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6eb0c-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6eb0c-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6eb0c-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6eb0c-911">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="6eb0c-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6eb0c-912">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6eb0c-913">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6eb0c-914">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6eb0c-915">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6eb0c-916">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6eb0c-917">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-917">Updated cmdlets</span></span>
        - <span data-ttu-id="6eb0c-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6eb0c-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6eb0c-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6eb0c-921">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6eb0c-922">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6eb0c-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6eb0c-923">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6eb0c-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6eb0c-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6eb0c-927">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="6eb0c-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6eb0c-928">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6eb0c-929">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-931">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6eb0c-932">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-934">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6eb0c-935">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6eb0c-936">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6eb0c-937">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6eb0c-938">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6eb0c-939">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6eb0c-940">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6eb0c-941">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6eb0c-942">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="6eb0c-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6eb0c-943">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-944">Az.Resources</span></span>
- <span data-ttu-id="6eb0c-945">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6eb0c-946">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6eb0c-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-947">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-948">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6eb0c-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6eb0c-949">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-950">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-951">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6eb0c-952">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6eb0c-953">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-954">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-955">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6eb0c-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6eb0c-956">Az.StorageSync</span></span>
* <span data-ttu-id="6eb0c-957">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6eb0c-958">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="6eb0c-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-959">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-960">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6eb0c-961">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6eb0c-962">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6eb0c-963">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-964">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-965">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6eb0c-966">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6eb0c-967">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6eb0c-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-968">Az.Advisor</span></span>
* <span data-ttu-id="6eb0c-969">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6eb0c-970">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="6eb0c-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-971">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-972">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6eb0c-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6eb0c-974">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6eb0c-975">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6eb0c-976">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6eb0c-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6eb0c-978">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-979">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-980">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-981">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-982">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-983">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-984">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6eb0c-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6eb0c-985">Az.EventGrid</span></span>
* <span data-ttu-id="6eb0c-986">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-987">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-988">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-989">Az.Network</span></span>
* <span data-ttu-id="6eb0c-990">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6eb0c-991">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6eb0c-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="6eb0c-993">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6eb0c-994">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="6eb0c-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-996">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-998">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="6eb0c-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-999">Az.Resources</span></span>
    - <span data-ttu-id="6eb0c-1000">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6eb0c-1001">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6eb0c-1002">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6eb0c-1003">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-1005">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1006">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1007">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6eb0c-1008">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6eb0c-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6eb0c-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6eb0c-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6eb0c-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6eb0c-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6eb0c-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6eb0c-1015">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1016">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1017">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6eb0c-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6eb0c-1019">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6eb0c-1020">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6eb0c-1021">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6eb0c-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6eb0c-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6eb0c-1024">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6eb0c-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6eb0c-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6eb0c-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1027">Az.StorageSync</span></span>
* <span data-ttu-id="6eb0c-1028">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6eb0c-1029">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1030">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1031">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6eb0c-1032">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6eb0c-1033">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6eb0c-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6eb0c-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1036">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1037">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6eb0c-1038">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6eb0c-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1039">Az.Dns</span></span>
* <span data-ttu-id="6eb0c-1040">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6eb0c-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1041">Az.EventGrid</span></span>
* <span data-ttu-id="6eb0c-1042">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6eb0c-1043">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1043">New cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6eb0c-1045">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6eb0c-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6eb0c-1047">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6eb0c-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6eb0c-1049">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6eb0c-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6eb0c-1051">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6eb0c-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6eb0c-1053">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6eb0c-1054">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6eb0c-1055">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6eb0c-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6eb0c-1057">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6eb0c-1058">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6eb0c-1059">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6eb0c-1060">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6eb0c-1062">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6eb0c-1063">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6eb0c-1064">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6eb0c-1065">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6eb0c-1066">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6eb0c-1067">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6eb0c-1068">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6eb0c-1069">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6eb0c-1070">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6eb0c-1071">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6eb0c-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6eb0c-1073">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6eb0c-1074">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6eb0c-1077">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6eb0c-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6eb0c-1079">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1080">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1081">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6eb0c-1082">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1082">New cmdlets</span></span>
        - <span data-ttu-id="6eb0c-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6eb0c-1084">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6eb0c-1085">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1085">New cmdlets</span></span> 
        - <span data-ttu-id="6eb0c-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6eb0c-1087">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6eb0c-1088">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1088">New cmdlets</span></span> 
        - <span data-ttu-id="6eb0c-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6eb0c-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6eb0c-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6eb0c-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6eb0c-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6eb0c-1094">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6eb0c-1095">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1095">New cmdlets</span></span>
        - <span data-ttu-id="6eb0c-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6eb0c-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6eb0c-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6eb0c-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6eb0c-1100">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6eb0c-1101">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6eb0c-1102">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6eb0c-1103">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6eb0c-1104">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6eb0c-1105">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6eb0c-1106">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6eb0c-1107">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6eb0c-1108">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6eb0c-1109">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6eb0c-1110">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6eb0c-1111">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6eb0c-1112">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6eb0c-1113">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6eb0c-1114">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-1115">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6eb0c-1116">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6eb0c-1117">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6eb0c-1118">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6eb0c-1119">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6eb0c-1120">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6eb0c-1121">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6eb0c-1122">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-1124">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1125">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1126">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6eb0c-1127">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6eb0c-1128">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6eb0c-1129">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-1131">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1132">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1133">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6eb0c-1134">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6eb0c-1135">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6eb0c-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6eb0c-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6eb0c-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6eb0c-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6eb0c-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1141">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1142">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6eb0c-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="6eb0c-1144">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6eb0c-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1146">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1147">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6eb0c-1148">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6eb0c-1149">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6eb0c-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1150">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-1151">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1152">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1153">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6eb0c-1154">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1155">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-1156">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6eb0c-1157">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1158">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1159">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6eb0c-1160">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6eb0c-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="6eb0c-1162">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1164">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-1166">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-1168">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6eb0c-1169">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1170">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1171">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6eb0c-1172">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6eb0c-1173">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6eb0c-1174">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1175">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1176">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6eb0c-1177">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-1179">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6eb0c-1180">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6eb0c-1181">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6eb0c-1182">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6eb0c-1183">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6eb0c-1184">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6eb0c-1185">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6eb0c-1186">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6eb0c-1187">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6eb0c-1188">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6eb0c-1189">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6eb0c-1190">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6eb0c-1191">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6eb0c-1192">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6eb0c-1193">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6eb0c-1194">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6eb0c-1195">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6eb0c-1196">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6eb0c-1197">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6eb0c-1198">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6eb0c-1199">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6eb0c-1200">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6eb0c-1201">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6eb0c-1202">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6eb0c-1203">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6eb0c-1204">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6eb0c-1205">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6eb0c-1206">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6eb0c-1207">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6eb0c-1208">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6eb0c-1209">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6eb0c-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6eb0c-1211">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6eb0c-1212">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6eb0c-1213">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6eb0c-1214">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6eb0c-1215">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6eb0c-1216">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6eb0c-1217">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6eb0c-1218">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6eb0c-1219">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6eb0c-1220">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6eb0c-1221">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6eb0c-1222">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6eb0c-1223">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6eb0c-1224">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6eb0c-1225">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6eb0c-1226">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6eb0c-1227">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6eb0c-1228">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6eb0c-1229">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6eb0c-1230">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6eb0c-1231">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6eb0c-1232">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6eb0c-1233">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6eb0c-1234">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6eb0c-1235">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6eb0c-1236">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6eb0c-1237">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6eb0c-1238">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6eb0c-1239">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6eb0c-1240">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6eb0c-1241">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6eb0c-1242">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6eb0c-1243">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6eb0c-1244">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6eb0c-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6eb0c-1246">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6eb0c-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6eb0c-1248">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6eb0c-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6eb0c-1250">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6eb0c-1251">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6eb0c-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6eb0c-1253">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6eb0c-1254">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6eb0c-1255">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1256">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1257">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6eb0c-1258">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6eb0c-1259">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6eb0c-1260">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6eb0c-1261">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6eb0c-1262">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6eb0c-1263">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1264">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1265">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6eb0c-1266">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1268">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1269">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-1270">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1271">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1272">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6eb0c-1273">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="6eb0c-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6eb0c-1275">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1276">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1277">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1278">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1279">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6eb0c-1280">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1281">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1282">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-1284">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6eb0c-1285">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1286">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1287">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6eb0c-1288">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6eb0c-1289">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6eb0c-1290">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6eb0c-1291">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6eb0c-1292">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6eb0c-1293">重大變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1293">Breaking changes</span></span>
    - <span data-ttu-id="6eb0c-1294">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6eb0c-1295">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6eb0c-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="6eb0c-1297">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6eb0c-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1298">Az.Dns</span></span>
* <span data-ttu-id="6eb0c-1299">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6eb0c-1300">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6eb0c-1301">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="6eb0c-1303">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6eb0c-1304">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1305">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-1306">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6eb0c-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6eb0c-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6eb0c-1309">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6eb0c-1310">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6eb0c-1311">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6eb0c-1312">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1313">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-1314">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6eb0c-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6eb0c-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6eb0c-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6eb0c-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6eb0c-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6eb0c-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6eb0c-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6eb0c-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6eb0c-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6eb0c-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6eb0c-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6eb0c-1326">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6eb0c-1327">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1328">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1329">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6eb0c-1330">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1330">New cmdlets</span></span>
        - <span data-ttu-id="6eb0c-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="6eb0c-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6eb0c-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6eb0c-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6eb0c-1335">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="6eb0c-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6eb0c-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6eb0c-1338">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6eb0c-1339">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6eb0c-1340">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6eb0c-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="6eb0c-1342">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6eb0c-1343">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6eb0c-1344">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1346">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6eb0c-1347">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6eb0c-1348">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6eb0c-1349">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6eb0c-1350">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6eb0c-1351">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6eb0c-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1352">Az.Relay</span></span>
* <span data-ttu-id="6eb0c-1353">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-1355">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1356">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1357">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6eb0c-1358">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6eb0c-1359">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6eb0c-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="6eb0c-1361">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6eb0c-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6eb0c-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6eb0c-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1365">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1366">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6eb0c-1367">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6eb0c-1368">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-1369">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-1370">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="6eb0c-1371">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6eb0c-1372">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6eb0c-1373">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6eb0c-1374">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6eb0c-1375">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1376">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1377">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1378">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6eb0c-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1379">Az.Batch</span></span>
* <span data-ttu-id="6eb0c-1380">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1381">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-1382">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-1384">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1385">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1386">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6eb0c-1387">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1388">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1389">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-1390">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1392">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6eb0c-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1393">Az.EventGrid</span></span>
* <span data-ttu-id="6eb0c-1394">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1395">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-1396">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6eb0c-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1397">Az.HDInsight</span></span>
* <span data-ttu-id="6eb0c-1398">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1399">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-1400">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1401">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-1402">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1403">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6eb0c-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="6eb0c-1405">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6eb0c-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1406">Az.Media</span></span>
* <span data-ttu-id="6eb0c-1407">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1408">Az.Monitor</span></span>
  * <span data-ttu-id="6eb0c-1409">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6eb0c-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6eb0c-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6eb0c-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6eb0c-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6eb0c-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6eb0c-1415">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1416">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1417">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1418">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6eb0c-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="6eb0c-1420">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-1422">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6eb0c-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6eb0c-1424">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1426">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1427">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6eb0c-1428">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6eb0c-1429">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6eb0c-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1430">Az.RedisCache</span></span>
* <span data-ttu-id="6eb0c-1431">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1432">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1433">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1434">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1435">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6eb0c-1436">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1437">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6eb0c-1438">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6eb0c-1439">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6eb0c-1440">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6eb0c-1441">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1442">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1443">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6eb0c-1444">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6eb0c-1445">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6eb0c-1446">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6eb0c-1447">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-1448">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-1449">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="6eb0c-1450">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6eb0c-1451">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6eb0c-1452">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6eb0c-1453">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6eb0c-1454">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1455">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1456">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1457">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6eb0c-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="6eb0c-1459">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6eb0c-1460">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1461">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1462">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6eb0c-1463">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6eb0c-1464">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1465">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1466">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6eb0c-1467">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6eb0c-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="6eb0c-1469">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1470">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-1471">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6eb0c-1472">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1473">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1474">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6eb0c-1475">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6eb0c-1476">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6eb0c-1477">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6eb0c-1478">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6eb0c-1479">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1480">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1481">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1482">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1483">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6eb0c-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="6eb0c-1485">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6eb0c-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6eb0c-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6eb0c-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6eb0c-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6eb0c-1490">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6eb0c-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6eb0c-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6eb0c-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6eb0c-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6eb0c-1495">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6eb0c-1496">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="6eb0c-1497">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="6eb0c-1498">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6eb0c-1499">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6eb0c-1500">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6eb0c-1501">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6eb0c-1502">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1503">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1504">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1505">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6eb0c-1506">動態分組</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="6eb0c-1507">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1507">Pre-Post script</span></span>
    * <span data-ttu-id="6eb0c-1508">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1509">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1510">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6eb0c-1511">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1512">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-1513">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1514">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1515">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6eb0c-1516">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1518">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6eb0c-1519">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1520">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1521">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6eb0c-1522">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1523">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1524">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1525">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1526">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6eb0c-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6eb0c-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6eb0c-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6eb0c-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6eb0c-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6eb0c-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1533">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1534">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6eb0c-1535">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1536">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1537">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6eb0c-1538">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1539">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1540">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6eb0c-1541">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6eb0c-1542">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1543">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-1544">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1545">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1546">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1547">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-1548">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6eb0c-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1549">Az.LogicApp</span></span>
* <span data-ttu-id="6eb0c-1550">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1551">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1552">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1554">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6eb0c-1555">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1555">SDK Update</span></span>
* <span data-ttu-id="6eb0c-1556">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6eb0c-1557">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1558">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1559">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6eb0c-1560">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6eb0c-1561">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6eb0c-1562">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6eb0c-1563">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6eb0c-1564">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1565">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1566">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6eb0c-1567">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1568">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1569">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6eb0c-1570">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6eb0c-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="6eb0c-1572">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1573">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1574">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6eb0c-1575">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6eb0c-1576">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-1578">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1579">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1580">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6eb0c-1581">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6eb0c-1582">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6eb0c-1583">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1585">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6eb0c-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1586">Az.EventHub</span></span>
* <span data-ttu-id="6eb0c-1587">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1588">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-1589">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6eb0c-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1590">Az.LogicApp</span></span>
* <span data-ttu-id="6eb0c-1591">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6eb0c-1592">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6eb0c-1593">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6eb0c-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6eb0c-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6eb0c-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6eb0c-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6eb0c-1598">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6eb0c-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6eb0c-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6eb0c-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6eb0c-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6eb0c-1603">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6eb0c-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1604">Az.Monitor</span></span>
* <span data-ttu-id="6eb0c-1605">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1606">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1607">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="6eb0c-1609">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6eb0c-1610">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6eb0c-1611">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1612">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1613">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6eb0c-1614">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6eb0c-1615">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6eb0c-1616">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1617">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1618">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6eb0c-1619">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1620">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1621">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6eb0c-1622">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1623">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1624">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6eb0c-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="6eb0c-1626">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1627">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1628">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6eb0c-1629">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6eb0c-1630">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="6eb0c-1632">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1633">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1634">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6eb0c-1635">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6eb0c-1636">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6eb0c-1637">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1638">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1639">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6eb0c-1640">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6eb0c-1641">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6eb0c-1642">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1643">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1644">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6eb0c-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="6eb0c-1646">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="6eb0c-1648">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6eb0c-1649">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1650">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1651">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6eb0c-1652">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6eb0c-1653">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6eb0c-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1654">Az.Aks</span></span>
* <span data-ttu-id="6eb0c-1655">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6eb0c-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1656">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1657">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6eb0c-1658">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6eb0c-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1659">Az.Cdn</span></span>
* <span data-ttu-id="6eb0c-1660">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1661">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1662">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6eb0c-1663">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6eb0c-1664">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6eb0c-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6eb0c-1666">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6eb0c-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1667">Az.DataFactory</span></span>
* <span data-ttu-id="6eb0c-1668">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1670">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6eb0c-1671">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6eb0c-1672">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1673">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-1674">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1675">Az.KeyVault</span></span>
* <span data-ttu-id="6eb0c-1676">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1677">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1678">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1679">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1680">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6eb0c-1681">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6eb0c-1682">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6eb0c-1683">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6eb0c-1684">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6eb0c-1685">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6eb0c-1686">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-1688">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6eb0c-1689">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1689">Fix some error messages.</span></span>
* <span data-ttu-id="6eb0c-1690">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6eb0c-1691">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6eb0c-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1692">Az.SignalR</span></span>
* <span data-ttu-id="6eb0c-1693">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1694">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1695">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6eb0c-1696">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6eb0c-1697">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6eb0c-1698">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1699">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1700">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6eb0c-1701">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6eb0c-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6eb0c-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6eb0c-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="6eb0c-1705">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1706">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1707">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6eb0c-1708">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6eb0c-1709">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6eb0c-1710">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1711">Az.Accounts</span></span>
* <span data-ttu-id="6eb0c-1712">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1713">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1714">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6eb0c-1715">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6eb0c-1716">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1718">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6eb0c-1719">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6eb0c-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1720">Az.EventGrid</span></span>
* <span data-ttu-id="6eb0c-1721">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6eb0c-1722">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6eb0c-1723">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6eb0c-1724">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6eb0c-1725">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6eb0c-1726">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6eb0c-1727">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6eb0c-1728">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6eb0c-1729">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6eb0c-1730">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="6eb0c-1731">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6eb0c-1732">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6eb0c-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1733">Az.IotHub</span></span>
* <span data-ttu-id="6eb0c-1734">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6eb0c-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1735">Az.LogicApp</span></span>
* <span data-ttu-id="6eb0c-1736">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1737">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1738">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6eb0c-1739">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6eb0c-1740">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6eb0c-1741">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6eb0c-1742">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6eb0c-1743">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6eb0c-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1744">Az.SignalR</span></span>
* <span data-ttu-id="6eb0c-1745">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1746">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1747">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6eb0c-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1748">Az.Storage</span></span>
* <span data-ttu-id="6eb0c-1749">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6eb0c-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="6eb0c-1751">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6eb0c-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1753">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-1754">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6eb0c-1755">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6eb0c-1756">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6eb0c-1757">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1757">General</span></span>

- <span data-ttu-id="6eb0c-1758">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="6eb0c-1759">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1759">Online help for each module</span></span>
- <span data-ttu-id="6eb0c-1760">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6eb0c-1761">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6eb0c-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1762">Az.Accounts</span></span>
- <span data-ttu-id="6eb0c-1763">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="6eb0c-1764">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="6eb0c-1766">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1766">Fixes for #7002</span></span>
- <span data-ttu-id="6eb0c-1767">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6eb0c-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1768">Az.Batch</span></span>
- <span data-ttu-id="6eb0c-1769">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6eb0c-1770">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6eb0c-1771">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6eb0c-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1772">Az.Billing</span></span>
- <span data-ttu-id="6eb0c-1773">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6eb0c-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="6eb0c-1775">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6eb0c-1776">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6eb0c-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="6eb0c-1778">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6eb0c-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6eb0c-1780">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="6eb0c-1782">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6eb0c-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1783">Az.Monitor</span></span>
- <span data-ttu-id="6eb0c-1784">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6eb0c-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1785">Az.KeyVault</span></span>
- <span data-ttu-id="6eb0c-1786">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6eb0c-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="6eb0c-1788">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6eb0c-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1789">Az.Media</span></span>
- <span data-ttu-id="6eb0c-1790">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1791">Az.Network</span></span>
<span data-ttu-id="6eb0c-1792">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6eb0c-1793">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="6eb0c-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6eb0c-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6eb0c-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6eb0c-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6eb0c-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6eb0c-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6eb0c-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6eb0c-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6eb0c-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6eb0c-1808">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6eb0c-1809">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6eb0c-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6eb0c-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6eb0c-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6eb0c-1813">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6eb0c-1814">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6eb0c-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="6eb0c-1816">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6eb0c-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1817">Az.Profile</span></span>
- <span data-ttu-id="6eb0c-1818">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="6eb0c-1820">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6eb0c-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1821">Az.Resources</span></span>
- <span data-ttu-id="6eb0c-1822">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="6eb0c-1824">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6eb0c-1825">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6eb0c-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="6eb0c-1827">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6eb0c-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1828">Az.Sql</span></span>
- <span data-ttu-id="6eb0c-1829">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6eb0c-1830">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6eb0c-1831">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6eb0c-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1832">Az.Storage</span></span>
- <span data-ttu-id="6eb0c-1833">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1834">Az.Websites</span></span>
- <span data-ttu-id="6eb0c-1835">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6eb0c-1836">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6eb0c-1837">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1837">General</span></span>

* <span data-ttu-id="6eb0c-1838">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6eb0c-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1839">Az.Compute</span></span>

* <span data-ttu-id="6eb0c-1840">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="6eb0c-1842">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6eb0c-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="6eb0c-1844">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="6eb0c-1845">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6eb0c-1846">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6eb0c-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="6eb0c-1848">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6eb0c-1849">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6eb0c-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1850">Az.Resources</span></span>

* <span data-ttu-id="6eb0c-1851">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6eb0c-1852">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6eb0c-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1853">Az.Sql</span></span>

* <span data-ttu-id="6eb0c-1854">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6eb0c-1855">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6eb0c-1856">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6eb0c-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1857">Az.Storage</span></span>

* <span data-ttu-id="6eb0c-1858">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6eb0c-1859">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6eb0c-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6eb0c-1861">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="6eb0c-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6eb0c-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6eb0c-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1864">Az.Websites</span></span>

* <span data-ttu-id="6eb0c-1865">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6eb0c-1866">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6eb0c-1867">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6eb0c-1868">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6eb0c-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="6eb0c-1870">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6eb0c-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1871">Az.Automation</span></span>
* <span data-ttu-id="6eb0c-1872">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6eb0c-1873">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6eb0c-1874">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6eb0c-1875">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6eb0c-1876">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6eb0c-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1877">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1878">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6eb0c-1879">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6eb0c-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="6eb0c-1881">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6eb0c-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6eb0c-1883">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1884">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1885">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6eb0c-1886">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6eb0c-1887">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6eb0c-1888">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6eb0c-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6eb0c-1890">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6eb0c-1891">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6eb0c-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6eb0c-1893">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6eb0c-1894">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6eb0c-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1895">Az.Relay</span></span>
* <span data-ttu-id="6eb0c-1896">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6eb0c-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1897">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1898">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6eb0c-1899">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6eb0c-1900">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-1902">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6eb0c-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1903">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-1904">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6eb0c-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6eb0c-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6eb0c-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6eb0c-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6eb0c-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6eb0c-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6eb0c-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6eb0c-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6eb0c-1913">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6eb0c-1914">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6eb0c-1915">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6eb0c-1916">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6eb0c-1917">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6eb0c-1918">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6eb0c-1919">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6eb0c-1920">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6eb0c-1921">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6eb0c-1922">一般</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1922">General</span></span>
* <span data-ttu-id="6eb0c-1923">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6eb0c-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1924">Az.Profile</span></span>
* <span data-ttu-id="6eb0c-1925">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6eb0c-1926">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6eb0c-1927">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6eb0c-1928">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6eb0c-1929">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6eb0c-1930">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6eb0c-1931">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-1933">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1934">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1935">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6eb0c-1936">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6eb0c-1937">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1939">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6eb0c-1940">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6eb0c-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1941">Az.Insights</span></span>
* <span data-ttu-id="6eb0c-1942">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6eb0c-1943">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6eb0c-1944">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6eb0c-1945">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1946">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1947">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6eb0c-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6eb0c-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6eb0c-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6eb0c-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6eb0c-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6eb0c-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6eb0c-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="6eb0c-1955">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1956">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1957">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6eb0c-1958">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6eb0c-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="6eb0c-1960">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6eb0c-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="6eb0c-1962">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6eb0c-1963">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6eb0c-1964">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6eb0c-1965">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6eb0c-1966">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6eb0c-1967">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6eb0c-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1968">Az.Profile</span></span>
* <span data-ttu-id="6eb0c-1969">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6eb0c-1970">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1971">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1972">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6eb0c-1973">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6eb0c-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="6eb0c-1975">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6eb0c-1976">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6eb0c-1977">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6eb0c-1978">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6eb0c-1979">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1980">Az.Network</span></span>
* <span data-ttu-id="6eb0c-1981">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6eb0c-1982">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1983">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-1984">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6eb0c-1985">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6eb0c-1986">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6eb0c-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1987">Azure.Storage</span></span>
* <span data-ttu-id="6eb0c-1988">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6eb0c-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6eb0c-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6eb0c-1991">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6eb0c-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6eb0c-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="6eb0c-1994">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6eb0c-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1995">Az.Compute</span></span>
* <span data-ttu-id="6eb0c-1996">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6eb0c-1997">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6eb0c-1998">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6eb0c-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6eb0c-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6eb0c-2000">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6eb0c-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2001">Az.Network</span></span>
* <span data-ttu-id="6eb0c-2002">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6eb0c-2003">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2003">new cmdlets added</span></span>
    - <span data-ttu-id="6eb0c-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6eb0c-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6eb0c-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6eb0c-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6eb0c-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6eb0c-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6eb0c-2010">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6eb0c-2011">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6eb0c-2012">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6eb0c-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2013">Az.RedisCache</span></span>
* <span data-ttu-id="6eb0c-2014">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6eb0c-2015">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6eb0c-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2016">Az.Resources</span></span>
* <span data-ttu-id="6eb0c-2017">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6eb0c-2018">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6eb0c-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2019">Az.Sql</span></span>
* <span data-ttu-id="6eb0c-2020">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6eb0c-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2021">Az.Websites</span></span>
* <span data-ttu-id="6eb0c-2022">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6eb0c-2023">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6eb0c-2024">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6eb0c-2025">初始版本</span><span class="sxs-lookup"><span data-stu-id="6eb0c-2025">Initial Release</span></span>
