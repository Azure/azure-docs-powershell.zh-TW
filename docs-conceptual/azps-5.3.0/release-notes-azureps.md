---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 613ef1e104cf825c32f50fd012132d1dde91a45c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893528"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="cd182-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-103">Azure PowerShell release notes</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="cd182-104">5.3.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cd182-104">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-105">Az.Accounts</span></span>
* <span data-ttu-id="cd182-106">已修正 Windows PowerShell 中不會遵守 Http Proxy 的問題 [#13647]</span><span class="sxs-lookup"><span data-stu-id="cd182-106">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="cd182-107">已改善所產生模組中長時間執行作業的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="cd182-107">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-108">Az.Automation</span></span>
* <span data-ttu-id="cd182-109">已修正 'Start-AzAutomationRunbook' 參數無法將 PSObject 所包裝的字串轉換為 JSON 字串的問題 [#13240]</span><span class="sxs-lookup"><span data-stu-id="cd182-109">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="cd182-110">已修正 New-AzAutomationUpdateManagementAzureQuery Cmdlet 的 Location 完成碼</span><span class="sxs-lookup"><span data-stu-id="cd182-110">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-111">Az.Compute</span></span>
* <span data-ttu-id="cd182-112">已將新參數集 'VMParameterSet' 中的新參數 'VM' 新增至 'Get-AzVMDscExtensionStatus' 和 'Get-AzVMDscExtension' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-112">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="cd182-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cd182-113">Az.Databricks</span></span>
* <span data-ttu-id="cd182-114">已修正可能導致 'New-AzDatabricksVNetPeering' 在完全佈建之前就傳回的問題 (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="cd182-114">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-115">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-116">已修正 SupportsShouldProcess 問題的 'Invoke-AzDataFactoryV2Pipeline' 命令</span><span class="sxs-lookup"><span data-stu-id="cd182-116">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cd182-117">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cd182-117">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cd182-118">已將 StartVMOnConnect 屬性新增至 hostpool。</span><span class="sxs-lookup"><span data-stu-id="cd182-118">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-119">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-119">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-120">已新增屬性：AzureHDInsightHostInfo 類別中的 Fqdn 和 EffectiveDiskEncryptionKeyUrl。</span><span class="sxs-lookup"><span data-stu-id="cd182-120">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-121">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-122">已將新的參數 '-AsPlainText' 新增至 'Get-AzKeyVaultSecret'，以直接以純文字傳回祕密 [#13630]</span><span class="sxs-lookup"><span data-stu-id="cd182-122">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="cd182-123">已支援從受管理的 HSM 完整備份中選擇性地還原金鑰 [#13526]</span><span class="sxs-lookup"><span data-stu-id="cd182-123">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="cd182-124">已修正一些小問題 [#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="cd182-124">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="cd182-125">已在 SecretManagement 模組中新增遺失的 'Get-Secret' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="cd182-125">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="cd182-126">已修正可能導致不使用預設存取原則來建立保存庫的問題 [#13687]</span><span class="sxs-lookup"><span data-stu-id="cd182-126">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="cd182-127">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="cd182-127">Az.Kusto</span></span>
* <span data-ttu-id="cd182-128">已將 API 版本更新為 2020-09-18。</span><span class="sxs-lookup"><span data-stu-id="cd182-128">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-129">Az.Network</span></span>
* <span data-ttu-id="cd182-130">已修正在 ExpressRouteCircuit 案例中移除對等互連和連線 Cmdlet 時所發生的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-130">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="cd182-131">'Remove-AzExpressRouteCircuitPeeringConfig' 和 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-131">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-132">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-132">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-133">已針對 Get-AzPolicyState 新增可傳回編頁結果的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-133">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-135">已啟用 SQL 的 softdelete 功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-135">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="cd182-136">已修正 SQL AG 還原並移除容器名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="cd182-136">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="cd182-137">已變更 Azure 檔案儲存體備份項目的容器名稱格式。</span><span class="sxs-lookup"><span data-stu-id="cd182-137">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="cd182-138">已新增復原服務保存庫的 CMK 功能支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-138">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-139">Az.Resources</span></span>
* <span data-ttu-id="cd182-140">已修正 'New-AzureManagedApplication' 和 'Set-AzureManagedApplication' 中的 NullRef 例外狀況問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-140">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="cd182-141">已將 Azure Resource Manager SDK 更新為使用最新的 DeploymentScripts 正式發行 API 版本：2020-10-01。</span><span class="sxs-lookup"><span data-stu-id="cd182-141">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-142">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-142">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-143">已修正 'Add-AzServiceFabricNodeType'。</span><span class="sxs-lookup"><span data-stu-id="cd182-143">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="cd182-144">已在建立虛擬機器擴展集之前，將節點類型新增至 Service Fabric 叢集。</span><span class="sxs-lookup"><span data-stu-id="cd182-144">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-145">Az.Sql</span></span>
* <span data-ttu-id="cd182-146">已修正 'InstanceFailoverGroup' 命令的參數描述。</span><span class="sxs-lookup"><span data-stu-id="cd182-146">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="cd182-147">已更新用來從 SQL 資料分類命令的識別碼中擷取 schemaName、tableName 和 columnName 的邏輯。</span><span class="sxs-lookup"><span data-stu-id="cd182-147">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="cd182-148">已修正 'Get-AzSqlDatabaseImportExportStatus' 中的 Status 和 StatusMessage 欄位以符合文件</span><span class="sxs-lookup"><span data-stu-id="cd182-148">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="cd182-149">已新增 Microsoft 支援作業 (DevOps) 稽核 Cmdlet：Get-AzSqlServerMSSupportAudit、Set-AzSqlServerMSSupportAudit、Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-149">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-150">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-150">Az.Storage</span></span>
* <span data-ttu-id="cd182-151">已支援儲存體帳戶的建立/更新/取得/列出 EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="cd182-151">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="cd182-152">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-152">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="cd182-153">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-153">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="cd182-154">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-154">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="cd182-155">已支援使用 [加密範圍] 設定來建立容器和上傳 Blob</span><span class="sxs-lookup"><span data-stu-id="cd182-155">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="cd182-156">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-156">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="cd182-157">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-157">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="cd182-158">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-158">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cd182-159">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="cd182-159">Thanks to our community contributors</span></span>
* <span data-ttu-id="cd182-160">Andreas Wolter (@AndreasWolter)，移除行銷語言，提供更好的篩選範例 (#13671)</span><span class="sxs-lookup"><span data-stu-id="cd182-160">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="cd182-161">Tidjani Belmansour (@BelRarr)，更新 Get-AzBillingInvoice.md (#13634)</span><span class="sxs-lookup"><span data-stu-id="cd182-161">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="cd182-162">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="cd182-162">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="cd182-163">修正拼字錯誤 (#13677)</span><span class="sxs-lookup"><span data-stu-id="cd182-163">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="cd182-164">更新 PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="cd182-164">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="cd182-165">@kilobyte97，「remove Cmdlet」的錯誤修正以刪除設定 (#13655)</span><span class="sxs-lookup"><span data-stu-id="cd182-165">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="cd182-166">@kongou-ae，更新 Set-AzFirewall.md (#13727)</span><span class="sxs-lookup"><span data-stu-id="cd182-166">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="cd182-167">@MasterKuat，修正文件中標題和程式碼之間的交換 (#13666)</span><span class="sxs-lookup"><span data-stu-id="cd182-167">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="cd182-168">NickT (@nukeulis)，更新 Set-AzContext.md (#13702)</span><span class="sxs-lookup"><span data-stu-id="cd182-168">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="cd182-169">@PaulHCode，更新 Start-AzJitNetworkAccessPolicy.md - 修正範例以顯示所示範的適當 Cmdlet (#13713)</span><span class="sxs-lookup"><span data-stu-id="cd182-169">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="cd182-170">Ryan Borstelmann (@ryanborMSFT)，移除了訂用帳戶識別碼 (#13715)</span><span class="sxs-lookup"><span data-stu-id="cd182-170">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="cd182-171">Shashikant Shakya (@shshakya)，更新 Set-AzSqlDatabase.md (#13674)</span><span class="sxs-lookup"><span data-stu-id="cd182-171">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="cd182-172">Sebastian Olsen (@Spacebjorn)，更新 Get-AzRecoveryServicesBackupItem.md (#13719)</span><span class="sxs-lookup"><span data-stu-id="cd182-172">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="cd182-173">5.2.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cd182-173">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-174">Az.Accounts</span></span>
* <span data-ttu-id="cd182-175">如果無法從基礎程式庫取得，則會受控以剖析原始權杖中的 ExpiresOn 時間</span><span class="sxs-lookup"><span data-stu-id="cd182-175">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="cd182-176">已改善互動式驗證無法使用時的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-176">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-177">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-178">[重大變更] 根據預設，'New-AzApiManagementProduct' 沒有訂用帳戶限制。</span><span class="sxs-lookup"><span data-stu-id="cd182-178">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-179">Az.Compute</span></span>
* <span data-ttu-id="cd182-180">已編輯 Get-AzVm，以在檢查節流之前，先依據 '-Name' 進行篩選，因為資源太多。</span><span class="sxs-lookup"><span data-stu-id="cd182-180">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="cd182-181">新的 Cmdlet 'Start-AzVmssRollingExtensionUpgrade'。</span><span class="sxs-lookup"><span data-stu-id="cd182-181">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd182-182">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd182-182">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd182-183">支援 'Get-AzContainerRegistryUsage' 的管線輸入參數 'Name' 與管線輸入中的值 [#13605]</span><span class="sxs-lookup"><span data-stu-id="cd182-183">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="cd182-184">改善 'Connect-AzContainerRegistry' 的例外狀況</span><span class="sxs-lookup"><span data-stu-id="cd182-184">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-185">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-185">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-186">已將 ADF .Net SDK 版本更新為 4.13.0</span><span class="sxs-lookup"><span data-stu-id="cd182-186">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd182-187">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd182-187">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd182-188">已新增客戶管理金鑰的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-188">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-189">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-189">Az.IotHub</span></span>
* <span data-ttu-id="cd182-190">已修正 SAS 權杖的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-190">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-191">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-191">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-192">在設定金鑰保存庫存取原則時，支援 'all' 做為選項</span><span class="sxs-lookup"><span data-stu-id="cd182-192">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="cd182-193">支援 SecretManagement 模組的新版本 [#13366]</span><span class="sxs-lookup"><span data-stu-id="cd182-193">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="cd182-194">支援 SecretManagementModule 中 'SecretValue' 的 ByteArray、String、PSCredential 和 Hashtable [#12190]</span><span class="sxs-lookup"><span data-stu-id="cd182-194">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="cd182-195">[重大變更] 重新設計與受控 HSM 相關 Cmdlet 的 API 介面。</span><span class="sxs-lookup"><span data-stu-id="cd182-195">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-196">Az.Monitor</span></span>
* <span data-ttu-id="cd182-197">已將 'New-AzAutoscaleProfile' 的參數 'Rule' 變更為接受空白清單。</span><span class="sxs-lookup"><span data-stu-id="cd182-197">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="cd182-198">[#12903]</span><span class="sxs-lookup"><span data-stu-id="cd182-198">[#12903]</span></span>
* <span data-ttu-id="cd182-199">已新增新的 Cmdlet，以支援建立更有彈性的診斷設定：</span><span class="sxs-lookup"><span data-stu-id="cd182-199">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="cd182-200">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="cd182-200">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="cd182-201">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="cd182-201">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="cd182-202">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="cd182-202">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-203">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-204">將說明文字和參數集名稱變更為 'Restore-AzRecoveryServicesBackupItem' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-204">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-205">Az.Resources</span></span>
* <span data-ttu-id="cd182-206">已將 '-Tag' 參數支援新增至 'Set-AzTemplateSpec' 和 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="cd182-206">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="cd182-207">已將標籤顯示支援新增至範本規格的預設格式器</span><span class="sxs-lookup"><span data-stu-id="cd182-207">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-208">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-208">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-209">已將範例新增至具有 SettingsSectionDescription param 的 'Set-AzServiceFabricSetting'</span><span class="sxs-lookup"><span data-stu-id="cd182-209">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="cd182-210">已將應用程式相關的 Cmdlet 更新為呼叫支援僅適用於 ARM 部署的資源</span><span class="sxs-lookup"><span data-stu-id="cd182-210">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="cd182-211">標示為已淘汰的叢集憑證 Cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 和 'Remove-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-211">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-212">Az.Sql</span></span>
* <span data-ttu-id="cd182-213">已將 SecondaryType 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="cd182-213">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="cd182-214">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-214">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cd182-215">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-215">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cd182-216">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="cd182-216">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="cd182-217">已將 HighAvailabilityReplicaCount 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="cd182-217">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="cd182-218">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-218">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cd182-219">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-219">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="cd182-220">使 ReadReplicaCount 成為下列內容中的 HighAvailabilityReplicaCount 別名：</span><span class="sxs-lookup"><span data-stu-id="cd182-220">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="cd182-221">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-221">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cd182-222">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-222">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-223">Az.Storage</span></span>
* <span data-ttu-id="cd182-224">支援上傳 Azure 檔案大小上限至 4 TiB</span><span class="sxs-lookup"><span data-stu-id="cd182-224">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="cd182-225">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-225">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="cd182-226">已將 Azure.Storage.Blobs 升級至 12.7.0</span><span class="sxs-lookup"><span data-stu-id="cd182-226">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="cd182-227">已將 Azure.Storage.Files.Shares 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="cd182-227">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="cd182-228">已將 Azure.Storage.Files.DataLake 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="cd182-228">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-229">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-229">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-230">已新增具有下載原則和本機快取模式的同步階層處理原則功能</span><span class="sxs-lookup"><span data-stu-id="cd182-230">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-231">Az.Websites</span></span>
* <span data-ttu-id="cd182-232">防止重複存取限制規則</span><span class="sxs-lookup"><span data-stu-id="cd182-232">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cd182-233">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="cd182-233">Thanks to our community contributors</span></span>
* <span data-ttu-id="cd182-234">Andrew Dawson (@dawsonar802)，升級 Get-AzKeyVaultCertificate.md - 取得憑證並將其另存為 pfx 區段，以使用 PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="cd182-234">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="cd182-235">@iviark，醫療保健 APIs Powershell BYOK 更新 (#13518)</span><span class="sxs-lookup"><span data-stu-id="cd182-235">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="cd182-236">John Duckmanton (@johnduckmanton)，修正 TagPatchOperation 的拼寫 (#13508)</span><span class="sxs-lookup"><span data-stu-id="cd182-236">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="cd182-237">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="cd182-237">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="cd182-238">Get-AzLogicAppRunHistory Help Tidy (#13513)</span><span class="sxs-lookup"><span data-stu-id="cd182-238">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="cd182-239">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="cd182-239">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="cd182-240">更新 Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="cd182-240">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="cd182-241">更新 New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="cd182-241">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="cd182-242">@SteppingRazor，New-AzApiManagementProduct：將 SubscriptionsLimit 參數的預設值變更為 None (#13457)</span><span class="sxs-lookup"><span data-stu-id="cd182-242">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="cd182-243">Steve Burkett (@SteveBurkettNZ)，修正範例中 WorkspaceResourceId 參數的打字錯誤 (#13589)</span><span class="sxs-lookup"><span data-stu-id="cd182-243">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="cd182-244">5.1.0 - 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cd182-244">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-245">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-245">Az.Accounts</span></span>
* <span data-ttu-id="cd182-246">已修正使用 ''Connect-AzAccount -DeviceCode' 時，可能不會遵守 TenantId 的問題 [#13477]</span><span class="sxs-lookup"><span data-stu-id="cd182-246">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="cd182-247">已新增 Cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="cd182-247">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="cd182-248">已修正無法存取使用者設定檔路徑時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-248">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="cd182-249">已修正 Connect-AzAccount 期間發生 Write-Object 錯誤的問題 [#13419]</span><span class="sxs-lookup"><span data-stu-id="cd182-249">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="cd182-250">已將參數 'ContainerRegistryEndpointSuffix' 新增至：'Add-AzEnvironment'、'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="cd182-250">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="cd182-251">支援點擊 <kbd>CTRL</kbd>+<kbd>C</kbd> 來中斷登入</span><span class="sxs-lookup"><span data-stu-id="cd182-251">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="cd182-252">已修正導致 'Connect-AzAccount -KeyVaultAccessToken' 無法運作的問題 [#13127]</span><span class="sxs-lookup"><span data-stu-id="cd182-252">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="cd182-253">已修正 'Invoke-AzRestMethod' 中 Null 參考和方法不區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-253">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-254">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-254">Az.Aks</span></span>
* <span data-ttu-id="cd182-255">已修正使用者無法使用服務主體建立新 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-255">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="cd182-256">[#13012]</span><span class="sxs-lookup"><span data-stu-id="cd182-256">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="cd182-257">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-257">Az.AppConfiguration</span></span>
* <span data-ttu-id="cd182-258">'Az.AppConfiguration' 模組的正式推出</span><span class="sxs-lookup"><span data-stu-id="cd182-258">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-259">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-259">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-260">已改善 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 命令的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-260">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-261">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-261">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-262">已將 ADLS 資料平面 SDK 更新為 1.2.4-alpha。</span><span class="sxs-lookup"><span data-stu-id="cd182-262">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="cd182-263">變更： https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="cd182-263">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cd182-264">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cd182-264">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cd182-265">已新增 MSIX Package Cmdlet 和更新應用程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-265">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-266">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-266">Az.EventHub</span></span>
* <span data-ttu-id="cd182-267">已修正 EventHub 叢集沒有標記時的叢集命令</span><span class="sxs-lookup"><span data-stu-id="cd182-267">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="cd182-268">已更新 AzEventHubGeoDRConfiguration 的 PartnerNamespace 命令解說文字</span><span class="sxs-lookup"><span data-stu-id="cd182-268">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-269">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-269">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-270">已將 'ResourceProviderConnection' 和 'PrivateLink' 參數新增至 'New-AzHDInsightCluster' Cmdlet 以支援轉送輸出和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="cd182-270">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="cd182-271">已將 'AmbariDatabase' 參數新增至 'New-AzHDInsightCluster' Cmdlet，以支援自訂 Ambari 資料庫功能</span><span class="sxs-lookup"><span data-stu-id="cd182-271">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="cd182-272">將接受值 'AmbariDatabase' 新增至 'Add-AzHDInsightMetastore' Cmdlet 的 'MetastoreType' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-272">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-273">Az.IotHub</span></span>
* <span data-ttu-id="cd182-274">允許在 IoT 中樞建立 Cmdlet 中使用標記。</span><span class="sxs-lookup"><span data-stu-id="cd182-274">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-275">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-275">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-276">支援更新金鑰保存庫標記</span><span class="sxs-lookup"><span data-stu-id="cd182-276">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd182-277">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd182-277">Az.LogicApp</span></span>
* <span data-ttu-id="cd182-278">已修正 Get-AzLogicAppRunHistory 只會取得結果第一頁的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-278">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-279">Az.Network</span></span>
* <span data-ttu-id="cd182-280">已更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-280">Updated below cmdlet</span></span> 
    - <span data-ttu-id="cd182-281">'New-AzLoadBalancerFrontendIpConfigCommand'、'Set-AzLoadBalancerFrontendIpConfigCommand'、'Add-AzLoadBalancerFrontendIpConfigCommand'：</span><span class="sxs-lookup"><span data-stu-id="cd182-281">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="cd182-282">已新增 PublicIpAddressPrefix 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-282">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="cd182-283">已新增 PublicIpAddressPrefixId 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-283">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="cd182-284">已將新屬性新增至下列 Cmdlet，以允許進行全域負載平衡</span><span class="sxs-lookup"><span data-stu-id="cd182-284">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="cd182-285">'New-AzLoadBalancer'：</span><span class="sxs-lookup"><span data-stu-id="cd182-285">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="cd182-286">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-286">Added Sku Tier property</span></span>
    - <span data-ttu-id="cd182-287">'New-AzPuplicIpAddress'：</span><span class="sxs-lookup"><span data-stu-id="cd182-287">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="cd182-288">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-288">Added Sku Tier property</span></span>
    - <span data-ttu-id="cd182-289">'New-AzPublicIpPrefix'：</span><span class="sxs-lookup"><span data-stu-id="cd182-289">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="cd182-290">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-290">Added Sku Tier property</span></span>
    - <span data-ttu-id="cd182-291">'New-AzLoadBalancerBackendAddressConfig'：</span><span class="sxs-lookup"><span data-stu-id="cd182-291">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="cd182-292">已新增 LoadBalancerFrontendIPConfigurationId 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-292">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="cd182-293">已更新規劃來取代下列 Cmdlet 的警告   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-293">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="cd182-294">已新增規劃來取代下列 Cmdlet 的 'RouteTable' 引數警告   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="cd182-294">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cd182-295">已將 '-MinScaleUnits' 和 '-MaxScaleUnits' 引數設為 'Set-AzExpressRouteGateway' 中的選擇性項目</span><span class="sxs-lookup"><span data-stu-id="cd182-295">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="cd182-296">已新增 Cmdlet 來支援應用程式閘道的相互驗證和 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="cd182-296">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="cd182-297">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-297">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cd182-298">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-298">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cd182-299">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-299">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cd182-300">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-300">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cd182-301">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-301">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cd182-302">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-302">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cd182-303">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-303">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cd182-304">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-304">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cd182-305">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-305">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="cd182-306">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-306">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cd182-307">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-307">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cd182-308">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-308">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cd182-309">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-309">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cd182-310">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-310">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cd182-311">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-311">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="cd182-312">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-312">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="cd182-313">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-313">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-314">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-314">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-315">指定原則 BackupTime 的格式為 UTC。</span><span class="sxs-lookup"><span data-stu-id="cd182-315">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="cd182-316">修改 Get-AzRecoveryServicesBackupJobDetails Cmdlet 中的中斷性變更警告。</span><span class="sxs-lookup"><span data-stu-id="cd182-316">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="cd182-317">更新 Set-AzRecoveryServicesBackupProtectionPolicy Cmdlet 的範例指令碼解說文字。</span><span class="sxs-lookup"><span data-stu-id="cd182-317">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-318">Az.Resources</span></span>
* <span data-ttu-id="cd182-319">已修正 What-If 會顯示兩個大小寫不同的資源群組範圍的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-319">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="cd182-320">已將 'Export-AzResourceGroup' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-320">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="cd182-321">已將文化特性資訊新增至 parse 方法</span><span class="sxs-lookup"><span data-stu-id="cd182-321">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-322">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-322">Az.Sql</span></span>
* <span data-ttu-id="cd182-323">已修正 Set-AzSqlDatabaseAudit 不支援超大規模資料庫資料庫和資料庫版本無法判斷的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-323">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="cd182-324">已將 MaintenanceConfigurationId 新增至 New-AzSqlInstance' 和 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="cd182-324">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="cd182-325">已修正 GetAzureSqlDatabaseReplicationLink.cs 中的錯誤 (bug)：PartnerServerName 參數會以值進行檢查，而非索引鍵</span><span class="sxs-lookup"><span data-stu-id="cd182-325">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-326">Az.Websites</span></span>
* <span data-ttu-id="cd182-327">新增最新存取限制功能的支援：ServiceTag、multi-ip 和 http-headers</span><span class="sxs-lookup"><span data-stu-id="cd182-327">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cd182-328">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="cd182-328">Thanks to our community contributors</span></span>
* <span data-ttu-id="cd182-329">John Q. Martin (@johnmart82)，新增防火牆必要條件資訊 (#13385)</span><span class="sxs-lookup"><span data-stu-id="cd182-329">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="cd182-330">Manikandan Duraisamy (@madurais-msft)，修正 PublicSubnetName 引數 (#13417)</span><span class="sxs-lookup"><span data-stu-id="cd182-330">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="cd182-331">@mahortas，更新 -HostNames 參數值 (#13349)</span><span class="sxs-lookup"><span data-stu-id="cd182-331">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="cd182-332">@MariachiForHire，新增支援的 TrafficAnalyticsInterval 值 (#13304)</span><span class="sxs-lookup"><span data-stu-id="cd182-332">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="cd182-333">Michael James (@mikejwhat)，允許 Get-AzLogicAppRunHistory 傳回超過 30 個項目 (#13393)</span><span class="sxs-lookup"><span data-stu-id="cd182-333">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="cd182-334">Shashikant Shakya (@shshakya)，更新 Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="cd182-334">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="cd182-335">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cd182-335">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-336">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-336">Az.Accounts</span></span>
* <span data-ttu-id="cd182-337">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="cd182-337">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="cd182-338">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="cd182-338">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-339">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-339">Az.Aks</span></span>
* <span data-ttu-id="cd182-340">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="cd182-340">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="cd182-341">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="cd182-341">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="cd182-342">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="cd182-342">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="cd182-343">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="cd182-343">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cd182-344">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd182-344">Az.Billing</span></span>
* <span data-ttu-id="cd182-345">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-345">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="cd182-346">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-346">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="cd182-347">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-347">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="cd182-348">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="cd182-348">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="cd182-349">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="cd182-349">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-350">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-350">Az.Cdn</span></span>
* <span data-ttu-id="cd182-351">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="cd182-351">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-352">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-352">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-353">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="cd182-353">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-354">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-354">Az.Compute</span></span>
* <span data-ttu-id="cd182-355">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="cd182-355">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="cd182-356">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-356">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="cd182-357">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="cd182-357">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="cd182-358">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-358">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="cd182-359">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-359">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd182-360">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd182-360">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd182-361">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="cd182-361">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="cd182-362">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="cd182-362">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="cd182-363">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="cd182-363">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="cd182-364">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="cd182-364">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="cd182-365">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cd182-365">Az.Databricks</span></span>
* <span data-ttu-id="cd182-366">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-366">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-367">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-367">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-368">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="cd182-368">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="cd182-369">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="cd182-369">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="cd182-370">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="cd182-370">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cd182-371">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cd182-371">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cd182-372">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="cd182-372">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="cd182-373">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="cd182-373">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="cd182-374">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="cd182-374">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="cd182-375">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="cd182-375">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd182-376">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd182-376">Az.Functions</span></span>
* <span data-ttu-id="cd182-377">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-377">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="cd182-378">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="cd182-378">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="cd182-379">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="cd182-379">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="cd182-380">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="cd182-380">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="cd182-381">[#12728]</span><span class="sxs-lookup"><span data-stu-id="cd182-381">[#12728]</span></span>
  - <span data-ttu-id="cd182-382">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-382">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="cd182-383">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="cd182-383">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="cd182-384">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="cd182-384">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="cd182-385">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="cd182-385">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-386">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-386">Az.HDInsight</span></span>
 * <span data-ttu-id="cd182-387">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-387">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="cd182-388">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="cd182-388">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="cd182-389">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="cd182-389">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="cd182-390">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="cd182-390">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="cd182-391">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="cd182-391">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cd182-392">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="cd182-392">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cd182-393">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="cd182-393">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="cd182-394">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="cd182-394">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="cd182-395">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="cd182-395">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="cd182-396">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-396">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="cd182-397">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="cd182-397">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="cd182-398">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="cd182-398">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="cd182-399">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="cd182-399">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="cd182-400">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="cd182-400">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cd182-401">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="cd182-401">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="cd182-402">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-402">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="cd182-403">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="cd182-403">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="cd182-404">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-404">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="cd182-405">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="cd182-405">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="cd182-406">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="cd182-406">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-407">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-407">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-408">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-408">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="cd182-409">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="cd182-409">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="cd182-410">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="cd182-410">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="cd182-411">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-411">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="cd182-412">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="cd182-412">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd182-413">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd182-413">Az.ManagedServices</span></span>
* <span data-ttu-id="cd182-414">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="cd182-414">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-415">Az.Network</span></span>
* <span data-ttu-id="cd182-416">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="cd182-416">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="cd182-417">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-417">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="cd182-418">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="cd182-418">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="cd182-419">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="cd182-419">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="cd182-420">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-420">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="cd182-421">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="cd182-421">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="cd182-422">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="cd182-422">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="cd182-423">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="cd182-423">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="cd182-424">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="cd182-424">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="cd182-425">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="cd182-425">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="cd182-426">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="cd182-426">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="cd182-427">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-427">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="cd182-428">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="cd182-428">Added parameter '-Type'</span></span>
    - <span data-ttu-id="cd182-429">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="cd182-429">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="cd182-430">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="cd182-430">Added parameter '-Scope'</span></span>
* <span data-ttu-id="cd182-431">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-431">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-432">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-433">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="cd182-433">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="cd182-434">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-434">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-435">Az.Resources</span></span>
* <span data-ttu-id="cd182-436">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-436">Fixed parsing bug</span></span>
* <span data-ttu-id="cd182-437">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-437">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="cd182-438">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="cd182-438">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="cd182-439">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-439">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="cd182-440">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-440">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="cd182-441">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-441">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="cd182-442">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="cd182-442">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="cd182-443">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-443">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="cd182-444">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-444">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-445">Az.Sql</span></span>
* <span data-ttu-id="cd182-446">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="cd182-446">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="cd182-447">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="cd182-447">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="cd182-448">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-448">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="cd182-449">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-449">Az.Storage</span></span>
* <span data-ttu-id="cd182-450">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="cd182-450">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="cd182-451">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-451">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-452">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-452">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-453">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-453">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="cd182-454">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-454">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cd182-455">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="cd182-455">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="cd182-456">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-456">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cd182-457">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-457">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cd182-458">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="cd182-458">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="cd182-459">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="cd182-459">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="cd182-460">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="cd182-460">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="cd182-461">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-461">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="cd182-462">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-462">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="cd182-463">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="cd182-463">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="cd182-464">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="cd182-464">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="cd182-465">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="cd182-465">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="cd182-466">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="cd182-466">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="cd182-467">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="cd182-467">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="cd182-468">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-468">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="cd182-469">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-469">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="cd182-470">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="cd182-470">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="cd182-471">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-471">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="cd182-472">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-472">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="cd182-473">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="cd182-473">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="cd182-474">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-474">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-475">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-475">Az.Websites</span></span>
* <span data-ttu-id="cd182-476">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-476">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="cd182-477">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="cd182-477">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cd182-478">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="cd182-478">Thanks to our community contributors</span></span>
* <span data-ttu-id="cd182-479">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="cd182-479">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="cd182-480">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="cd182-480">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="cd182-481">(#13249)</span><span class="sxs-lookup"><span data-stu-id="cd182-481">(#13249)</span></span>
* <span data-ttu-id="cd182-482">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="cd182-482">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="cd182-483">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="cd182-483">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="cd182-484">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="cd182-484">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="cd182-485">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-485">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="cd182-486">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-486">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="cd182-487">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-487">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="cd182-488">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="cd182-488">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="cd182-489">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-489">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="cd182-490">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-490">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="cd182-491">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cd182-491">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-492">Az.Accounts</span></span>
* <span data-ttu-id="cd182-493">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="cd182-493">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-494">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-494">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-495">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-495">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="cd182-496">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-496">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-497">Az.Compute</span></span>
* <span data-ttu-id="cd182-498">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-498">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="cd182-499">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-499">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="cd182-500">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cd182-500">Az.Databricks</span></span>
* <span data-ttu-id="cd182-501">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="cd182-501">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="cd182-502">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-502">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-503">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-503">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-504">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-504">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-505">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-505">Az.EventHub</span></span>
* <span data-ttu-id="cd182-506">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-506">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-507">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-507">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-508">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-508">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="cd182-509">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-509">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="cd182-510">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-510">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="cd182-511">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-511">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="cd182-512">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-512">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="cd182-513">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-513">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-514">Az.IotHub</span></span>
* <span data-ttu-id="cd182-515">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-515">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-516">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-516">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-517">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="cd182-517">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd182-518">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd182-518">Az.ManagedServices</span></span>
* <span data-ttu-id="cd182-519">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="cd182-519">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-520">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-520">Az.Monitor</span></span>
* <span data-ttu-id="cd182-521">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-521">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="cd182-522">[#12889]</span><span class="sxs-lookup"><span data-stu-id="cd182-522">[#12889]</span></span>
* <span data-ttu-id="cd182-523">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-523">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="cd182-524">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="cd182-524">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-525">Az.Network</span></span>
* <span data-ttu-id="cd182-526">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="cd182-526">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="cd182-527">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-527">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-529">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-529">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd182-530">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd182-530">Az.RedisCache</span></span>
* <span data-ttu-id="cd182-531">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="cd182-531">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-532">Az.Sql</span></span>
* <span data-ttu-id="cd182-533">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="cd182-533">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="cd182-534">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-534">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="cd182-535">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="cd182-535">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="cd182-536">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="cd182-536">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="cd182-537">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="cd182-537">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="cd182-538">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-538">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-539">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-539">Az.Storage</span></span>
* <span data-ttu-id="cd182-540">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-540">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="cd182-541">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-541">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="cd182-542">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-542">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="cd182-543">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="cd182-543">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="cd182-544">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-544">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="cd182-545">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="cd182-545">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="cd182-546">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-546">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="cd182-547">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd182-547">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="cd182-548">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-548">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="cd182-549">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-549">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="cd182-550">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-550">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-551">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-551">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-552">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-552">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cd182-553">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="cd182-553">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="cd182-554">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="cd182-554">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="cd182-555">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="cd182-555">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-556">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-556">Az.Accounts</span></span>
* <span data-ttu-id="cd182-557">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-557">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="cd182-558">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="cd182-558">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-559">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-559">Az.Aks</span></span>
* <span data-ttu-id="cd182-560">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="cd182-560">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="cd182-561">[#12372]</span><span class="sxs-lookup"><span data-stu-id="cd182-561">[#12372]</span></span>
* <span data-ttu-id="cd182-562">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-562">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="cd182-563">[#11239]</span><span class="sxs-lookup"><span data-stu-id="cd182-563">[#11239]</span></span>
* <span data-ttu-id="cd182-564">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="cd182-564">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="cd182-565">[#11239]</span><span class="sxs-lookup"><span data-stu-id="cd182-565">[#11239]</span></span>
* <span data-ttu-id="cd182-566">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="cd182-566">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="cd182-567">[#12371]</span><span class="sxs-lookup"><span data-stu-id="cd182-567">[#12371]</span></span>
* <span data-ttu-id="cd182-568">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="cd182-568">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-569">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-569">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-570">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="cd182-570">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-571">Az.Compute</span></span>
* <span data-ttu-id="cd182-572">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-572">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="cd182-573">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="cd182-573">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="cd182-574">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-574">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="cd182-575">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-575">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="cd182-576">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="cd182-576">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="cd182-577">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="cd182-577">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="cd182-578">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="cd182-578">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="cd182-579">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cd182-579">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="cd182-580">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="cd182-580">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="cd182-581">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="cd182-581">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-582">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-582">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-583">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="cd182-583">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-584">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-584">Az.EventHub</span></span>
* <span data-ttu-id="cd182-585">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="cd182-585">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="cd182-586">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-586">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd182-587">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd182-587">Az.Functions</span></span>
* <span data-ttu-id="cd182-588">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-588">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="cd182-589">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="cd182-589">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="cd182-590">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd182-590">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-591">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-591">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-592">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="cd182-592">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="cd182-593">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-593">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="cd182-594">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="cd182-594">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="cd182-595">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-595">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cd182-596">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-596">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cd182-597">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-597">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cd182-598">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-598">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cd182-599">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="cd182-599">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-600">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-600">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-601">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="cd182-601">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="cd182-602">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="cd182-602">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="cd182-603">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="cd182-603">Az.Kusto</span></span>
* <span data-ttu-id="cd182-604">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="cd182-604">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-605">Az.Network</span></span>
* <span data-ttu-id="cd182-606">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="cd182-606">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="cd182-607">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="cd182-607">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="cd182-608">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="cd182-608">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="cd182-609">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="cd182-609">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="cd182-610">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="cd182-610">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="cd182-611">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="cd182-611">Added subscription level parameter set</span></span>
    - <span data-ttu-id="cd182-612">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="cd182-612">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="cd182-613">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="cd182-613">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cd182-614">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="cd182-614">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cd182-615">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="cd182-615">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="cd182-616">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-616">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="cd182-617">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="cd182-617">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="cd182-618">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="cd182-618">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="cd182-619">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-619">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="cd182-620">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="cd182-620">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="cd182-621">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="cd182-621">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="cd182-622">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="cd182-622">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="cd182-623">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="cd182-623">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="cd182-624">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="cd182-624">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="cd182-625">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="cd182-625">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="cd182-626">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="cd182-626">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cd182-627">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="cd182-627">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cd182-628">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-628">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="cd182-629">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="cd182-629">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-630">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-631">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="cd182-631">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-632">Az.Resources</span></span>
* <span data-ttu-id="cd182-633">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="cd182-633">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="cd182-634">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-634">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="cd182-635">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="cd182-635">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="cd182-636">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="cd182-636">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-638">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-638">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="cd182-639">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-639">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cd182-640">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-640">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cd182-641">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-641">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cd182-642">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-642">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cd182-643">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-643">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cd182-644">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-644">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cd182-645">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="cd182-645">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cd182-646">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="cd182-646">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cd182-647">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="cd182-647">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cd182-648">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="cd182-648">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cd182-649">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-649">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cd182-650">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="cd182-650">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="cd182-651">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-651">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cd182-652">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="cd182-652">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="cd182-653">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="cd182-653">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-654">Az.Sql</span></span>
* <span data-ttu-id="cd182-655">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="cd182-655">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="cd182-656">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-656">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-657">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-657">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-658">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="cd182-658">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="cd182-659">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-659">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="cd182-660">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="cd182-660">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cd182-661">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="cd182-661">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cd182-662">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="cd182-662">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cd182-663">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="cd182-663">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="cd182-664">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-664">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-665">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-665">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-666">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-666">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-667">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="cd182-667">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="cd182-668">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="cd182-668">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="cd182-669">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="cd182-669">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="cd182-670">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="cd182-670">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cd182-671">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="cd182-671">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cd182-672">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="cd182-672">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-673">Az.Storage</span></span>
* <span data-ttu-id="cd182-674">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="cd182-674">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="cd182-675">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="cd182-675">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="cd182-676">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-676">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-677">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-677">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cd182-678">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="cd182-678">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="cd182-679">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="cd182-679">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="cd182-680">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="cd182-680">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="cd182-681">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-681">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="cd182-682">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-682">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="cd182-683">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-683">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cd182-684">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-684">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cd182-685">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-685">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cd182-686">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-686">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cd182-687">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="cd182-687">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="cd182-688">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="cd182-688">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="cd182-689">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="cd182-689">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cd182-690">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="cd182-690">Thanks to our community contributors</span></span>
* <span data-ttu-id="cd182-691">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="cd182-691">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="cd182-692">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="cd182-692">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="cd182-693">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="cd182-693">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="cd182-694">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="cd182-694">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="cd182-695">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="cd182-695">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="cd182-696">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="cd182-696">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="cd182-697">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="cd182-697">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="cd182-698">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="cd182-698">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="cd182-699">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="cd182-699">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="cd182-700">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="cd182-700">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="cd182-701">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="cd182-701">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="cd182-702">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="cd182-702">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="cd182-703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-703">Az.Compute</span></span>
* <span data-ttu-id="cd182-704">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="cd182-704">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="cd182-705">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="cd182-705">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-706">Az.Accounts</span></span>
* <span data-ttu-id="cd182-707">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="cd182-707">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="cd182-708">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="cd182-708">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-709">Az.Automation</span></span>
* <span data-ttu-id="cd182-710">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="cd182-710">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-711">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-711">Az.Compute</span></span>
* <span data-ttu-id="cd182-712">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="cd182-712">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="cd182-713">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="cd182-713">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="cd182-714">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="cd182-714">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="cd182-715">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-715">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-716">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-717">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="cd182-717">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-718">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-719">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="cd182-719">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-720">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-720">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-721">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-721">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="cd182-722">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-722">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cd182-723">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cd182-723">Az.Maintenance</span></span>
* <span data-ttu-id="cd182-724">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-724">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="cd182-725">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-725">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd182-726">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd182-726">Az.ManagedServices</span></span>
* <span data-ttu-id="cd182-727">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="cd182-727">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-728">Az.Monitor</span></span>
* <span data-ttu-id="cd182-729">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="cd182-729">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="cd182-730">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-730">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-731">Az.Resources</span></span>
* <span data-ttu-id="cd182-732">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="cd182-732">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="cd182-733">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-733">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="cd182-734">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="cd182-734">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="cd182-735">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="cd182-735">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="cd182-736">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="cd182-736">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cd182-737">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="cd182-737">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="cd182-738">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="cd182-738">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="cd182-739">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-739">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd182-740">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd182-740">Az.SignalR</span></span>
* <span data-ttu-id="cd182-741">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-741">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="cd182-742">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-742">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-743">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-743">Az.Storage</span></span>
* <span data-ttu-id="cd182-744">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="cd182-744">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="cd182-745">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="cd182-745">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="cd182-746">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-746">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="cd182-747">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-747">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="cd182-748">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="cd182-748">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="cd182-749">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-749">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="cd182-750">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="cd182-750">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="cd182-751">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-751">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="cd182-752">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="cd182-752">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="cd182-753">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="cd182-753">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="cd182-754">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-754">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cd182-755">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-755">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cd182-756">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-756">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="cd182-757">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="cd182-757">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cd182-758">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-758">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="cd182-759">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="cd182-759">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-760">Az.Accounts</span></span>
* <span data-ttu-id="cd182-761">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="cd182-761">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="cd182-762">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="cd182-762">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="cd182-763">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-763">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="cd182-764">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-764">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="cd182-765">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="cd182-765">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-766">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-766">Az.Aks</span></span>
* <span data-ttu-id="cd182-767">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="cd182-767">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="cd182-768">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="cd182-768">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-769">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-769">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-770">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-770">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-771">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-771">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-772">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-772">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd182-773">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-773">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="cd182-774">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-774">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-775">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-775">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd182-776">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-776">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="cd182-777">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-777">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-778">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-778">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-779">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-779">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd182-780">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-780">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd182-781">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-781">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-782">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-783">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="cd182-783">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-784">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-784">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-785">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="cd182-785">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-786">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-786">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-787">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="cd182-787">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="cd182-788">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-788">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cd182-789">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-789">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cd182-790">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="cd182-790">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="cd182-791">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="cd182-791">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cd182-792">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-792">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cd182-793">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-793">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-794">Az.Network</span></span>
* <span data-ttu-id="cd182-795">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-795">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cd182-796">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-796">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="cd182-797">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="cd182-797">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="cd182-798">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-798">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-799">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-799">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-800">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="cd182-800">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="cd182-801">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="cd182-801">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="cd182-802">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="cd182-802">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-804">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="cd182-804">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-805">Az.Resources</span></span>
* <span data-ttu-id="cd182-806">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="cd182-806">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="cd182-807">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="cd182-807">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-808">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-808">Az.Sql</span></span>
* <span data-ttu-id="cd182-809">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-809">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cd182-810">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-810">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-811">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-811">Az.Storage</span></span>
* <span data-ttu-id="cd182-812">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-812">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="cd182-813">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="cd182-813">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="cd182-814">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="cd182-814">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="cd182-815">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-815">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="cd182-816">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="cd182-816">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="cd182-817">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="cd182-817">Supported get single file share usage</span></span>
    - <span data-ttu-id="cd182-818">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-818">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="cd182-819">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="cd182-819">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-820">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-820">Az.Accounts</span></span>
* <span data-ttu-id="cd182-821">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="cd182-821">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="cd182-822">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="cd182-822">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-823">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-823">Az.Aks</span></span>
* <span data-ttu-id="cd182-824">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="cd182-824">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-825">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd182-826">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="cd182-826">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-827">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-827">Az.Automation</span></span>
* <span data-ttu-id="cd182-828">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-828">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-829">Az.Compute</span></span>
* <span data-ttu-id="cd182-830">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="cd182-830">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-831">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-831">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-832">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="cd182-832">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd182-833">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd182-833">Az.EventGrid</span></span>
* <span data-ttu-id="cd182-834">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cd182-834">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="cd182-835">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="cd182-835">Added new features:</span></span>
    - <span data-ttu-id="cd182-836">輸入對應</span><span class="sxs-lookup"><span data-stu-id="cd182-836">Input mapping</span></span>
    - <span data-ttu-id="cd182-837">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-837">Event Delivery Schema</span></span>
    - <span data-ttu-id="cd182-838">私人連結</span><span class="sxs-lookup"><span data-stu-id="cd182-838">Private Link</span></span>
    - <span data-ttu-id="cd182-839">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-839">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="cd182-840">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="cd182-840">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="cd182-841">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="cd182-841">Azure Function As Destination</span></span>
    - <span data-ttu-id="cd182-842">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="cd182-842">WebHook Batching</span></span>
    - <span data-ttu-id="cd182-843">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="cd182-843">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="cd182-844">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="cd182-844">IpFiltering</span></span>
* <span data-ttu-id="cd182-845">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-845">Updated cmdlets:</span></span>
    - <span data-ttu-id="cd182-846">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="cd182-846">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="cd182-847">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="cd182-847">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="cd182-848">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="cd182-848">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="cd182-849">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="cd182-849">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="cd182-850">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-850">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="cd182-851">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="cd182-851">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cd182-852">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="cd182-852">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="cd182-853">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="cd182-853">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cd182-854">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="cd182-854">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-855">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-855">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-856">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="cd182-856">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="cd182-857">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="cd182-857">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-858">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-858">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-859">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="cd182-859">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-860">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-860">Az.Monitor</span></span>
* <span data-ttu-id="cd182-861">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="cd182-861">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-862">Az.Network</span></span>
* <span data-ttu-id="cd182-863">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="cd182-863">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="cd182-864">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-864">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="cd182-865">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="cd182-865">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd182-866">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="cd182-866">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd182-867">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="cd182-867">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd182-868">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="cd182-868">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd182-869">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-869">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="cd182-870">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-870">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="cd182-871">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="cd182-871">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd182-872">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="cd182-872">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd182-873">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="cd182-873">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd182-874">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="cd182-874">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd182-875">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="cd182-875">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="cd182-876">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-876">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="cd182-877">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-877">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cd182-878">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-878">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cd182-879">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-879">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-881">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="cd182-881">Removed project reference to Authentication</span></span>
* <span data-ttu-id="cd182-882">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="cd182-882">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="cd182-883">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-883">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-884">Az.Resources</span></span>
* <span data-ttu-id="cd182-885">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-885">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="cd182-886">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-886">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-887">Az.Sql</span></span>
* <span data-ttu-id="cd182-888">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-888">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="cd182-889">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-889">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="cd182-890">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="cd182-890">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-891">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-891">Az.Storage</span></span>
* <span data-ttu-id="cd182-892">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-892">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="cd182-893">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-893">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="cd182-894">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-894">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cd182-895">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-895">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-896">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="cd182-896">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cd182-897">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="cd182-897">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cd182-898">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="cd182-898">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="cd182-899">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="cd182-899">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="cd182-900">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-900">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="cd182-901">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="cd182-901">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="cd182-902">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="cd182-902">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="cd182-903">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="cd182-903">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="cd182-904">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-904">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cd182-905">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="cd182-905">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="cd182-906">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="cd182-906">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="cd182-907">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-907">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cd182-908">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="cd182-908">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-909">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-909">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-910">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="cd182-910">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="cd182-911">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-911">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="cd182-912">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="cd182-912">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="cd182-913">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-913">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-914">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-914">Az.Websites</span></span>
* <span data-ttu-id="cd182-915">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="cd182-915">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="cd182-916">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cd182-916">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-917">Az.Accounts</span></span>
* <span data-ttu-id="cd182-918">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="cd182-918">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="cd182-919">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="cd182-919">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="cd182-920">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="cd182-920">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="cd182-921">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="cd182-921">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-922">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-922">Az.Aks</span></span>
* <span data-ttu-id="cd182-923">透過對 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="cd182-923">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-924">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-924">Az.Batch</span></span>
* <span data-ttu-id="cd182-925">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-925">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="cd182-926">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="cd182-926">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-927">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-927">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-928">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-928">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="cd182-929">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="cd182-929">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-930">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-930">Az.Compute</span></span>
* <span data-ttu-id="cd182-931">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-931">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="cd182-932">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="cd182-932">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="cd182-933">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="cd182-933">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="cd182-934">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="cd182-934">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="cd182-935">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-935">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-936">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-937">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="cd182-937">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-938">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-938">Az.EventHub</span></span>
* <span data-ttu-id="cd182-939">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-939">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd182-940">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd182-940">Az.Functions</span></span>
* <span data-ttu-id="cd182-941">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-941">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-942">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-942">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-943">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="cd182-943">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd182-944">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd182-944">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd182-945">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="cd182-945">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="cd182-946">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-946">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-947">Az.Monitor</span></span>
* <span data-ttu-id="cd182-948">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="cd182-948">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="cd182-949">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="cd182-949">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-950">Az.Network</span></span>
* <span data-ttu-id="cd182-951">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-951">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cd182-952">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-952">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cd182-953">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="cd182-953">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="cd182-954">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="cd182-954">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="cd182-955">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-955">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="cd182-956">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-956">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="cd182-957">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="cd182-957">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd182-958">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="cd182-958">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd182-959">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="cd182-959">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd182-960">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="cd182-960">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="cd182-961">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-961">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="cd182-962">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-962">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cd182-963">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="cd182-963">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="cd182-964">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd182-964">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="cd182-965">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="cd182-965">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="cd182-966">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="cd182-966">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="cd182-967">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-967">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="cd182-968">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="cd182-968">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="cd182-969">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="cd182-969">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="cd182-970">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="cd182-970">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="cd182-971">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="cd182-971">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="cd182-972">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-972">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="cd182-973">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="cd182-973">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="cd182-974">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="cd182-974">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="cd182-975">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="cd182-975">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cd182-976">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="cd182-976">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cd182-977">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="cd182-977">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="cd182-978">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="cd182-978">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="cd182-979">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-979">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd182-980">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-980">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd182-981">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-981">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd182-982">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-982">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd182-983">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-983">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd182-984">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-984">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="cd182-985">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-985">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="cd182-986">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="cd182-986">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="cd182-987">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-987">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd182-988">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-988">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd182-989">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-989">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd182-990">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-990">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="cd182-991">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-991">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="cd182-992">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-992">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cd182-993">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-993">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cd182-994">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-994">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd182-995">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-995">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd182-996">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-996">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="cd182-997">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-997">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="cd182-998">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-998">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="cd182-999">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-999">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-1000">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1000">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-1001">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="cd182-1001">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="cd182-1002">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="cd182-1002">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="cd182-1003">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="cd182-1003">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="cd182-1004">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="cd182-1004">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cd182-1005">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="cd182-1005">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1006">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1006">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1007">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1007">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="cd182-1008">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="cd182-1008">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1009">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1009">Az.Resources</span></span>
* <span data-ttu-id="cd182-1010">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="cd182-1010">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="cd182-1011">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="cd182-1011">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="cd182-1012">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="cd182-1012">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="cd182-1013">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1013">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="cd182-1014">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1014">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="cd182-1015">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1015">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1016">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1016">Az.Sql</span></span>
* <span data-ttu-id="cd182-1017">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1017">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="cd182-1018">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-1018">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="cd182-1019">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="cd182-1019">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1020">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1020">Az.Storage</span></span>
* <span data-ttu-id="cd182-1021">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1021">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="cd182-1022">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1022">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-1023">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1023">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-1024">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1024">Az.Websites</span></span>
* <span data-ttu-id="cd182-1025">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="cd182-1025">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cd182-1026">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="cd182-1026">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="cd182-1027">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-1027">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="cd182-1028">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-1028">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="cd182-1029">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1029">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="cd182-1030">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="cd182-1030">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="cd182-1031">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1031">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-1032">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1032">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1033">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="cd182-1033">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-1034">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1034">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd182-1035">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1035">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-1036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-1036">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-1037">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1037">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cd182-1038">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd182-1038">Az.Billing</span></span>
* <span data-ttu-id="cd182-1039">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1039">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-1040">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1040">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-1041">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="cd182-1041">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1042">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1043">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1043">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="cd182-1044">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="cd182-1044">Az.DataShare</span></span>
* <span data-ttu-id="cd182-1045">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="cd182-1045">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cd182-1046">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cd182-1046">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cd182-1047">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="cd182-1047">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-1048">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1048">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-1049">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1049">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="cd182-1050">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="cd182-1050">Added optional parameters to</span></span> 
    - <span data-ttu-id="cd182-1051">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="cd182-1051">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cd182-1052">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="cd182-1052">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-1053">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1053">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-1054">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="cd182-1054">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cd182-1055">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cd182-1055">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cd182-1056">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1056">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cd182-1057">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cd182-1057">Az.PrivateDns</span></span>
* <span data-ttu-id="cd182-1058">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="cd182-1058">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1060">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="cd182-1060">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="cd182-1061">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1061">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1062">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1062">Az.Resources</span></span>
* <span data-ttu-id="cd182-1063">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1063">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="cd182-1064">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="cd182-1064">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="cd182-1065">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="cd182-1065">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="cd182-1066">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-1066">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="cd182-1067">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1067">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1068">Az.Sql</span></span>
* <span data-ttu-id="cd182-1069">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="cd182-1069">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cd182-1070">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="cd182-1070">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cd182-1071">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1071">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1072">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1072">Az.Storage</span></span>
* <span data-ttu-id="cd182-1073">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1073">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="cd182-1074">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1074">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cd182-1075">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-1075">Highlights since the last release</span></span>
* <span data-ttu-id="cd182-1076">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cd182-1076">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="cd182-1077">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="cd182-1077">General availability of Az.Functions</span></span> 
* <span data-ttu-id="cd182-1078">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1078">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1079">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1080">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-1080">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="cd182-1081">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="cd182-1081">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-1082">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-1082">Az.Aks</span></span>
* <span data-ttu-id="cd182-1083">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="cd182-1083">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="cd182-1084">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="cd182-1084">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="cd182-1085">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="cd182-1085">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-1086">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-1086">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-1087">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="cd182-1087">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="cd182-1088">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="cd182-1088">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="cd182-1089">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1089">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd182-1090">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="cd182-1090">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd182-1091">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1091">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd182-1092">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="cd182-1092">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="cd182-1093">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1093">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd182-1094">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="cd182-1094">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd182-1095">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1095">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd182-1096">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="cd182-1096">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd182-1097">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="cd182-1097">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="cd182-1098">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="cd182-1098">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="cd182-1099">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="cd182-1099">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="cd182-1100">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd182-1100">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="cd182-1101">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd182-1101">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="cd182-1102">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd182-1102">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cd182-1103">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1103">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cd182-1104">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="cd182-1104">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="cd182-1105">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="cd182-1105">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="cd182-1106">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1106">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-1107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-1107">Az.Batch</span></span>
* <span data-ttu-id="cd182-1108">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="cd182-1108">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="cd182-1109">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="cd182-1109">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="cd182-1110">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1110">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="cd182-1111">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1111">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="cd182-1112">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1112">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="cd182-1113">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="cd182-1113">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="cd182-1114">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="cd182-1114">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="cd182-1115">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1115">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="cd182-1116">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1116">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1117">Az.Compute</span></span>
* <span data-ttu-id="cd182-1118">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1118">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="cd182-1119">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1119">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="cd182-1120">重大變更</span><span class="sxs-lookup"><span data-stu-id="cd182-1120">Breaking changes</span></span>
    - <span data-ttu-id="cd182-1121">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-1121">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="cd182-1122">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-1122">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="cd182-1123">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="cd182-1123">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="cd182-1124">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="cd182-1124">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="cd182-1125">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1125">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="cd182-1126">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="cd182-1126">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="cd182-1127">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="cd182-1127">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1128">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1129">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="cd182-1129">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-1130">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-1130">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-1131">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1131">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cd182-1132">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1132">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cd182-1133">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1133">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="cd182-1134">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="cd182-1134">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd182-1135">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd182-1135">Az.Functions</span></span>
* <span data-ttu-id="cd182-1136">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="cd182-1136">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-1137">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-1137">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-1138">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="cd182-1138">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd182-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd182-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd182-1140">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="cd182-1140">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1141">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1141">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1142">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="cd182-1142">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="cd182-1143">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="cd182-1143">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="cd182-1144">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="cd182-1144">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="cd182-1145">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="cd182-1145">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="cd182-1146">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="cd182-1146">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="cd182-1147">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1147">New cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1148">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1148">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd182-1149">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1149">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd182-1150">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1150">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd182-1151">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1151">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="cd182-1152">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="cd182-1152">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="cd182-1153">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="cd182-1153">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1154">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1155">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="cd182-1155">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="cd182-1156">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="cd182-1156">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="cd182-1157">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="cd182-1157">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="cd182-1158">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1158">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="cd182-1159">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="cd182-1159">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="cd182-1160">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="cd182-1160">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="cd182-1161">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="cd182-1161">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1162">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1163">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="cd182-1163">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="cd182-1164">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="cd182-1164">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="cd182-1165">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="cd182-1165">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="cd182-1166">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="cd182-1166">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="cd182-1167">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="cd182-1167">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="cd182-1168">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="cd182-1168">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="cd182-1169">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="cd182-1169">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1170">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1170">Az.Network</span></span>
* <span data-ttu-id="cd182-1171">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="cd182-1171">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="cd182-1172">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="cd182-1172">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="cd182-1173">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="cd182-1173">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="cd182-1174">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-1174">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="cd182-1175">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1175">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="cd182-1176">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1176">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-1177">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd182-1177">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd182-1178">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd182-1178">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd182-1179">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd182-1179">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd182-1180">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd182-1180">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="cd182-1181">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="cd182-1181">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="cd182-1182">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="cd182-1182">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="cd182-1183">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="cd182-1183">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="cd182-1184">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="cd182-1184">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="cd182-1185">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="cd182-1185">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="cd182-1186">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="cd182-1186">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="cd182-1187">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-1187">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="cd182-1188">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="cd182-1188">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd182-1189">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="cd182-1189">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd182-1190">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="cd182-1190">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd182-1191">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="cd182-1191">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="cd182-1192">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="cd182-1192">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="cd182-1193">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="cd182-1193">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="cd182-1194">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1194">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd182-1195">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cd182-1195">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-1196">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1196">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-1197">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="cd182-1197">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="cd182-1198">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1198">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="cd182-1199">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="cd182-1199">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="cd182-1200">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="cd182-1200">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="cd182-1201">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="cd182-1201">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="cd182-1202">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="cd182-1202">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="cd182-1203">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1203">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="cd182-1204">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1204">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1205">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1206">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="cd182-1206">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="cd182-1207">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="cd182-1207">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="cd182-1208">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1208">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="cd182-1209">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="cd182-1209">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="cd182-1210">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="cd182-1210">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1211">Az.Resources</span></span>
* <span data-ttu-id="cd182-1212">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="cd182-1212">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="cd182-1213">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="cd182-1213">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="cd182-1214">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="cd182-1214">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="cd182-1215">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="cd182-1215">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="cd182-1216">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="cd182-1216">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="cd182-1217">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="cd182-1217">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="cd182-1218">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="cd182-1218">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="cd182-1219">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="cd182-1219">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cd182-1220">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1220">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="cd182-1221">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="cd182-1221">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="cd182-1222">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="cd182-1222">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="cd182-1223">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="cd182-1223">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="cd182-1224">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="cd182-1224">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="cd182-1225">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="cd182-1225">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="cd182-1226">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="cd182-1226">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="cd182-1227">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="cd182-1227">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="cd182-1228">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1228">'New-AzDeployment'</span></span>
    - <span data-ttu-id="cd182-1229">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1229">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="cd182-1230">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1230">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cd182-1231">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="cd182-1231">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-1232">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-1232">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-1233">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="cd182-1233">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1234">Az.Sql</span></span>
* <span data-ttu-id="cd182-1235">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="cd182-1235">Enhance performance of:</span></span>
    - <span data-ttu-id="cd182-1236">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="cd182-1236">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd182-1237">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="cd182-1237">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd182-1238">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="cd182-1238">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd182-1239">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="cd182-1239">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd182-1240">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="cd182-1240">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd182-1241">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="cd182-1241">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd182-1242">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="cd182-1242">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd182-1243">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="cd182-1243">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="cd182-1244">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-1244">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="cd182-1245">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-1245">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1246">Az.Storage</span></span>
* <span data-ttu-id="cd182-1247">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1247">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-1248">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="cd182-1248">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="cd182-1249">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1249">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-1250">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-1250">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="cd182-1251">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="cd182-1251">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cd182-1252">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="cd182-1252">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="cd182-1253">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="cd182-1253">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="cd182-1254">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="cd182-1254">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="cd182-1255">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="cd182-1255">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="cd182-1256">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="cd182-1256">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="cd182-1257">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="cd182-1257">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="cd182-1258">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="cd182-1258">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="cd182-1259">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="cd182-1259">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="cd182-1260">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1260">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="cd182-1261">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1261">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cd182-1262">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1262">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-1263">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="cd182-1263">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="cd182-1264">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="cd182-1264">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="cd182-1265">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="cd182-1265">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cd182-1266">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1266">Supported failover Storage account</span></span>
    - <span data-ttu-id="cd182-1267">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="cd182-1267">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="cd182-1268">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-1268">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="cd182-1269">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-1269">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="cd182-1270">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1270">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="cd182-1271">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1271">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd182-1272">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="cd182-1272">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="cd182-1273">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="cd182-1273">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="cd182-1274">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-1274">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cd182-1275">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-1275">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cd182-1276">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="cd182-1276">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="cd182-1277">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1277">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd182-1278">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="cd182-1278">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="cd182-1279">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="cd182-1279">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cd182-1280">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1280">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd182-1281">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-1281">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="cd182-1282">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-1282">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="cd182-1283">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-1283">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="cd182-1284">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1284">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="cd182-1285">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="cd182-1285">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cd182-1286">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd182-1286">Az.TrafficManager</span></span>
* <span data-ttu-id="cd182-1287">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-1287">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-1288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1288">Az.Websites</span></span>
* <span data-ttu-id="cd182-1289">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="cd182-1289">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="cd182-1290">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1290">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cd182-1291">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-1291">Highlights since the last release</span></span>
* <span data-ttu-id="cd182-1292">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cd182-1292">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1293">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1294">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="cd182-1294">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-1295">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-1295">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-1296">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="cd182-1296">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cd182-1297">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-1297">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-1298">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-1298">Az.Cdn</span></span>
* <span data-ttu-id="cd182-1299">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="cd182-1299">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-1300">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1300">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-1301">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="cd182-1301">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1302">Az.Compute</span></span>
* <span data-ttu-id="cd182-1303">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-1303">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="cd182-1304">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="cd182-1304">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1305">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1305">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1306">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1306">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1307">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="cd182-1307">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="cd182-1308">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="cd182-1308">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="cd182-1309">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="cd182-1309">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="cd182-1310">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1310">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1311">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="cd182-1311">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="cd182-1312">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="cd182-1312">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="cd182-1313">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="cd182-1313">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="cd182-1314">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1314">New cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1315">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-1315">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd182-1316">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-1316">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd182-1317">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-1317">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd182-1318">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cd182-1318">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="cd182-1319">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="cd182-1319">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1320">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1320">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1321">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="cd182-1321">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="cd182-1322">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="cd182-1322">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="cd182-1323">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="cd182-1323">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="cd182-1324">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="cd182-1324">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cd182-1325">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cd182-1325">Az.Maintenance</span></span>
* <span data-ttu-id="cd182-1326">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1326">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1327">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1327">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1328">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1328">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="cd182-1329">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-1329">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd182-1330">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-1330">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd182-1331">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-1331">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd182-1332">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cd182-1332">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd182-1333">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cd182-1333">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cd182-1334">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cd182-1334">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cd182-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cd182-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1336">Az.Network</span></span>
* <span data-ttu-id="cd182-1337">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="cd182-1337">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="cd182-1338">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-1338">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cd182-1339">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-1339">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cd182-1340">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-1340">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="cd182-1341">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-1341">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="cd182-1342">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="cd182-1342">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="cd182-1343">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cd182-1343">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="cd182-1344">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="cd182-1344">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="cd182-1345">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="cd182-1345">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="cd182-1346">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-1346">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cd182-1347">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="cd182-1347">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="cd182-1348">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cd182-1348">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cd182-1349">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="cd182-1349">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="cd182-1350">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="cd182-1350">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="cd182-1351">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1351">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="cd182-1352">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1352">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-1353">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1353">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-1354">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1354">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="cd182-1355">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="cd182-1355">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-1356">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-1356">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-1357">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-1357">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1358">Az.Sql</span></span>
* <span data-ttu-id="cd182-1359">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1359">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="cd182-1360">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="cd182-1360">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1361">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1361">Az.Storage</span></span>
* <span data-ttu-id="cd182-1362">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="cd182-1362">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cd182-1363">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="cd182-1363">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="cd182-1364">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1364">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="cd182-1365">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1365">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd182-1366">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="cd182-1366">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="cd182-1367">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-1367">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd182-1368">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-1368">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd182-1369">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="cd182-1369">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="cd182-1370">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-1370">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd182-1371">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="cd182-1371">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="cd182-1372">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-1372">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd182-1373">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="cd182-1373">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="cd182-1374">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cd182-1374">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="cd182-1375">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1375">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="cd182-1376">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-1376">General</span></span>
* <span data-ttu-id="cd182-1377">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="cd182-1377">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="cd182-1378">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1378">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="cd182-1379">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="cd182-1379">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="cd182-1380">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="cd182-1380">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="cd182-1381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd182-1381">Az.Billing</span></span>
  - <span data-ttu-id="cd182-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1382">Az.Compute</span></span>
  - <span data-ttu-id="cd182-1383">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd182-1383">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="cd182-1384">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1384">Az.EventHub</span></span>
  - <span data-ttu-id="cd182-1385">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1385">Az.IotHub</span></span>
  - <span data-ttu-id="cd182-1386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1386">Az.KeyVault</span></span>
  - <span data-ttu-id="cd182-1387">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1387">Az.Monitor</span></span>
  - <span data-ttu-id="cd182-1388">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1388">Az.Network</span></span>
  - <span data-ttu-id="cd182-1389">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1389">Az.Resources</span></span>
  - <span data-ttu-id="cd182-1390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1390">Az.Storage</span></span>
  - <span data-ttu-id="cd182-1391">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1391">Az.Websites</span></span>
* <span data-ttu-id="cd182-1392">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1392">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="cd182-1393">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="cd182-1393">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="cd182-1394">您可以在[這裡](/azure-stack/operator/powershell-install-az-module)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="cd182-1394">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="cd182-1395">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1395">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-1396">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1396">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1397">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="cd182-1397">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1398">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1398">Az.Compute</span></span>
* <span data-ttu-id="cd182-1399">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1399">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="cd182-1400">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="cd182-1400">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="cd182-1401">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1401">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="cd182-1402">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-1402">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="cd182-1403">[#11354]</span><span class="sxs-lookup"><span data-stu-id="cd182-1403">[#11354]</span></span>
* <span data-ttu-id="cd182-1404">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1404">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="cd182-1405">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-1405">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd182-1406">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-1406">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd182-1407">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-1407">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd182-1408">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="cd182-1408">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="cd182-1409">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-1409">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="cd182-1410">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="cd182-1410">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="cd182-1411">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="cd182-1411">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="cd182-1412">[#11257]</span><span class="sxs-lookup"><span data-stu-id="cd182-1412">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1413">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1414">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1414">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="cd182-1415">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="cd182-1415">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-1416">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-1416">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-1417">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="cd182-1417">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="cd182-1418">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="cd182-1418">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-1419">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-1419">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-1420">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="cd182-1420">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1421">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1421">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1422">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1422">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="cd182-1423">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1423">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1424">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="cd182-1424">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="cd182-1425">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="cd182-1425">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1426">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1427">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="cd182-1427">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1428">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1429">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="cd182-1429">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1430">Az.Network</span></span>
* <span data-ttu-id="cd182-1431">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="cd182-1431">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="cd182-1432">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-1432">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd182-1433">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="cd182-1433">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd182-1434">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="cd182-1434">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="cd182-1435">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="cd182-1435">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cd182-1436">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-1436">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-1437">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1437">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-1438">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1438">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1439">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1440">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1440">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="cd182-1441">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="cd182-1441">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="cd182-1442">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1442">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="cd182-1443">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1443">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="cd182-1444">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1444">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="cd182-1445">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1445">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1446">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1446">Az.Resources</span></span>
* <span data-ttu-id="cd182-1447">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="cd182-1447">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="cd182-1448">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="cd182-1448">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="cd182-1449">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1449">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="cd182-1450">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1450">Added example.</span></span>
* <span data-ttu-id="cd182-1451">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="cd182-1451">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="cd182-1452">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1452">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1453">Az.Sql</span></span>
* <span data-ttu-id="cd182-1454">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="cd182-1454">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="cd182-1455">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="cd182-1455">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd182-1456">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="cd182-1456">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="cd182-1457">Az.Support</span><span class="sxs-lookup"><span data-stu-id="cd182-1457">Az.Support</span></span>
* <span data-ttu-id="cd182-1458">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-1458">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1459">Az.Websites</span></span>
* <span data-ttu-id="cd182-1460">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1460">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="cd182-1461">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="cd182-1461">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd182-1462">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="cd182-1462">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd182-1463">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="cd182-1463">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd182-1464">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="cd182-1464">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="cd182-1465">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1465">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1466">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1467">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="cd182-1467">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="cd182-1468">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="cd182-1468">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="cd182-1469">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1469">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-1470">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-1470">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-1471">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="cd182-1471">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="cd182-1472">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="cd182-1472">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="cd182-1473">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1473">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="cd182-1474">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="cd182-1474">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-1475">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-1475">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-1476">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="cd182-1476">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1477">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1478">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1478">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cd182-1479">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1479">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1480">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1480">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1481">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1481">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1482">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1482">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1483">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1483">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="cd182-1484">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1484">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="cd182-1485">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1485">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1486">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="cd182-1486">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd182-1487">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="cd182-1487">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd182-1488">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="cd182-1488">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd182-1489">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="cd182-1489">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="cd182-1490">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="cd182-1490">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cd182-1491">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="cd182-1491">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cd182-1492">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1492">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="cd182-1493">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1493">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1494">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="cd182-1494">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="cd182-1495">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="cd182-1495">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="cd182-1496">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1496">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1497">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1498">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="cd182-1498">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1499">Az.Network</span></span>
* <span data-ttu-id="cd182-1500">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-1500">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="cd182-1501">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-1501">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="cd182-1502">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="cd182-1502">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="cd182-1503">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1503">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1504">Az.Resources</span></span>
* <span data-ttu-id="cd182-1505">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-1505">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="cd182-1506">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="cd182-1506">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="cd182-1507">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="cd182-1507">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="cd182-1508">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="cd182-1508">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="cd182-1509">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-1509">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="cd182-1510">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1510">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="cd182-1511">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="cd182-1511">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="cd182-1512">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd182-1512">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="cd182-1513">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd182-1513">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cd182-1514">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd182-1514">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cd182-1515">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd182-1515">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="cd182-1516">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1516">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="cd182-1517">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd182-1517">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="cd182-1518">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="cd182-1518">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1519">Az.Sql</span></span>
* <span data-ttu-id="cd182-1520">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1520">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cd182-1521">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1521">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="cd182-1522">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="cd182-1522">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="cd182-1523">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="cd182-1523">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="cd182-1524">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="cd182-1524">Remove an LTR backup</span></span>
    - <span data-ttu-id="cd182-1525">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="cd182-1525">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="cd182-1526">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="cd182-1526">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="cd182-1527">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-1527">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="cd182-1528">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-1528">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1529">Az.Storage</span></span>
* <span data-ttu-id="cd182-1530">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="cd182-1530">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="cd182-1531">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-1531">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="cd182-1532">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1532">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="cd182-1533">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-1533">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="cd182-1534">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="cd182-1534">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-1535">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1535">Az.Websites</span></span>
* <span data-ttu-id="cd182-1536">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="cd182-1536">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="cd182-1537">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1537">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="cd182-1538">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="cd182-1538">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="cd182-1539">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="cd182-1539">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="cd182-1540">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-1540">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="cd182-1541">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1541">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-1542">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-1542">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-1543">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="cd182-1543">Updated client side telemetry.</span></span>
* <span data-ttu-id="cd182-1544">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="cd182-1544">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="cd182-1545">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-1545">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1546">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1547">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="cd182-1547">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-1548">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-1548">Az.Automation</span></span>
* <span data-ttu-id="cd182-1549">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-1549">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-1551">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1551">Updated SDK to 7.0</span></span>
* <span data-ttu-id="cd182-1552">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1552">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1553">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1553">Az.Compute</span></span>
* <span data-ttu-id="cd182-1554">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="cd182-1554">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-1555">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-1555">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-1556">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="cd182-1556">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1557">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1557">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1558">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1558">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cd182-1559">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-1559">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd182-1560">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1560">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1561">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1561">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1562">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1562">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd182-1563">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="cd182-1563">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1564">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1564">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1565">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="cd182-1565">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1566">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1566">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1567">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="cd182-1567">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="cd182-1568">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="cd182-1568">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="cd182-1569">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="cd182-1569">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1570">Az.Network</span></span>
* <span data-ttu-id="cd182-1571">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="cd182-1571">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="cd182-1572">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1572">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cd182-1573">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="cd182-1573">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cd182-1574">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="cd182-1574">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="cd182-1575">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-1575">No new cmdlets are added.</span></span> <span data-ttu-id="cd182-1576">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="cd182-1576">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1577">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1577">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1578">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1578">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1579">Az.Resources</span></span>
* <span data-ttu-id="cd182-1580">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1580">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="cd182-1581">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cd182-1581">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="cd182-1582">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cd182-1582">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="cd182-1583">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="cd182-1583">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="cd182-1584">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="cd182-1584">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="cd182-1585">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="cd182-1585">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="cd182-1586">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="cd182-1586">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="cd182-1587">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="cd182-1587">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1588">Az.Sql</span></span>
* <span data-ttu-id="cd182-1589">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1589">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="cd182-1590">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1590">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="cd182-1591">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="cd182-1591">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cd182-1592">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd182-1592">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cd182-1593">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1593">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-1594">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-1594">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-1595">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="cd182-1595">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="cd182-1596">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1596">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-1597">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-1598">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="cd182-1598">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="cd182-1599">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="cd182-1599">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1600">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1601">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="cd182-1601">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="cd182-1602">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="cd182-1602">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-1603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-1603">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-1604">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="cd182-1604">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="cd182-1605">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="cd182-1605">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="cd182-1606"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="cd182-1606">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="cd182-1607">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="cd182-1607">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1608">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1608">Az.Compute</span></span>
* <span data-ttu-id="cd182-1609">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="cd182-1609">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="cd182-1610">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1610">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="cd182-1611">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1611">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="cd182-1612">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-1612">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="cd182-1613">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-1613">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1614">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1614">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1615">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1615">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cd182-1616">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cd182-1616">Az.DeploymentManager</span></span>
* <span data-ttu-id="cd182-1617">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="cd182-1617">Adds LIST operations for resources</span></span>
* <span data-ttu-id="cd182-1618">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="cd182-1618">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-1619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-1619">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-1620">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-1620">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1621">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1621">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1622">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="cd182-1622">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1623">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1623">Az.Network</span></span>
* <span data-ttu-id="cd182-1624">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1624">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="cd182-1625">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="cd182-1625">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="cd182-1626">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1626">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cd182-1627">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="cd182-1627">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="cd182-1628">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="cd182-1628">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="cd182-1629">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1629">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="cd182-1630">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="cd182-1630">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="cd182-1631">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1631">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="cd182-1632">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1632">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="cd182-1634">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1634">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="cd182-1635">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cd182-1635">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="cd182-1636">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1636">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-1637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-1637">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-1638">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="cd182-1638">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="cd182-1639">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="cd182-1639">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="cd182-1640">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="cd182-1640">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="cd182-1641">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="cd182-1641">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1642">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1642">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1643">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="cd182-1643">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="cd182-1644">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1644">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1645">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1645">Az.Resources</span></span>
* <span data-ttu-id="cd182-1646">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="cd182-1646">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="cd182-1647">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-1647">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1648">Az.Sql</span></span>
<span data-ttu-id="cd182-1649">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="cd182-1649">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1650">Az.Storage</span></span>
* <span data-ttu-id="cd182-1651">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="cd182-1651">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="cd182-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd182-1653">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="cd182-1653">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="cd182-1654">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="cd182-1654">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-1655">Az.Websites</span></span>
* <span data-ttu-id="cd182-1656">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1656">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="cd182-1657">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-1657">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="cd182-1658">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1658">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-1659">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1659">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1660">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-1660">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-1661">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-1661">Az.Cdn</span></span>
* <span data-ttu-id="cd182-1662">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="cd182-1662">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1663">Az.Compute</span></span>
* <span data-ttu-id="cd182-1664">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-1664">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cd182-1665">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-1665">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd182-1666">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-1666">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cd182-1667">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd182-1667">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cd182-1668">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1668">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd182-1669">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="cd182-1669">Get the Edge Storage Container</span></span>
* <span data-ttu-id="cd182-1670">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1670">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd182-1671">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="cd182-1671">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="cd182-1672">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1672">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd182-1673">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="cd182-1673">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="cd182-1674">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="cd182-1674">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd182-1675">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="cd182-1675">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="cd182-1676">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1676">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd182-1677">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1677">Get the Edge Storage Account</span></span>
* <span data-ttu-id="cd182-1678">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1678">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd182-1679">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1679">Create new Edge Storage Account</span></span>
* <span data-ttu-id="cd182-1680">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cd182-1680">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd182-1681">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-1681">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="cd182-1682">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="cd182-1682">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="cd182-1683">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="cd182-1683">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="cd182-1684">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="cd182-1684">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="cd182-1685">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="cd182-1685">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1686">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1687">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-1687">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="cd182-1688">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1688">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="cd182-1689">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="cd182-1689">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="cd182-1690">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cd182-1690">Az.DevTestLabs</span></span>
* <span data-ttu-id="cd182-1691">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="cd182-1691">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-1692">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1692">Az.EventHub</span></span>
* <span data-ttu-id="cd182-1693">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="cd182-1693">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-1694">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-1694">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-1695">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-1695">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cd182-1696">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd182-1696">Az.MachineLearning</span></span>
* <span data-ttu-id="cd182-1697">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1697">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="cd182-1698">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd182-1698">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd182-1699">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="cd182-1699">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="cd182-1700">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd182-1700">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd182-1701">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd182-1701">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd182-1702">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd182-1702">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd182-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="cd182-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="cd182-1704">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="cd182-1704">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1705">Az.Network</span></span>
* <span data-ttu-id="cd182-1706">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="cd182-1706">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1707">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1708">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="cd182-1708">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="cd182-1709">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="cd182-1709">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cd182-1710">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="cd182-1710">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cd182-1711">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="cd182-1711">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1712">Az.Resources</span></span>
* <span data-ttu-id="cd182-1713">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-1713">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1714">Az.Sql</span></span>
* <span data-ttu-id="cd182-1715">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="cd182-1715">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="cd182-1716">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-1716">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cd182-1717">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd182-1717">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cd182-1718">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="cd182-1718">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1719">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1719">Az.Storage</span></span>
* <span data-ttu-id="cd182-1720">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1720">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="cd182-1721">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-1721">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="cd182-1722">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="cd182-1722">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="cd182-1723">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-1723">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="cd182-1724">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1724">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="cd182-1725">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-1725">General</span></span>
* <span data-ttu-id="cd182-1726">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="cd182-1726">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1727">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1727">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1728">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="cd182-1728">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="cd182-1729">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-1729">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-1730">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-1730">Az.Batch</span></span>
* <span data-ttu-id="cd182-1731">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd182-1731">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1732">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1732">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1733">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1733">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-1734">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-1734">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-1735">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1735">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="cd182-1736">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="cd182-1736">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd182-1737">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd182-1737">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd182-1738">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="cd182-1738">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-1739">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-1739">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-1740">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-1740">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="cd182-1741">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="cd182-1741">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="cd182-1742">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1742">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-1743">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-1743">Az.Monitor</span></span>
* <span data-ttu-id="cd182-1744">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="cd182-1744">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="cd182-1745">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="cd182-1745">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="cd182-1746">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="cd182-1746">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1747">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1747">Az.Network</span></span>
* <span data-ttu-id="cd182-1748">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="cd182-1748">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1749">Az.Resources</span></span>
* <span data-ttu-id="cd182-1750">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-1750">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="cd182-1751">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1751">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1752">Az.Sql</span></span>
* <span data-ttu-id="cd182-1753">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="cd182-1753">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-1754">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-1754">Az.Storage</span></span>
* <span data-ttu-id="cd182-1755">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-1755">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="cd182-1756">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cd182-1756">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="cd182-1757">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd182-1757">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="cd182-1758">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-1758">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="cd182-1759">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="cd182-1759">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="cd182-1760">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="cd182-1760">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="cd182-1761">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="cd182-1761">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="cd182-1762">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-1762">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="cd182-1763">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-1763">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="cd182-1764">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="cd182-1764">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="cd182-1765">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="cd182-1765">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="cd182-1766">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-1766">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="cd182-1767">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="cd182-1767">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="cd182-1768">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1768">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-1769">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-1769">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-1770">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1770">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="cd182-1771">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1771">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1772">Az.Compute</span></span>
* <span data-ttu-id="cd182-1773">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="cd182-1773">VM Reapply feature</span></span>
    - <span data-ttu-id="cd182-1774">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1774">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="cd182-1775">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="cd182-1775">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="cd182-1776">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd182-1776">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="cd182-1777">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1777">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="cd182-1778">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="cd182-1778">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd182-1779">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1779">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="cd182-1780">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="cd182-1780">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="cd182-1781">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1781">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="cd182-1782">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1782">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="cd182-1783">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1783">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cd182-1784">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd182-1784">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cd182-1785">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="cd182-1785">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd182-1786">取得訂單</span><span class="sxs-lookup"><span data-stu-id="cd182-1786">Get the Order</span></span>
* <span data-ttu-id="cd182-1787">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="cd182-1787">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd182-1788">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="cd182-1788">Create new Order</span></span>
* <span data-ttu-id="cd182-1789">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="cd182-1789">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd182-1790">移除訂單</span><span class="sxs-lookup"><span data-stu-id="cd182-1790">Remove the Order</span></span>
* <span data-ttu-id="cd182-1791">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="cd182-1791">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="cd182-1792">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="cd182-1792">Now creates Local Share</span></span>
* <span data-ttu-id="cd182-1793">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="cd182-1793">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="cd182-1794">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="cd182-1794">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="cd182-1795">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="cd182-1795">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="cd182-1796">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="cd182-1796">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="cd182-1797">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="cd182-1797">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd182-1798">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-1798">Gets the information about Triggers</span></span>
* <span data-ttu-id="cd182-1799">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="cd182-1799">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd182-1800">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="cd182-1800">Create new Triggers</span></span>
* <span data-ttu-id="cd182-1801">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="cd182-1801">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd182-1802">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="cd182-1802">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1803">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1803">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1804">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1804">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="cd182-1805">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1805">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-1806">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-1806">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-1807">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="cd182-1807">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-1808">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1808">Az.EventHub</span></span>
* <span data-ttu-id="cd182-1809">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="cd182-1809">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-1810">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-1810">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-1811">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="cd182-1811">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="cd182-1812">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="cd182-1812">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="cd182-1813">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="cd182-1813">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="cd182-1814">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="cd182-1814">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1815">Az.Network</span></span>
* <span data-ttu-id="cd182-1816">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1816">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cd182-1817">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cd182-1817">Az.PrivateDns</span></span>
* <span data-ttu-id="cd182-1818">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="cd182-1818">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1819">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1820">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="cd182-1820">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="cd182-1821">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="cd182-1821">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="cd182-1822">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="cd182-1822">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd182-1823">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd182-1823">Az.RedisCache</span></span>
* <span data-ttu-id="cd182-1824">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-1824">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="cd182-1825">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1825">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="cd182-1826">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-1826">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1827">Az.Resources</span></span>
- <span data-ttu-id="cd182-1828">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1828">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="cd182-1829">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="cd182-1829">Updated create policy definition help example</span></span>
- <span data-ttu-id="cd182-1830">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="cd182-1830">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="cd182-1831">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="cd182-1831">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="cd182-1832">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd182-1832">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-1833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-1833">Az.Sql</span></span>
* <span data-ttu-id="cd182-1834">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1834">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="cd182-1835">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd182-1835">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="cd182-1836">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cd182-1836">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="cd182-1837">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-1837">General</span></span>
* <span data-ttu-id="cd182-1838">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1838">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-1839">Az.Accounts</span></span>
* <span data-ttu-id="cd182-1840">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-1840">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cd182-1841">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cd182-1841">Az.Advisor</span></span>
* <span data-ttu-id="cd182-1842">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="cd182-1842">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-1843">Az.Batch</span></span>
* <span data-ttu-id="cd182-1844">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1844">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="cd182-1845">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1845">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="cd182-1846">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="cd182-1846">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="cd182-1847">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="cd182-1847">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="cd182-1848">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1848">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="cd182-1849">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="cd182-1849">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="cd182-1850">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="cd182-1850">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="cd182-1851">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="cd182-1851">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="cd182-1852">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="cd182-1852">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="cd182-1853">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1853">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cd182-1854">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1854">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="cd182-1855">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="cd182-1855">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="cd182-1856">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1856">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cd182-1857">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-1857">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="cd182-1858">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1858">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="cd182-1859">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1859">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="cd182-1860">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1860">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="cd182-1861">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-1861">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="cd182-1862">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="cd182-1862">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="cd182-1863">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="cd182-1863">This operation is no longer supported.</span></span>
* <span data-ttu-id="cd182-1864">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1864">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cd182-1865">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1865">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cd182-1866">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="cd182-1866">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="cd182-1867">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="cd182-1867">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="cd182-1868">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="cd182-1868">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="cd182-1869">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="cd182-1869">New non-verified images are also now returned.</span></span> <span data-ttu-id="cd182-1870">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd182-1870">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="cd182-1871">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="cd182-1871">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="cd182-1872">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="cd182-1872">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="cd182-1873">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="cd182-1873">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="cd182-1874">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="cd182-1874">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="cd182-1875">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="cd182-1875">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="cd182-1876">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="cd182-1876">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="cd182-1877">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="cd182-1877">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="cd182-1878">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="cd182-1878">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="cd182-1879">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="cd182-1879">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-1880">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-1880">Az.Cdn</span></span>
* <span data-ttu-id="cd182-1881">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="cd182-1881">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="cd182-1882">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="cd182-1882">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-1883">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-1883">Az.Compute</span></span>
* <span data-ttu-id="cd182-1884">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="cd182-1884">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="cd182-1885">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cd182-1885">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="cd182-1886">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cd182-1886">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="cd182-1887">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-1887">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd182-1888">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-1888">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="cd182-1889">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="cd182-1889">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="cd182-1890">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-1890">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd182-1891">重大變更</span><span class="sxs-lookup"><span data-stu-id="cd182-1891">Breaking changes</span></span>
    - <span data-ttu-id="cd182-1892">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cd182-1892">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="cd182-1893">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="cd182-1893">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-1894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-1894">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-1895">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1895">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-1896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-1896">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-1897">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="cd182-1897">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="cd182-1898">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cd182-1898">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="cd182-1899">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="cd182-1899">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="cd182-1900">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="cd182-1900">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="cd182-1901">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-1901">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="cd182-1902">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-1902">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-1903">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-1903">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-1904">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="cd182-1904">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-1905">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-1905">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-1906">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-1906">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="cd182-1907">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="cd182-1907">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="cd182-1908">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="cd182-1908">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="cd182-1909">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1909">Removed five cmdlets:</span></span>
    - <span data-ttu-id="cd182-1910">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd182-1910">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd182-1911">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd182-1911">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd182-1912">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd182-1912">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd182-1913">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd182-1913">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="cd182-1914">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd182-1914">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="cd182-1915">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1915">Added three cmdlets:</span></span>
    - <span data-ttu-id="cd182-1916">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="cd182-1916">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cd182-1917">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="cd182-1917">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cd182-1918">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="cd182-1918">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="cd182-1919">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="cd182-1919">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="cd182-1920">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="cd182-1920">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="cd182-1921">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="cd182-1921">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="cd182-1922">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="cd182-1922">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="cd182-1923">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="cd182-1923">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="cd182-1924">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="cd182-1924">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="cd182-1925">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="cd182-1925">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="cd182-1926">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="cd182-1926">Added some scenario test cases.</span></span>
* <span data-ttu-id="cd182-1927">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="cd182-1927">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-1928">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1928">Az.IotHub</span></span>
* <span data-ttu-id="cd182-1929">重大變更：</span><span class="sxs-lookup"><span data-stu-id="cd182-1929">Breaking changes:</span></span>
    - <span data-ttu-id="cd182-1930">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-1930">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd182-1931">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1931">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd182-1932">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-1932">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd182-1933">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1933">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd182-1934">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1934">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="cd182-1935">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1935">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="cd182-1936">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1936">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="cd182-1937">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1937">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="cd182-1938">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-1938">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd182-1939">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1939">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd182-1940">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-1940">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd182-1941">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="cd182-1941">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-1942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-1942">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-1943">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="cd182-1943">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1944">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="cd182-1944">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="cd182-1945">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="cd182-1945">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="cd182-1946">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="cd182-1946">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1947">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="cd182-1947">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1948">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="cd182-1948">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1949">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="cd182-1949">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1950">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-1950">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-1951">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="cd182-1951">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-1952">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-1952">Az.Resources</span></span>
* <span data-ttu-id="cd182-1953">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="cd182-1953">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-1954">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-1954">Az.Network</span></span>
* <span data-ttu-id="cd182-1955">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cd182-1955">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="cd182-1956">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1956">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd182-1957">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1957">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-1958">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1958">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-1959">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1959">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-1960">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1960">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-1961">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1961">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cd182-1962">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cd182-1962">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="cd182-1963">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1963">New cmdlet:</span></span>
        - <span data-ttu-id="cd182-1964">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="cd182-1964">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="cd182-1965">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-1965">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="cd182-1966">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="cd182-1966">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="cd182-1967">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="cd182-1967">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="cd182-1968">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="cd182-1968">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="cd182-1969">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="cd182-1969">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="cd182-1970">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="cd182-1970">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="cd182-1971">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1971">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="cd182-1972">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1972">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-1973">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="cd182-1973">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="cd182-1974">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-1974">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd182-1975">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-1975">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd182-1976">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-1976">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd182-1977">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cd182-1977">Set-AzVirtualHub</span></span>
* <span data-ttu-id="cd182-1978">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1978">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="cd182-1979">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1979">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd182-1980">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="cd182-1980">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cd182-1981">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="cd182-1981">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cd182-1982">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cd182-1982">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="cd182-1983">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cd182-1983">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="cd182-1984">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1984">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="cd182-1985">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1985">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-1986">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-1986">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="cd182-1987">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1987">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd182-1988">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cd182-1988">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd182-1989">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cd182-1989">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd182-1990">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cd182-1990">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd182-1991">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cd182-1991">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd182-1992">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cd182-1992">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="cd182-1993">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-1993">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="cd182-1994">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-1994">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-1995">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cd182-1995">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="cd182-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="cd182-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="cd182-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cd182-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="cd182-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cd182-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="cd182-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cd182-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="cd182-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="cd182-2001">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2001">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd182-2002">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2002">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="cd182-2003">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2003">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="cd182-2004">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="cd182-2004">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="cd182-2005">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2005">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="cd182-2006">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2006">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd182-2007">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cd182-2007">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="cd182-2008">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cd182-2008">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="cd182-2009">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="cd182-2009">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="cd182-2010">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="cd182-2010">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="cd182-2011">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2011">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="cd182-2012">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2012">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-2013">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2013">New-AzIpGroup</span></span>
        - <span data-ttu-id="cd182-2014">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2014">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="cd182-2015">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2015">Get-AzIpGroup</span></span>
        - <span data-ttu-id="cd182-2016">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2016">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-2017">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2017">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-2018">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="cd182-2018">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2019">Az.Sql</span></span>
* <span data-ttu-id="cd182-2020">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2020">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="cd182-2021">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2021">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="cd182-2022">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="cd182-2022">Removed deprecated aliases:</span></span>
* <span data-ttu-id="cd182-2023">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="cd182-2023">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="cd182-2024">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="cd182-2024">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="cd182-2025">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2025">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cd182-2026">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="cd182-2026">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="cd182-2027">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2027">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="cd182-2028">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="cd182-2028">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2029">Az.Storage</span></span>
* <span data-ttu-id="cd182-2030">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="cd182-2030">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="cd182-2031">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2031">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cd182-2032">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2032">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cd182-2033">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="cd182-2033">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="cd182-2034">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd182-2034">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="cd182-2035">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd182-2035">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="cd182-2036">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="cd182-2036">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="cd182-2037">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-2037">General</span></span>
* <span data-ttu-id="cd182-2038">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-2038">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-2039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2039">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2040">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="cd182-2040">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-2041">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-2041">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-2042">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2042">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="cd182-2043">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2043">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2044">Az.Automation</span></span>
* <span data-ttu-id="cd182-2045">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2045">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-2046">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-2046">Az.Batch</span></span>
* <span data-ttu-id="cd182-2047">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="cd182-2047">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2048">Az.Compute</span></span>
* <span data-ttu-id="cd182-2049">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2049">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd182-2050">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="cd182-2050">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="cd182-2051">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="cd182-2051">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="cd182-2052">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="cd182-2052">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2053">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2054">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="cd182-2054">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="cd182-2055">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="cd182-2055">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="cd182-2056">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="cd182-2056">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-2057">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-2057">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-2058">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-2058">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd182-2059">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd182-2059">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd182-2060">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-2060">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="cd182-2061">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="cd182-2061">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="cd182-2062">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-2062">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="cd182-2063">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="cd182-2063">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-2064">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2064">Az.IotHub</span></span>
* <span data-ttu-id="cd182-2065">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="cd182-2065">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="cd182-2066">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd182-2066">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2067">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2067">Az.Monitor</span></span>
* <span data-ttu-id="cd182-2068">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="cd182-2068">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="cd182-2069">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="cd182-2069">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="cd182-2070">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="cd182-2070">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="cd182-2071">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-2071">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2072">Az.Network</span></span>
* <span data-ttu-id="cd182-2073">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="cd182-2073">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="cd182-2074">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2074">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="cd182-2075">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2075">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-2076">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2076">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="cd182-2077">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2077">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cd182-2078">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2078">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="cd182-2079">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2079">Updated cmdlets:</span></span>
        - <span data-ttu-id="cd182-2080">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2080">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd182-2081">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2081">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd182-2082">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2082">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cd182-2083">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="cd182-2083">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="cd182-2084">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="cd182-2084">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="cd182-2085">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="cd182-2085">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="cd182-2086">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="cd182-2086">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd182-2087">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd182-2087">Az.RedisCache</span></span>
* <span data-ttu-id="cd182-2088">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="cd182-2088">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2089">Az.Sql</span></span>
* <span data-ttu-id="cd182-2090">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2090">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2091">Az.Storage</span></span>
* <span data-ttu-id="cd182-2092">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="cd182-2092">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="cd182-2093">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="cd182-2093">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cd182-2094">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cd182-2094">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="cd182-2095">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="cd182-2095">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cd182-2096">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2096">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-2097">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-2097">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-2098">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="cd182-2098">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2099">Az.Websites</span></span>
* <span data-ttu-id="cd182-2100">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="cd182-2100">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="cd182-2101">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cd182-2102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-2102">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-2103">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="cd182-2104">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="cd182-2104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="cd182-2105">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2106">Az.Automation</span></span>
* <span data-ttu-id="cd182-2107">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="cd182-2107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="cd182-2108">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="cd182-2108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="cd182-2109">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cd182-2109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2110">Az.Compute</span></span>
* <span data-ttu-id="cd182-2111">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="cd182-2112">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd182-2113">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="cd182-2113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="cd182-2114">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="cd182-2114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="cd182-2115">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="cd182-2115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="cd182-2116">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="cd182-2116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="cd182-2117">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cd182-2117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="cd182-2118">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="cd182-2118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="cd182-2119">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2120">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2121">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="cd182-2121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="cd182-2122">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="cd182-2122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-2123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-2123">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-2124">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="cd182-2124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-2125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2125">Az.IotHub</span></span>
* <span data-ttu-id="cd182-2126">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="cd182-2127">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="cd182-2128">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cd182-2128">New cmdlets are:</span></span>
    - <span data-ttu-id="cd182-2129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd182-2129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd182-2130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd182-2130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd182-2131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd182-2131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd182-2132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd182-2132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2133">Az.Monitor</span></span>
* <span data-ttu-id="cd182-2134">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="cd182-2134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="cd182-2135">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="cd182-2135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="cd182-2136">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="cd182-2136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="cd182-2137">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="cd182-2137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="cd182-2138">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="cd182-2138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="cd182-2139">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="cd182-2139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="cd182-2140">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="cd182-2140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="cd182-2141">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-2141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="cd182-2142">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-2142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cd182-2143">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="cd182-2143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="cd182-2144">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-2144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cd182-2145">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="cd182-2145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="cd182-2146">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="cd182-2146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="cd182-2147">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="cd182-2147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="cd182-2148">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="cd182-2148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="cd182-2149">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="cd182-2149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="cd182-2150">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="cd182-2150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="cd182-2151">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="cd182-2152">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="cd182-2153">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="cd182-2153">Overall improved help files</span></span>
* <span data-ttu-id="cd182-2154">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-2154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2155">Az.Network</span></span>
* <span data-ttu-id="cd182-2156">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="cd182-2157">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-2157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="cd182-2158">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="cd182-2158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="cd182-2159">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="cd182-2159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="cd182-2160">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="cd182-2160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="cd182-2161">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="cd182-2161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="cd182-2162">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="cd182-2162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="cd182-2163">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="cd182-2163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="cd182-2164">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="cd182-2164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="cd182-2165">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="cd182-2165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="cd182-2166">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="cd182-2166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="cd182-2167">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="cd182-2167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="cd182-2168">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2168">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cd182-2169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="cd182-2170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="cd182-2171">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2171">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd182-2172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cd182-2172">New-VpnSite</span></span>
        - <span data-ttu-id="cd182-2173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cd182-2173">Update-VpnSite</span></span>
        - <span data-ttu-id="cd182-2174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2174">New-VpnConnection</span></span>
        - <span data-ttu-id="cd182-2175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2175">Update-VpnConnection</span></span>
* <span data-ttu-id="cd182-2176">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2178">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="cd182-2178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="cd182-2179">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="cd182-2179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2180">Az.Resources</span></span>
* <span data-ttu-id="cd182-2181">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-2182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2182">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-2183">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="cd182-2184">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="cd182-2184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="cd182-2185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd182-2185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd182-2186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd182-2186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd182-2187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd182-2187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd182-2188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cd182-2188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="cd182-2189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd182-2189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd182-2190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd182-2190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd182-2191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd182-2191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd182-2192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd182-2192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd182-2193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cd182-2193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="cd182-2194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd182-2194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd182-2195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd182-2195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd182-2196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd182-2196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd182-2197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="cd182-2197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="cd182-2198">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="cd182-2198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd182-2199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd182-2199">Az.SignalR</span></span>
* <span data-ttu-id="cd182-2200">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2201">Az.Sql</span></span>
* <span data-ttu-id="cd182-2202">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="cd182-2203">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="cd182-2204">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="cd182-2204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cd182-2205">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-2205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="cd182-2206">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2207">Az.Storage</span></span>
* <span data-ttu-id="cd182-2208">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cd182-2209">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="cd182-2209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="cd182-2210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="cd182-2211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="cd182-2212">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="cd182-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="cd182-2214">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="cd182-2214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="cd182-2215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-2215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd182-2216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-2216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd182-2217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-2217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd182-2218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd182-2218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2219">Az.Websites</span></span>
* <span data-ttu-id="cd182-2220">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="cd182-2221">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="cd182-2221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="cd182-2222">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="cd182-2223">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="cd182-2224">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-2224">General</span></span>
* <span data-ttu-id="cd182-2225">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-2226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2226">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2227">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="cd182-2227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-2228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-2228">Az.Aks</span></span>
* <span data-ttu-id="cd182-2229">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="cd182-2230">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="cd182-2230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-2231">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-2232">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="cd182-2233">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="cd182-2233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="cd182-2234">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="cd182-2235">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="cd182-2235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="cd182-2236">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="cd182-2236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-2237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-2237">Az.Batch</span></span>
* <span data-ttu-id="cd182-2238">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="cd182-2238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-2239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-2239">Az.Cdn</span></span>
* <span data-ttu-id="cd182-2240">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2241">Az.Compute</span></span>
* <span data-ttu-id="cd182-2242">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="cd182-2243">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="cd182-2243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="cd182-2244">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="cd182-2244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="cd182-2245">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="cd182-2245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="cd182-2246">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="cd182-2246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="cd182-2247">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="cd182-2247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="cd182-2248">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-2248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="cd182-2249">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2250">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2251">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="cd182-2251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="cd182-2252">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="cd182-2252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="cd182-2253">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="cd182-2253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="cd182-2254">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="cd182-2254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-2255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-2255">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-2256">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cd182-2256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2257">Az.EventHub</span></span>
* <span data-ttu-id="cd182-2258">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="cd182-2259">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="cd182-2259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="cd182-2260">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="cd182-2261">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="cd182-2261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="cd182-2262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cd182-2262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cd182-2263">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2264">Az.Monitor</span></span>
* <span data-ttu-id="cd182-2265">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-2265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2266">Az.Network</span></span>
* <span data-ttu-id="cd182-2267">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="cd182-2268">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="cd182-2269">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="cd182-2269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="cd182-2270">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="cd182-2271">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="cd182-2271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="cd182-2272">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="cd182-2272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="cd182-2273">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-2274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2274">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-2275">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="cd182-2275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="cd182-2276">新增了範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2276">Added example</span></span>
    - <span data-ttu-id="cd182-2277">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-2277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="cd182-2278">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="cd182-2279">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2280">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2281">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2282">Az.Resources</span></span>
* <span data-ttu-id="cd182-2283">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="cd182-2284">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="cd182-2285">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="cd182-2285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="cd182-2286">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-2287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-2287">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-2288">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="cd182-2289">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="cd182-2289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="cd182-2290">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-2290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-2291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2291">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-2292">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="cd182-2292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="cd182-2293">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="cd182-2294">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="cd182-2294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="cd182-2295">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="cd182-2296">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="cd182-2296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="cd182-2297">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2298">Az.Sql</span></span>
* <span data-ttu-id="cd182-2299">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="cd182-2299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2300">Az.Storage</span></span>
* <span data-ttu-id="cd182-2301">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="cd182-2302">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="cd182-2302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="cd182-2303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="cd182-2304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd182-2304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="cd182-2305">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="cd182-2305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="cd182-2306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd182-2306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2307">Az.Websites</span></span>
* <span data-ttu-id="cd182-2308">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="cd182-2308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="cd182-2309">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-2310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2310">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2311">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cd182-2311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cd182-2312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cd182-2313">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2314">Az.Automation</span></span>
* <span data-ttu-id="cd182-2315">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2315">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-2316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2316">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-2317">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2318">Az.Compute</span></span>
* <span data-ttu-id="cd182-2319">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd182-2320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd182-2320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd182-2321">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="cd182-2322">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="cd182-2322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2323">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2324">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="cd182-2324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="cd182-2325">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-2326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2326">Az.EventHub</span></span>
* <span data-ttu-id="cd182-2327">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cd182-2327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cd182-2328">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-2328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-2329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-2329">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-2330">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd182-2331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd182-2331">Az.LogicApp</span></span>
* <span data-ttu-id="cd182-2332">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="cd182-2332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="cd182-2333">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd182-2334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2334">Az.ManagedServices</span></span>
* <span data-ttu-id="cd182-2335">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2336">Az.Network</span></span>
* <span data-ttu-id="cd182-2337">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="cd182-2338">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2338">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd182-2339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd182-2340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd182-2341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-2342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-2343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-2344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd182-2345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="cd182-2345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="cd182-2346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="cd182-2347">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="cd182-2347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="cd182-2348">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="cd182-2349">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="cd182-2349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="cd182-2350">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="cd182-2350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="cd182-2351">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="cd182-2351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="cd182-2352">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="cd182-2352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="cd182-2353">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2353">Updated cmdlets</span></span>
        - <span data-ttu-id="cd182-2354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd182-2355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd182-2356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cd182-2357">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cd182-2358">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cd182-2358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="cd182-2359">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2359">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd182-2360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cd182-2361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cd182-2362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="cd182-2363">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="cd182-2363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="cd182-2364">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="cd182-2364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="cd182-2365">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="cd182-2365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-2366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2366">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-2367">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="cd182-2367">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="cd182-2368">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="cd182-2368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2370">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cd182-2371">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="cd182-2372">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="cd182-2373">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cd182-2374">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="cd182-2375">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cd182-2376">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="cd182-2377">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cd182-2378">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="cd182-2378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="cd182-2379">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="cd182-2379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2380">Az.Resources</span></span>
- <span data-ttu-id="cd182-2381">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="cd182-2382">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cd182-2382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-2383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-2383">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-2384">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cd182-2384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cd182-2385">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-2385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2386">Az.Sql</span></span>
* <span data-ttu-id="cd182-2387">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="cd182-2388">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="cd182-2389">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="cd182-2389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2390">Az.Storage</span></span>
* <span data-ttu-id="cd182-2391">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-2391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-2392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-2392">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-2393">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="cd182-2394">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="cd182-2394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2395">Az.Websites</span></span>
* <span data-ttu-id="cd182-2396">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-2396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="cd182-2397">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="cd182-2398">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-2398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="cd182-2399">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-2400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2400">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2401">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cd182-2402">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cd182-2403">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cd182-2404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cd182-2404">Az.Advisor</span></span>
* <span data-ttu-id="cd182-2405">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="cd182-2405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cd182-2406">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="cd182-2406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd182-2407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-2407">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-2408">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cd182-2409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cd182-2409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cd182-2410">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cd182-2411">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cd182-2412">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cd182-2413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cd182-2413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cd182-2414">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2415">Az.Automation</span></span>
* <span data-ttu-id="cd182-2416">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="cd182-2416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2417">Az.Compute</span></span>
* <span data-ttu-id="cd182-2418">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2419">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2420">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="cd182-2420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd182-2421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd182-2421">Az.EventGrid</span></span>
* <span data-ttu-id="cd182-2422">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-2423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2423">Az.IotHub</span></span>
* <span data-ttu-id="cd182-2424">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2425">Az.Network</span></span>
* <span data-ttu-id="cd182-2426">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="cd182-2426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cd182-2427">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-2428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2428">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-2429">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cd182-2430">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="cd182-2430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-2431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2431">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-2432">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="cd182-2432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2433">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2434">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="cd182-2434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2435">Az.Resources</span></span>
    - <span data-ttu-id="cd182-2436">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="cd182-2436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cd182-2437">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cd182-2438">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cd182-2439">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="cd182-2439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-2440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-2440">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-2441">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="cd182-2441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2442">Az.Sql</span></span>
* <span data-ttu-id="cd182-2443">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="cd182-2443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cd182-2444">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="cd182-2444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cd182-2445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd182-2446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd182-2447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd182-2448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cd182-2449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cd182-2450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd182-2450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cd182-2451">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="cd182-2451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2452">Az.Storage</span></span>
* <span data-ttu-id="cd182-2453">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="cd182-2453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cd182-2454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd182-2454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cd182-2455">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-2455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cd182-2456">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-2456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cd182-2457">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cd182-2457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cd182-2458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cd182-2459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cd182-2460">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="cd182-2460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cd182-2461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd182-2461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cd182-2462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd182-2462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd182-2463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd182-2463">Az.StorageSync</span></span>
* <span data-ttu-id="cd182-2464">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="cd182-2464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cd182-2465">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-2466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2466">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2467">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-2467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cd182-2468">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="cd182-2468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cd182-2469">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cd182-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cd182-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cd182-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cd182-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2472">Az.Compute</span></span>
* <span data-ttu-id="cd182-2473">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cd182-2474">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cd182-2475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cd182-2475">Az.Dns</span></span>
* <span data-ttu-id="cd182-2476">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="cd182-2476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd182-2477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd182-2477">Az.EventGrid</span></span>
* <span data-ttu-id="cd182-2478">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cd182-2478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cd182-2479">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2479">New cmdlets:</span></span>
    - <span data-ttu-id="cd182-2480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd182-2480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd182-2481">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="cd182-2481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd182-2482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd182-2482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd182-2483">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="cd182-2483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cd182-2484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd182-2484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd182-2485">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="cd182-2485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd182-2486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cd182-2486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cd182-2487">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd182-2487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd182-2488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cd182-2488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cd182-2489">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd182-2489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cd182-2490">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="cd182-2490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cd182-2491">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cd182-2492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cd182-2492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cd182-2493">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="cd182-2493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="cd182-2494">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="cd182-2494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cd182-2495">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cd182-2496">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2496">Updated cmdlets:</span></span>
    - <span data-ttu-id="cd182-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="cd182-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cd182-2498">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd182-2498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cd182-2499">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd182-2499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cd182-2500">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cd182-2501">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cd182-2501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cd182-2502">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="cd182-2502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cd182-2503">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cd182-2504">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="cd182-2504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cd182-2505">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="cd182-2505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="cd182-2506">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="cd182-2506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cd182-2507">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="cd182-2507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cd182-2508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cd182-2508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cd182-2509">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd182-2509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cd182-2510">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd182-2510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-2511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-2511">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-2512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cd182-2512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cd182-2513">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="cd182-2513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cd182-2514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd182-2514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cd182-2515">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="cd182-2515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2516">Az.Network</span></span>
* <span data-ttu-id="cd182-2517">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cd182-2518">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2518">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cd182-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cd182-2520">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cd182-2520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cd182-2521">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2521">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cd182-2522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cd182-2523">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cd182-2524">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2524">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2525">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd182-2526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd182-2527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd182-2527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd182-2528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cd182-2529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cd182-2530">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd182-2530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cd182-2531">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2531">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd182-2532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd182-2533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd182-2533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd182-2534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd182-2534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd182-2535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cd182-2535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cd182-2536">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="cd182-2536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cd182-2537">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="cd182-2537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cd182-2538">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="cd182-2538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cd182-2539">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="cd182-2539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cd182-2540">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="cd182-2540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cd182-2541">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="cd182-2541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cd182-2542">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-2542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cd182-2543">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="cd182-2543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cd182-2544">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cd182-2545">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="cd182-2545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cd182-2546">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="cd182-2546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cd182-2547">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cd182-2548">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="cd182-2548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cd182-2549">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cd182-2550">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cd182-2551">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="cd182-2551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cd182-2552">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="cd182-2552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cd182-2553">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="cd182-2553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cd182-2554">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="cd182-2554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="cd182-2555">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="cd182-2555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="cd182-2556">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cd182-2556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cd182-2557">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cd182-2557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cd182-2558">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cd182-2558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-2559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2559">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-2560">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="cd182-2560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2561">Az.Resources</span></span>
* <span data-ttu-id="cd182-2562">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="cd182-2562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cd182-2563">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cd182-2564">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cd182-2565">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="cd182-2565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-2566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2566">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-2567">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2568">Az.Sql</span></span>
* <span data-ttu-id="cd182-2569">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="cd182-2569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cd182-2570">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="cd182-2570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cd182-2571">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="cd182-2571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cd182-2572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd182-2572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd182-2573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd182-2573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd182-2574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd182-2574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd182-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cd182-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cd182-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cd182-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2577">Az.Storage</span></span>
* <span data-ttu-id="cd182-2578">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="cd182-2578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cd182-2579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2579">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd182-2580">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-2580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cd182-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2582">Az.Websites</span></span>
* <span data-ttu-id="cd182-2583">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="cd182-2583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cd182-2584">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="cd182-2584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cd182-2585">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cd182-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-2586">Az.Cdn</span></span>
* <span data-ttu-id="cd182-2587">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-2587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2588">Az.Compute</span></span>
* <span data-ttu-id="cd182-2589">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="cd182-2589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cd182-2590">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cd182-2590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-2591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2591">Az.EventHub</span></span>
* <span data-ttu-id="cd182-2592">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="cd182-2592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cd182-2593">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd182-2593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2594">Az.Network</span></span>
* <span data-ttu-id="cd182-2595">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="cd182-2595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cd182-2596">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="cd182-2596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-2597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2597">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-2598">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2599">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2600">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="cd182-2600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-2601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-2601">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-2602">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd182-2602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-2603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2603">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-2604">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cd182-2605">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2606">Az.Sql</span></span>
* <span data-ttu-id="cd182-2607">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="cd182-2607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cd182-2608">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cd182-2609">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="cd182-2609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cd182-2610">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2611">Az.Websites</span></span>
* <span data-ttu-id="cd182-2612">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cd182-2613">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cd182-2614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-2614">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-2615">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="cd182-2615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cd182-2616">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="cd182-2616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cd182-2617">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="cd182-2617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cd182-2618">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="cd182-2618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cd182-2619">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="cd182-2619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cd182-2620">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="cd182-2620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cd182-2621">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="cd182-2621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cd182-2622">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="cd182-2622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cd182-2623">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="cd182-2623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cd182-2624">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="cd182-2624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cd182-2625">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="cd182-2625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cd182-2626">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="cd182-2626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cd182-2627">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="cd182-2627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cd182-2628">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cd182-2629">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cd182-2630">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cd182-2631">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cd182-2632">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cd182-2632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cd182-2633">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="cd182-2633">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="cd182-2634">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="cd182-2634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cd182-2635">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="cd182-2635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cd182-2636">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="cd182-2636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cd182-2637">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="cd182-2637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cd182-2638">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="cd182-2638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="cd182-2639">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cd182-2640">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cd182-2641">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="cd182-2641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cd182-2642">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="cd182-2642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cd182-2643">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cd182-2644">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="cd182-2644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cd182-2645">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-2645">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="cd182-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cd182-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cd182-2647">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="cd182-2647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cd182-2648">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cd182-2648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd182-2649">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="cd182-2649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cd182-2650">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-2650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cd182-2651">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-2651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cd182-2652">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="cd182-2652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cd182-2653">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="cd182-2653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cd182-2654">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cd182-2654">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd182-2655">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="cd182-2655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cd182-2656">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="cd182-2656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cd182-2657">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="cd182-2657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cd182-2658">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cd182-2659">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cd182-2659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd182-2660">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="cd182-2660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cd182-2661">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="cd182-2661">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cd182-2662">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cd182-2663">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="cd182-2663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cd182-2664">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="cd182-2664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cd182-2665">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cd182-2666">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="cd182-2666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cd182-2667">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cd182-2668">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="cd182-2668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cd182-2669">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="cd182-2669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cd182-2670">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="cd182-2670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cd182-2671">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cd182-2671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cd182-2672">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="cd182-2672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cd182-2673">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="cd182-2673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cd182-2674">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cd182-2675">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cd182-2675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cd182-2676">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="cd182-2676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cd182-2677">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="cd182-2677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cd182-2678">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-2678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cd182-2679">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="cd182-2679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cd182-2680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="cd182-2680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cd182-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cd182-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cd182-2682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="cd182-2682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cd182-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cd182-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cd182-2684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cd182-2684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cd182-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cd182-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cd182-2686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="cd182-2686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cd182-2687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="cd182-2687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cd182-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cd182-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cd182-2689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-2689">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="cd182-2690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cd182-2690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cd182-2691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="cd182-2691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2692">Az.Automation</span></span>
* <span data-ttu-id="cd182-2693">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="cd182-2693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cd182-2694">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cd182-2695">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cd182-2696">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="cd182-2696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cd182-2697">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cd182-2698">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cd182-2699">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="cd182-2699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2700">Az.Compute</span></span>
* <span data-ttu-id="cd182-2701">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cd182-2702">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="cd182-2702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-2703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-2703">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-2704">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="cd182-2704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2705">Az.Monitor</span></span>
* <span data-ttu-id="cd182-2706">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-2706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2707">Az.Network</span></span>
* <span data-ttu-id="cd182-2708">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="cd182-2708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cd182-2709">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2709">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd182-2710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-2710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cd182-2711">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="cd182-2711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2712">Az.Resources</span></span>
* <span data-ttu-id="cd182-2713">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="cd182-2713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2714">Az.Sql</span></span>
* <span data-ttu-id="cd182-2715">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="cd182-2715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cd182-2716">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-2717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2717">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2718">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-2719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2719">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-2720">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="cd182-2720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cd182-2721">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-2721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2722">Az.Compute</span></span>
* <span data-ttu-id="cd182-2723">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-2723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cd182-2724">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cd182-2725">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cd182-2726">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="cd182-2726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cd182-2727">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="cd182-2727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cd182-2728">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd182-2728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="cd182-2729">重大變更</span><span class="sxs-lookup"><span data-stu-id="cd182-2729">Breaking changes</span></span>
    - <span data-ttu-id="cd182-2730">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="cd182-2730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cd182-2731">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="cd182-2731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cd182-2732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cd182-2732">Az.DeploymentManager</span></span>
* <span data-ttu-id="cd182-2733">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cd182-2734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cd182-2734">Az.Dns</span></span>
* <span data-ttu-id="cd182-2735">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="cd182-2735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cd182-2736">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cd182-2737">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="cd182-2737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd182-2738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-2738">Az.FrontDoor</span></span>
* <span data-ttu-id="cd182-2739">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cd182-2740">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="cd182-2740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cd182-2741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-2741">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-2742">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-2742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cd182-2743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd182-2743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cd182-2744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd182-2744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cd182-2745">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd182-2745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cd182-2746">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="cd182-2746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cd182-2747">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd182-2747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cd182-2748">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="cd182-2748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2749">Az.Monitor</span></span>
* <span data-ttu-id="cd182-2750">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="cd182-2750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="cd182-2751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cd182-2751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cd182-2752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd182-2752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cd182-2753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cd182-2753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cd182-2754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cd182-2754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cd182-2755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cd182-2755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cd182-2756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cd182-2756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cd182-2757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd182-2758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd182-2759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd182-2760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd182-2761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd182-2762">[更多](/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-2762">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cd182-2763">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2764">Az.Network</span></span>
* <span data-ttu-id="cd182-2765">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cd182-2766">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2766">New cmdlets</span></span>
        - <span data-ttu-id="cd182-2767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd182-2767">New-AzNatGateway</span></span>
        - <span data-ttu-id="cd182-2768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd182-2768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cd182-2769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd182-2769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cd182-2770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd182-2770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cd182-2771">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2771">Updated cmdlets</span></span>
        - <span data-ttu-id="cd182-2772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cd182-2772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cd182-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cd182-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cd182-2774">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cd182-2774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cd182-2775">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cd182-2775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cd182-2776">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cd182-2776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-2777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2777">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-2778">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cd182-2778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cd182-2779">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="cd182-2779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cd182-2780">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="cd182-2780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2781">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2782">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="cd182-2782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cd182-2783">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="cd182-2783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cd182-2784">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="cd182-2784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cd182-2785">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="cd182-2785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cd182-2786">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="cd182-2786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cd182-2787">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="cd182-2787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cd182-2788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cd182-2788">Az.Relay</span></span>
* <span data-ttu-id="cd182-2789">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-2789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-2790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-2790">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-2791">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2792">Az.Storage</span></span>
* <span data-ttu-id="cd182-2793">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="cd182-2793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cd182-2794">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="cd182-2794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cd182-2795">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="cd182-2795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cd182-2796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2796">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd182-2797">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="cd182-2797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cd182-2798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cd182-2799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cd182-2800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-2800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2801">Az.Websites</span></span>
* <span data-ttu-id="cd182-2802">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-2802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cd182-2803">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="cd182-2803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cd182-2804">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-2805">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-2805">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-2806">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-2806">General availability of `Az` module</span></span>
* <span data-ttu-id="cd182-2807">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd182-2807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd182-2808">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd182-2808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd182-2809">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd182-2810">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-2810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd182-2811">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd182-2812">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-2813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2813">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2814">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="cd182-2814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd182-2815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-2815">Az.Batch</span></span>
* <span data-ttu-id="cd182-2816">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-2817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-2817">Az.Cdn</span></span>
* <span data-ttu-id="cd182-2818">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-2819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2819">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-2820">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2821">Az.Compute</span></span>
* <span data-ttu-id="cd182-2822">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cd182-2823">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2824">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2825">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2826">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="cd182-2826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-2827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-2827">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-2828">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd182-2829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd182-2829">Az.EventGrid</span></span>
* <span data-ttu-id="cd182-2830">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-2831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2831">Az.EventHub</span></span>
* <span data-ttu-id="cd182-2832">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2832">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd182-2833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd182-2833">Az.HDInsight</span></span>
* <span data-ttu-id="cd182-2834">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-2835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-2835">Az.IotHub</span></span>
* <span data-ttu-id="cd182-2836">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-2837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-2837">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-2838">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2839">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cd182-2840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd182-2840">Az.MachineLearning</span></span>
* <span data-ttu-id="cd182-2841">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cd182-2842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd182-2842">Az.Media</span></span>
* <span data-ttu-id="cd182-2843">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-2844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-2844">Az.Monitor</span></span>
  * <span data-ttu-id="cd182-2845">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cd182-2846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cd182-2846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cd182-2847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cd182-2847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cd182-2848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd182-2848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd182-2849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd182-2849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd182-2850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd182-2850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cd182-2851">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="cd182-2851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2852">Az.Network</span></span>
* <span data-ttu-id="cd182-2853">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2854">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cd182-2855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cd182-2855">Az.NotificationHubs</span></span>
* <span data-ttu-id="cd182-2856">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-2857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-2857">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-2858">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cd182-2859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cd182-2859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cd182-2860">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2861">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2862">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2863">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="cd182-2863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cd182-2864">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="cd182-2864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cd182-2865">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="cd182-2865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd182-2866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd182-2866">Az.RedisCache</span></span>
* <span data-ttu-id="cd182-2867">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2868">Az.Resources</span></span>
* <span data-ttu-id="cd182-2869">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2870">Az.Sql</span></span>
* <span data-ttu-id="cd182-2871">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-2871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cd182-2872">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2873">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="cd182-2873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cd182-2874">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="cd182-2874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cd182-2875">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="cd182-2875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cd182-2876">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-2876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cd182-2877">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cd182-2877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2878">Az.Websites</span></span>
* <span data-ttu-id="cd182-2879">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="cd182-2879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cd182-2880">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-2880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd182-2881">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="cd182-2881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cd182-2882">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd182-2882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cd182-2883">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-2884">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-2884">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-2885">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-2885">General availability of `Az` module</span></span>
* <span data-ttu-id="cd182-2886">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd182-2886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd182-2887">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd182-2887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd182-2888">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd182-2889">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-2889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd182-2890">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd182-2891">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd182-2892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2892">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2893">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-2894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2894">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd182-2895">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="cd182-2895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cd182-2896">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="cd182-2896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2897">Az.Automation</span></span>
* <span data-ttu-id="cd182-2898">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cd182-2898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cd182-2899">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="cd182-2899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cd182-2900">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cd182-2900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2901">Az.Compute</span></span>
* <span data-ttu-id="cd182-2902">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-2902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd182-2903">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="cd182-2903">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cd182-2904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-2904">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd182-2905">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="cd182-2905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2906">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2907">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="cd182-2907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cd182-2908">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-2908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2909">Az.Resources</span></span>
* <span data-ttu-id="cd182-2910">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="cd182-2910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cd182-2911">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="cd182-2911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cd182-2912">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="cd182-2912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cd182-2913">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd182-2913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cd182-2914">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="cd182-2914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cd182-2915">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd182-2915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2916">Az.Sql</span></span>
* <span data-ttu-id="cd182-2917">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="cd182-2917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2918">Az.Storage</span></span>
* <span data-ttu-id="cd182-2919">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="cd182-2919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cd182-2920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd182-2920">New-AzStorageContext</span></span>
* <span data-ttu-id="cd182-2921">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-2921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cd182-2922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd182-2922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd182-2923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd182-2923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd182-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cd182-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cd182-2926">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cd182-2927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd182-2928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd182-2929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cd182-2930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd182-2930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cd182-2931">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd182-2932">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cd182-2932">Highlights since the last major release</span></span>
* <span data-ttu-id="cd182-2933">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cd182-2933">General availability of `Az` module</span></span>
* <span data-ttu-id="cd182-2934">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd182-2934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd182-2935">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd182-2935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd182-2936">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd182-2937">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-2937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd182-2938">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd182-2939">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2940">Az.Automation</span></span>
* <span data-ttu-id="cd182-2941">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="cd182-2941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cd182-2942">動態分組</span><span class="sxs-lookup"><span data-stu-id="cd182-2942">Dynamic grouping</span></span>
    * <span data-ttu-id="cd182-2943">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="cd182-2943">Pre-Post script</span></span>
    * <span data-ttu-id="cd182-2944">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="cd182-2944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2945">Az.Compute</span></span>
* <span data-ttu-id="cd182-2946">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cd182-2947">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="cd182-2947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-2948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-2948">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-2949">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2950">Az.Network</span></span>
* <span data-ttu-id="cd182-2951">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cd182-2952">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="cd182-2952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2953">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2954">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="cd182-2954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cd182-2955">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2956">Az.Resources</span></span>
* <span data-ttu-id="cd182-2957">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cd182-2958">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="cd182-2958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-2959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-2959">Az.Sql</span></span>
* <span data-ttu-id="cd182-2960">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-2960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-2961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-2961">Az.Storage</span></span>
* <span data-ttu-id="cd182-2962">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="cd182-2962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cd182-2963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd182-2964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd182-2965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-2965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd182-2966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cd182-2966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cd182-2967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cd182-2967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cd182-2968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cd182-2968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-2969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-2969">Az.Websites</span></span>
* <span data-ttu-id="cd182-2970">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="cd182-2970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="cd182-2971">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cd182-2971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-2972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-2972">Az.Accounts</span></span>
* <span data-ttu-id="cd182-2973">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cd182-2974">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="cd182-2974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-2975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-2975">Az.Automation</span></span>
* <span data-ttu-id="cd182-2976">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd182-2977">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-2977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cd182-2978">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="cd182-2978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-2979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-2979">Az.Cdn</span></span>
* <span data-ttu-id="cd182-2980">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-2981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-2981">Az.Compute</span></span>
* <span data-ttu-id="cd182-2982">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-2983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-2983">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-2984">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="cd182-2984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd182-2985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd182-2985">Az.LogicApp</span></span>
* <span data-ttu-id="cd182-2986">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="cd182-2986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-2987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-2987">Az.Network</span></span>
* <span data-ttu-id="cd182-2988">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-2989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-2989">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-2990">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-2990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cd182-2991">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="cd182-2991">SDK Update</span></span>
* <span data-ttu-id="cd182-2992">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="cd182-2992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cd182-2993">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="cd182-2993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-2994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-2994">Az.Resources</span></span>
* <span data-ttu-id="cd182-2995">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-2995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cd182-2996">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cd182-2996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cd182-2997">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cd182-2998">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cd182-2998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cd182-2999">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-2999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cd182-3000">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cd182-3000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3001">Az.Sql</span></span>
* <span data-ttu-id="cd182-3002">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="cd182-3002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cd182-3003">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="cd182-3003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-3004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3004">Az.Storage</span></span>
* <span data-ttu-id="cd182-3005">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd182-3005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cd182-3006">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-3007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3007">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd182-3008">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-3009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-3009">Az.Automation</span></span>
* <span data-ttu-id="cd182-3010">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-3010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cd182-3011">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cd182-3012">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="cd182-3012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-3013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3013">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-3014">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="cd182-3014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3015">Az.Compute</span></span>
* <span data-ttu-id="cd182-3016">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cd182-3017">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="cd182-3017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cd182-3018">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cd182-3019">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="cd182-3019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3020">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-3021">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd182-3022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd182-3022">Az.EventHub</span></span>
* <span data-ttu-id="cd182-3023">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="cd182-3023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-3024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-3024">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-3025">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="cd182-3025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd182-3026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd182-3026">Az.LogicApp</span></span>
* <span data-ttu-id="cd182-3027">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="cd182-3027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cd182-3028">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="cd182-3028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cd182-3029">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cd182-3030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd182-3030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd182-3031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd182-3031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd182-3032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd182-3032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd182-3033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd182-3033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cd182-3034">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cd182-3035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-3035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd182-3036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-3036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd182-3037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-3037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd182-3038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-3038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cd182-3039">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="cd182-3039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd182-3040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-3040">Az.Monitor</span></span>
* <span data-ttu-id="cd182-3041">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="cd182-3041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-3042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3042">Az.Network</span></span>
* <span data-ttu-id="cd182-3043">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-3044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-3044">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd182-3045">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-3045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cd182-3046">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="cd182-3046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="cd182-3047">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="cd182-3047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3048">Az.Resources</span></span>
* <span data-ttu-id="cd182-3049">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd182-3050">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cd182-3051">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cd182-3052">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-3052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3053">Az.Sql</span></span>
* <span data-ttu-id="cd182-3054">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cd182-3055">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="cd182-3055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-3056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3056">Az.Websites</span></span>
* <span data-ttu-id="cd182-3057">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cd182-3058">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-3059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3059">Az.Accounts</span></span>
* <span data-ttu-id="cd182-3060">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cd182-3060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-3061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3061">Az.AnalysisServices</span></span>
<span data-ttu-id="cd182-3062">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="cd182-3062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3063">Az.Compute</span></span>
* <span data-ttu-id="cd182-3064">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cd182-3065">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="cd182-3065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cd182-3066">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-3067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3067">Az.RecoveryServices</span></span>
<span data-ttu-id="cd182-3068">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="cd182-3068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3069">Az.Resources</span></span>
* <span data-ttu-id="cd182-3070">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="cd182-3070">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="cd182-3071">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cd182-3071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd182-3072">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="cd182-3073">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cd182-3073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3074">Az.Sql</span></span>
* <span data-ttu-id="cd182-3075">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd182-3075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cd182-3076">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cd182-3077">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="cd182-3077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cd182-3078">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-3079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3079">Az.Accounts</span></span>
* <span data-ttu-id="cd182-3080">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="cd182-3080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd182-3081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3081">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd182-3082">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="cd182-3082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-3083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3083">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd182-3084">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="cd182-3084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cd182-3085">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-3086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3086">Az.Accounts</span></span>
* <span data-ttu-id="cd182-3087">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cd182-3087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd182-3088">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd182-3089">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-3089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd182-3090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd182-3090">Az.Aks</span></span>
* <span data-ttu-id="cd182-3091">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd182-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-3092">Az.Automation</span></span>
* <span data-ttu-id="cd182-3093">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cd182-3094">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd182-3095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd182-3095">Az.Cdn</span></span>
* <span data-ttu-id="cd182-3096">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3097">Az.Compute</span></span>
* <span data-ttu-id="cd182-3098">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cd182-3099">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd182-3099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cd182-3100">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-3100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd182-3101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd182-3101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd182-3102">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd182-3103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd182-3103">Az.DataFactory</span></span>
* <span data-ttu-id="cd182-3104">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="cd182-3104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3105">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-3106">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cd182-3107">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cd182-3107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cd182-3108">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-3109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-3109">Az.IotHub</span></span>
* <span data-ttu-id="cd182-3110">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-3110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd182-3111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-3111">Az.KeyVault</span></span>
* <span data-ttu-id="cd182-3112">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-3113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3113">Az.Network</span></span>
* <span data-ttu-id="cd182-3114">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3115">Az.Resources</span></span>
* <span data-ttu-id="cd182-3116">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cd182-3117">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cd182-3118">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="cd182-3118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cd182-3119">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cd182-3120">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cd182-3121">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cd182-3122">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cd182-3122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-3123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-3123">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-3124">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cd182-3124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cd182-3125">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-3125">Fix some error messages.</span></span>
* <span data-ttu-id="cd182-3126">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cd182-3127">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd182-3128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd182-3128">Az.SignalR</span></span>
* <span data-ttu-id="cd182-3129">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3130">Az.Sql</span></span>
* <span data-ttu-id="cd182-3131">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd182-3132">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="cd182-3132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cd182-3133">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cd182-3134">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="cd182-3134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-3135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3135">Az.Storage</span></span>
* <span data-ttu-id="cd182-3136">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd182-3137">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="cd182-3137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cd182-3138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cd182-3138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cd182-3139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cd182-3139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cd182-3140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd182-3140">Az.TrafficManager</span></span>
* <span data-ttu-id="cd182-3141">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3142">Az.Websites</span></span>
* <span data-ttu-id="cd182-3143">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd182-3144">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="cd182-3144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cd182-3145">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="cd182-3145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cd182-3146">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd182-3147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3147">Az.Accounts</span></span>
* <span data-ttu-id="cd182-3148">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="cd182-3148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3149">Az.Compute</span></span>
* <span data-ttu-id="cd182-3150">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="cd182-3150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cd182-3151">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="cd182-3151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cd182-3152">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3153">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-3154">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cd182-3155">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="cd182-3155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd182-3156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd182-3156">Az.EventGrid</span></span>
* <span data-ttu-id="cd182-3157">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cd182-3157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cd182-3158">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="cd182-3158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cd182-3159">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cd182-3159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd182-3160">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="cd182-3160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd182-3161">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="cd182-3161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd182-3162">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="cd182-3162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cd182-3163">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cd182-3163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd182-3164">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="cd182-3164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd182-3165">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="cd182-3165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd182-3166">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="cd182-3166">Dead letter endpoint.</span></span>
* <span data-ttu-id="cd182-3167">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="cd182-3167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cd182-3168">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-3168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd182-3169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd182-3169">Az.IotHub</span></span>
* <span data-ttu-id="cd182-3170">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="cd182-3170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd182-3171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd182-3171">Az.LogicApp</span></span>
* <span data-ttu-id="cd182-3172">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-3172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3173">Az.Resources</span></span>
* <span data-ttu-id="cd182-3174">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cd182-3175">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cd182-3175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cd182-3176">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="cd182-3176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd182-3177">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-3177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cd182-3178">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="cd182-3178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cd182-3179">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cd182-3179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd182-3180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd182-3180">Az.SignalR</span></span>
* <span data-ttu-id="cd182-3181">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3182">Az.Sql</span></span>
* <span data-ttu-id="cd182-3183">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="cd182-3183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd182-3184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3184">Az.Storage</span></span>
* <span data-ttu-id="cd182-3185">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-3185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cd182-3186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd182-3186">New-AzStorageContext</span></span>
* <span data-ttu-id="cd182-3187">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="cd182-3187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cd182-3188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd182-3188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-3189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3189">Az.Websites</span></span>
* <span data-ttu-id="cd182-3190">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="cd182-3190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cd182-3191">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cd182-3192">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cd182-3193">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-3193">General</span></span>

- <span data-ttu-id="cd182-3194">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="cd182-3194">General Availability of Az Module</span></span>
- <span data-ttu-id="cd182-3195">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="cd182-3195">Online help for each module</span></span>
- <span data-ttu-id="cd182-3196">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cd182-3196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cd182-3197">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cd182-3198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3198">Az.Accounts</span></span>
- <span data-ttu-id="cd182-3199">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="cd182-3199">Changed from Az.Profile</span></span>
- <span data-ttu-id="cd182-3200">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="cd182-3200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd182-3201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-3201">Az.ApiManagement</span></span>
- <span data-ttu-id="cd182-3202">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="cd182-3202">Fixes for #7002</span></span>
- <span data-ttu-id="cd182-3203">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cd182-3204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd182-3204">Az.Batch</span></span>
- <span data-ttu-id="cd182-3205">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="cd182-3205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cd182-3206">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="cd182-3206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cd182-3207">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cd182-3208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd182-3208">Az.Billing</span></span>
- <span data-ttu-id="cd182-3209">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cd182-3210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3210">Az.CognitivServices</span></span>
- <span data-ttu-id="cd182-3211">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="cd182-3211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cd182-3212">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="cd182-3212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd182-3213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3213">Az.ContainerInstance</span></span>
- <span data-ttu-id="cd182-3214">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cd182-3215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cd182-3215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cd182-3216">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3217">Az.DataLakeStore</span></span>
- <span data-ttu-id="cd182-3218">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cd182-3219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd182-3219">Az.Monitor</span></span>
- <span data-ttu-id="cd182-3220">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cd182-3221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd182-3221">Az.KeyVault</span></span>
- <span data-ttu-id="cd182-3222">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="cd182-3222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cd182-3223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd182-3223">Az.MachineLearning</span></span>
- <span data-ttu-id="cd182-3224">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cd182-3225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd182-3225">Az.Media</span></span>
- <span data-ttu-id="cd182-3226">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="cd182-3226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd182-3227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3227">Az.Network</span></span>
<span data-ttu-id="cd182-3228">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cd182-3229">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd182-3229">New cmdlets added:</span></span>
        - <span data-ttu-id="cd182-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cd182-3235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cd182-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cd182-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd182-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cd182-3238">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd182-3238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cd182-3239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd182-3239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cd182-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd182-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd182-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd182-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd182-3242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-3242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cd182-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cd182-3244">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-3244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cd182-3245">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cd182-3246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd182-3246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd182-3247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd182-3247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd182-3248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd182-3248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cd182-3249">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cd182-3250">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cd182-3251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-3251">Az.OperationalInsights</span></span>
- <span data-ttu-id="cd182-3252">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cd182-3253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd182-3253">Az.Profile</span></span>
- <span data-ttu-id="cd182-3254">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd182-3254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-3255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3255">Az.RecoveryServices</span></span>
- <span data-ttu-id="cd182-3256">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cd182-3257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3257">Az.Resources</span></span>
- <span data-ttu-id="cd182-3258">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd182-3259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-3259">Az.ServiceFabric</span></span>
- <span data-ttu-id="cd182-3260">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="cd182-3260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cd182-3261">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cd182-3262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cd182-3262">Az.SIgnalR</span></span>
- <span data-ttu-id="cd182-3263">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="cd182-3263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cd182-3264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3264">Az.Sql</span></span>
- <span data-ttu-id="cd182-3265">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="cd182-3265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cd182-3266">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cd182-3267">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd182-3268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3268">Az.Storage</span></span>
- <span data-ttu-id="cd182-3269">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd182-3270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3270">Az.Websites</span></span>
- <span data-ttu-id="cd182-3271">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd182-3271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cd182-3272">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cd182-3273">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-3273">General</span></span>

* <span data-ttu-id="cd182-3274">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="cd182-3274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd182-3275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3275">Az.Compute</span></span>

* <span data-ttu-id="cd182-3276">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="cd182-3276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3277">Az.DataLakeStore</span></span>

* <span data-ttu-id="cd182-3278">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="cd182-3278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cd182-3279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd182-3279">Az.FrontDoor</span></span>

* <span data-ttu-id="cd182-3280">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="cd182-3280">Fixed some broken links</span></span>
    - <span data-ttu-id="cd182-3281">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="cd182-3281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cd182-3282">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="cd182-3282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd182-3283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3283">Az.RecoveryServices</span></span>

* <span data-ttu-id="cd182-3284">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-3284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cd182-3285">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="cd182-3285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd182-3286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3286">Az.Resources</span></span>

* <span data-ttu-id="cd182-3287">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cd182-3287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cd182-3288">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="cd182-3288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cd182-3289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3289">Az.Sql</span></span>

* <span data-ttu-id="cd182-3290">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="cd182-3290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cd182-3291">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cd182-3292">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="cd182-3292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd182-3293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3293">Az.Storage</span></span>

* <span data-ttu-id="cd182-3294">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="cd182-3294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cd182-3295">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="cd182-3295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cd182-3296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd182-3296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd182-3297">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="cd182-3297">Support Static Website configuration</span></span>
    - <span data-ttu-id="cd182-3298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd182-3298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cd182-3299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd182-3299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd182-3300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3300">Az.Websites</span></span>

* <span data-ttu-id="cd182-3301">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cd182-3301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="cd182-3302">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="cd182-3302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cd182-3303">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="cd182-3303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cd182-3304">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd182-3305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd182-3305">Az.ApiManagement</span></span>
* <span data-ttu-id="cd182-3306">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-3306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cd182-3307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd182-3307">Az.Automation</span></span>
* <span data-ttu-id="cd182-3308">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd182-3309">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cd182-3310">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cd182-3311">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cd182-3312">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="cd182-3312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd182-3313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3313">Az.Compute</span></span>
* <span data-ttu-id="cd182-3314">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cd182-3315">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-3315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd182-3316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3316">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd182-3317">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-3317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cd182-3318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cd182-3318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cd182-3319">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="cd182-3319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd182-3320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3320">Az.Network</span></span>
* <span data-ttu-id="cd182-3321">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="cd182-3321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cd182-3322">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="cd182-3322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cd182-3323">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="cd182-3323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="cd182-3324">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cd182-3325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd182-3325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cd182-3326">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="cd182-3326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cd182-3327">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="cd182-3327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cd182-3328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cd182-3328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cd182-3329">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cd182-3330">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cd182-3330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cd182-3331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cd182-3331">Az.Relay</span></span>
* <span data-ttu-id="cd182-3332">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="cd182-3332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd182-3333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3333">Az.Resources</span></span>
* <span data-ttu-id="cd182-3334">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="cd182-3334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cd182-3335">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="cd182-3335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cd182-3336">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="cd182-3336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd182-3337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-3337">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-3338">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="cd182-3338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cd182-3339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3339">Az.Sql</span></span>
* <span data-ttu-id="cd182-3340">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cd182-3341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd182-3342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd182-3343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd182-3344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd182-3344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd182-3345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd182-3345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd182-3346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd182-3346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd182-3347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd182-3347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd182-3348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd182-3348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cd182-3349">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="cd182-3349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cd182-3350">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="cd182-3350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cd182-3351">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="cd182-3351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cd182-3352">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="cd182-3352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd182-3353">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="cd182-3353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd182-3354">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="cd182-3354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cd182-3355">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="cd182-3355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cd182-3356">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cd182-3357">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cd182-3358">一般</span><span class="sxs-lookup"><span data-stu-id="cd182-3358">General</span></span>
* <span data-ttu-id="cd182-3359">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="cd182-3359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cd182-3360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd182-3360">Az.Profile</span></span>
* <span data-ttu-id="cd182-3361">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cd182-3361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cd182-3362">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="cd182-3362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cd182-3363">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="cd182-3363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cd182-3364">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cd182-3364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cd182-3365">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cd182-3366">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cd182-3367">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-3368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3368">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-3369">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="cd182-3369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3370">Az.Compute</span></span>
* <span data-ttu-id="cd182-3371">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cd182-3372">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cd182-3372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cd182-3373">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3374">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-3375">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="cd182-3375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cd182-3376">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="cd182-3376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cd182-3377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cd182-3377">Az.Insights</span></span>
* <span data-ttu-id="cd182-3378">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="cd182-3378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cd182-3379">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cd182-3380">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="cd182-3380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cd182-3381">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="cd182-3381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-3382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3382">Az.Network</span></span>
* <span data-ttu-id="cd182-3383">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="cd182-3383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cd182-3384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-3384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cd182-3385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cd182-3385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cd182-3386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd182-3386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cd182-3387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cd182-3387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cd182-3388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd182-3388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cd182-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd182-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd182-3390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd182-3390">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd182-3391">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3392">Az.Resources</span></span>
* <span data-ttu-id="cd182-3393">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cd182-3393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cd182-3394">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="cd182-3394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd182-3395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd182-3395">Az.ServiceBus</span></span>
* <span data-ttu-id="cd182-3396">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="cd182-3396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd182-3397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd182-3397">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd182-3398">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="cd182-3398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cd182-3399">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd182-3399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cd182-3400">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="cd182-3400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cd182-3401">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="cd182-3401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cd182-3402">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="cd182-3402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cd182-3403">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cd182-3404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd182-3404">Az.Profile</span></span>
* <span data-ttu-id="cd182-3405">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cd182-3406">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cd182-3406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3407">Az.Compute</span></span>
* <span data-ttu-id="cd182-3408">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="cd182-3408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cd182-3409">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-3409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd182-3410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd182-3410">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd182-3411">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="cd182-3411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cd182-3412">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cd182-3412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cd182-3413">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd182-3413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd182-3414">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cd182-3414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd182-3415">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cd182-3415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-3416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3416">Az.Network</span></span>
* <span data-ttu-id="cd182-3417">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="cd182-3417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cd182-3418">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd182-3418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3419">Az.Resources</span></span>
* <span data-ttu-id="cd182-3420">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="cd182-3420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cd182-3421">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="cd182-3421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cd182-3422">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cd182-3423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cd182-3423">Azure.Storage</span></span>
* <span data-ttu-id="cd182-3424">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cd182-3425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd182-3425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cd182-3426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd182-3426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd182-3427">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cd182-3427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cd182-3428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cd182-3428">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd182-3429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd182-3429">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd182-3430">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="cd182-3430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd182-3431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd182-3431">Az.Compute</span></span>
* <span data-ttu-id="cd182-3432">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="cd182-3432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cd182-3433">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="cd182-3433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cd182-3434">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cd182-3434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cd182-3435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cd182-3435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cd182-3436">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="cd182-3436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd182-3437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd182-3437">Az.Network</span></span>
* <span data-ttu-id="cd182-3438">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="cd182-3438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cd182-3439">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3439">new cmdlets added</span></span>
    - <span data-ttu-id="cd182-3440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd182-3440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd182-3441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd182-3441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd182-3442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd182-3442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd182-3443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd182-3443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd182-3444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-3444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cd182-3445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd182-3445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cd182-3446">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="cd182-3446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cd182-3447">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cd182-3448">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd182-3448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd182-3449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd182-3449">Az.RedisCache</span></span>
* <span data-ttu-id="cd182-3450">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="cd182-3450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cd182-3451">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="cd182-3451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd182-3452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd182-3452">Az.Resources</span></span>
* <span data-ttu-id="cd182-3453">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd182-3453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd182-3454">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="cd182-3454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd182-3455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd182-3455">Az.Sql</span></span>
* <span data-ttu-id="cd182-3456">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="cd182-3456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd182-3457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd182-3457">Az.Websites</span></span>
* <span data-ttu-id="cd182-3458">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="cd182-3458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cd182-3459">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="cd182-3459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cd182-3460">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="cd182-3460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cd182-3461">初始版本</span><span class="sxs-lookup"><span data-stu-id="cd182-3461">Initial Release</span></span>