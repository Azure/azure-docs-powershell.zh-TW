---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 25d4df411c6df652170880c123e2fbdf24546193
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856127"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e5c6c-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-103">Azure PowerShell release notes</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="e5c6c-104">5.2.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-104">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-105">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-106">如果無法從基礎程式庫取得，則會受控以剖析原始權杖中的 ExpiresOn 時間</span><span class="sxs-lookup"><span data-stu-id="e5c6c-106">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="e5c6c-107">已改善互動式驗證無法使用時的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-107">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-108">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-109">[重大變更] 根據預設，'New-AzApiManagementProduct' 沒有訂用帳戶限制。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-109">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-110">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-111">已編輯 Get-AzVm，以在檢查節流之前，先依據 '-Name' 進行篩選，因為資源太多。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-111">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="e5c6c-112">新的 Cmdlet 'Start-AzVmssRollingExtensionUpgrade'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-112">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e5c6c-113">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-113">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e5c6c-114">支援 'Get-AzContainerRegistryUsage' 的管線輸入參數 'Name' 與管線輸入中的值 [#13605]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-114">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="e5c6c-115">改善 'Connect-AzContainerRegistry' 的例外狀況</span><span class="sxs-lookup"><span data-stu-id="e5c6c-115">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-116">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-117">已將 ADF .Net SDK 版本更新為 4.13.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-117">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e5c6c-118">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e5c6c-118">Az.HealthcareApis</span></span>
* <span data-ttu-id="e5c6c-119">已新增客戶管理金鑰的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-119">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-120">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-121">已修正 SAS 權杖的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-121">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-122">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-123">在設定金鑰保存庫存取原則時，支援 'all' 做為選項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-123">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="e5c6c-124">支援 SecretManagement 模組的新版本 [#13366]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-124">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="e5c6c-125">支援 SecretManagementModule 中 'SecretValue' 的 ByteArray、String、PSCredential 和 Hashtable [#12190]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-125">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="e5c6c-126">[重大變更] 重新設計與受控 HSM 相關 Cmdlet 的 API 介面。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-126">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-127">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-128">已將 'New-AzAutoscaleProfile' 的參數 'Rule' 變更為接受空白清單。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-128">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="e5c6c-129">[#12903]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-129">[#12903]</span></span>
* <span data-ttu-id="e5c6c-130">已新增新的 Cmdlet，以支援建立更有彈性的診斷設定：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-130">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="e5c6c-131">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-131">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="e5c6c-132">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-132">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="e5c6c-133">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-133">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-135">將說明文字和參數集名稱變更為 'Restore-AzRecoveryServicesBackupItem' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-135">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-136">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-137">已將 '-Tag' 參數支援新增至 'Set-AzTemplateSpec' 和 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-137">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="e5c6c-138">已將標籤顯示支援新增至範本規格的預設格式器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-138">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-139">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-139">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-140">已將範例新增至具有 SettingsSectionDescription param 的 'Set-AzServiceFabricSetting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-140">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="e5c6c-141">已將應用程式相關的 Cmdlet 更新為呼叫支援僅適用於 ARM 部署的資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-141">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="e5c6c-142">標示為已淘汰的叢集憑證 Cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 和 'Remove-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-142">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-143">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-144">已將 SecondaryType 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-144">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="e5c6c-145">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-145">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="e5c6c-146">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-146">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="e5c6c-147">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-147">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="e5c6c-148">已將 HighAvailabilityReplicaCount 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-148">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="e5c6c-149">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-149">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="e5c6c-150">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-150">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="e5c6c-151">使 ReadReplicaCount 成為下列內容中的 HighAvailabilityReplicaCount 別名：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-151">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="e5c6c-152">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-152">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="e5c6c-153">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-153">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-154">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-155">支援上傳 Azure 檔案大小上限至 4 TiB</span><span class="sxs-lookup"><span data-stu-id="e5c6c-155">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="e5c6c-156">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-156">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="e5c6c-157">已將 Azure.Storage.Blobs 升級至 12.7.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-157">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="e5c6c-158">已將 Azure.Storage.Files.Shares 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-158">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="e5c6c-159">已將 Azure.Storage.Files.DataLake 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-159">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-160">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-160">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-161">已新增具有下載原則和本機快取模式的同步階層處理原則功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-161">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-162">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-162">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-163">防止重複存取限制規則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-163">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="e5c6c-164">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="e5c6c-164">Thanks to our community contributors</span></span>
* <span data-ttu-id="e5c6c-165">Andrew Dawson (@dawsonar802)，升級 Get-AzKeyVaultCertificate.md - 取得憑證並將其另存為 pfx 區段，以使用 PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-165">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="e5c6c-166">@iviark，醫療保健 APIs Powershell BYOK 更新 (#13518)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-166">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="e5c6c-167">John Duckmanton (@johnduckmanton)，修正 TagPatchOperation 的拼寫 (#13508)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-167">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="e5c6c-168">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-168">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="e5c6c-169">Get-AzLogicAppRunHistory Help Tidy (#13513)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-169">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="e5c6c-170">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-170">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="e5c6c-171">更新 Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-171">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="e5c6c-172">更新 New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-172">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="e5c6c-173">@SteppingRazor，New-AzApiManagementProduct：將 SubscriptionsLimit 參數的預設值變更為 None (#13457)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-173">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="e5c6c-174">Steve Burkett (@SteveBurkettNZ)，修正範例中 WorkspaceResourceId 參數的打字錯誤 (#13589)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-174">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="e5c6c-175">5.1.0 - 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-175">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-176">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-176">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-177">已修正使用 ''Connect-AzAccount -DeviceCode' 時，可能不會遵守 TenantId 的問題 [#13477]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-177">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="e5c6c-178">已新增 Cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-178">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="e5c6c-179">已修正無法存取使用者設定檔路徑時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-179">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="e5c6c-180">已修正 Connect-AzAccount 期間發生 Write-Object 錯誤的問題 [#13419]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-180">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="e5c6c-181">已將參數 'ContainerRegistryEndpointSuffix' 新增至：'Add-AzEnvironment'、'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-181">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="e5c6c-182">支援點擊 <kbd>CTRL</kbd>+<kbd>C</kbd> 來中斷登入</span><span class="sxs-lookup"><span data-stu-id="e5c6c-182">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="e5c6c-183">已修正導致 'Connect-AzAccount -KeyVaultAccessToken' 無法運作的問題 [#13127]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-183">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="e5c6c-184">已修正 'Invoke-AzRestMethod' 中 Null 參考和方法不區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-184">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-185">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-186">已修正使用者無法使用服務主體建立新 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-186">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="e5c6c-187">[#13012]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-187">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="e5c6c-188">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-188">Az.AppConfiguration</span></span>
* <span data-ttu-id="e5c6c-189">'Az.AppConfiguration' 模組的正式推出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-189">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-190">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-191">已改善 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 命令的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-191">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-192">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-192">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-193">已將 ADLS 資料平面 SDK 更新為 1.2.4-alpha。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-193">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="e5c6c-194">變更： https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="e5c6c-194">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="e5c6c-195">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="e5c6c-195">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="e5c6c-196">已新增 MSIX Package Cmdlet 和更新應用程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-196">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-197">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-198">已修正 EventHub 叢集沒有標記時的叢集命令</span><span class="sxs-lookup"><span data-stu-id="e5c6c-198">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="e5c6c-199">已更新 AzEventHubGeoDRConfiguration 的 PartnerNamespace 命令解說文字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-199">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-200">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-200">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-201">已將 'ResourceProviderConnection' 和 'PrivateLink' 參數新增至 'New-AzHDInsightCluster' Cmdlet 以支援轉送輸出和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-201">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="e5c6c-202">已將 'AmbariDatabase' 參數新增至 'New-AzHDInsightCluster' Cmdlet，以支援自訂 Ambari 資料庫功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-202">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="e5c6c-203">將接受值 'AmbariDatabase' 新增至 'Add-AzHDInsightMetastore' Cmdlet 的 'MetastoreType' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-203">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-204">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-205">允許在 IoT 中樞建立 Cmdlet 中使用標記。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-205">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-206">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-207">支援更新金鑰保存庫標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-207">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e5c6c-208">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e5c6c-208">Az.LogicApp</span></span>
* <span data-ttu-id="e5c6c-209">已修正 Get-AzLogicAppRunHistory 只會取得結果第一頁的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-209">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-210">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-210">Az.Network</span></span>
* <span data-ttu-id="e5c6c-211">已更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-211">Updated below cmdlet</span></span> 
    - <span data-ttu-id="e5c6c-212">'New-AzLoadBalancerFrontendIpConfigCommand'、'Set-AzLoadBalancerFrontendIpConfigCommand'、'Add-AzLoadBalancerFrontendIpConfigCommand'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-212">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="e5c6c-213">已新增 PublicIpAddressPrefix 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-213">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="e5c6c-214">已新增 PublicIpAddressPrefixId 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-214">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="e5c6c-215">已將新屬性新增至下列 Cmdlet，以允許進行全域負載平衡</span><span class="sxs-lookup"><span data-stu-id="e5c6c-215">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="e5c6c-216">'New-AzLoadBalancer'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-216">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="e5c6c-217">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-217">Added Sku Tier property</span></span>
    - <span data-ttu-id="e5c6c-218">'New-AzPuplicIpAddress'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-218">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="e5c6c-219">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-219">Added Sku Tier property</span></span>
    - <span data-ttu-id="e5c6c-220">'New-AzPublicIpPrefix'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-220">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="e5c6c-221">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-221">Added Sku Tier property</span></span>
    - <span data-ttu-id="e5c6c-222">'New-AzLoadBalancerBackendAddressConfig'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-222">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="e5c6c-223">已新增 LoadBalancerFrontendIPConfigurationId 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-223">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="e5c6c-224">已更新規劃來取代下列 Cmdlet 的警告   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-224">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="e5c6c-225">已新增規劃來取代下列 Cmdlet 的 'RouteTable' 引數警告   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-225">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="e5c6c-226">已將 '-MinScaleUnits' 和 '-MaxScaleUnits' 引數設為 'Set-AzExpressRouteGateway' 中的選擇性項目</span><span class="sxs-lookup"><span data-stu-id="e5c6c-226">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="e5c6c-227">已新增 Cmdlet 來支援應用程式閘道的相互驗證和 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="e5c6c-227">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="e5c6c-228">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-228">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-229">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-229">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-230">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-230">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-231">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-231">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-232">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-232">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="e5c6c-233">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-233">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="e5c6c-234">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-234">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="e5c6c-235">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-235">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="e5c6c-236">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-236">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="e5c6c-237">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-237">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="e5c6c-238">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-238">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="e5c6c-239">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-239">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="e5c6c-240">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-240">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="e5c6c-241">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-241">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="e5c6c-242">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-242">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="e5c6c-243">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-243">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="e5c6c-244">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-244">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-245">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-245">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-246">指定原則 BackupTime 的格式為 UTC。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-246">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="e5c6c-247">修改 Get-AzRecoveryServicesBackupJobDetails Cmdlet 中的中斷性變更警告。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-247">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="e5c6c-248">更新 Set-AzRecoveryServicesBackupProtectionPolicy Cmdlet 的範例指令碼解說文字。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-248">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-249">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-250">已修正 What-If 會顯示兩個大小寫不同的資源群組範圍的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-250">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="e5c6c-251">已將 'Export-AzResourceGroup' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-251">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="e5c6c-252">已將文化特性資訊新增至 parse 方法</span><span class="sxs-lookup"><span data-stu-id="e5c6c-252">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-253">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-253">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-254">已修正 Set-AzSqlDatabaseAudit 不支援超大規模資料庫資料庫和資料庫版本無法判斷的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-254">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="e5c6c-255">已將 MaintenanceConfigurationId 新增至 New-AzSqlInstance' 和 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-255">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="e5c6c-256">已修正 GetAzureSqlDatabaseReplicationLink.cs 中的錯誤 (bug)：PartnerServerName 參數會以值進行檢查，而非索引鍵</span><span class="sxs-lookup"><span data-stu-id="e5c6c-256">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-257">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-257">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-258">新增最新存取限制功能的支援：ServiceTag、multi-ip 和 http-headers</span><span class="sxs-lookup"><span data-stu-id="e5c6c-258">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="e5c6c-259">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="e5c6c-259">Thanks to our community contributors</span></span>
* <span data-ttu-id="e5c6c-260">John Q. Martin (@johnmart82)，新增防火牆必要條件資訊 (#13385)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-260">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="e5c6c-261">Manikandan Duraisamy (@madurais-msft)，修正 PublicSubnetName 引數 (#13417)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-261">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="e5c6c-262">@mahortas，更新 -HostNames 參數值 (#13349)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-262">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="e5c6c-263">@MariachiForHire，新增支援的 TrafficAnalyticsInterval 值 (#13304)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-263">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="e5c6c-264">Michael James (@mikejwhat)，允許 Get-AzLogicAppRunHistory 傳回超過 30 個項目 (#13393)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-264">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="e5c6c-265">Shashikant Shakya (@shshakya)，更新 Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-265">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="e5c6c-266">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-266">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-267">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-268">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-268">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="e5c6c-269">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-269">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-270">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-271">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-271">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="e5c6c-272">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-272">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="e5c6c-273">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-273">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="e5c6c-274">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-274">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="e5c6c-275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e5c6c-275">Az.Billing</span></span>
* <span data-ttu-id="e5c6c-276">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-276">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="e5c6c-277">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-277">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="e5c6c-278">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-278">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="e5c6c-279">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-279">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="e5c6c-280">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="e5c6c-280">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-281">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-281">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-282">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-282">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-283">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-284">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-284">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-285">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-286">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-286">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="e5c6c-287">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-287">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-288">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-288">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="e5c6c-289">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-289">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="e5c6c-290">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-290">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="e5c6c-291">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-291">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e5c6c-292">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="e5c6c-292">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="e5c6c-293">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-293">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="e5c6c-294">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-294">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="e5c6c-295">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-295">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="e5c6c-296">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-296">Az.Databricks</span></span>
* <span data-ttu-id="e5c6c-297">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-297">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-298">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-298">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-299">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-299">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="e5c6c-300">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="e5c6c-300">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="e5c6c-301">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="e5c6c-301">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="e5c6c-302">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="e5c6c-302">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="e5c6c-303">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-303">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="e5c6c-304">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-304">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="e5c6c-305">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-305">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="e5c6c-306">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-306">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e5c6c-307">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e5c6c-307">Az.Functions</span></span>
* <span data-ttu-id="e5c6c-308">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-308">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="e5c6c-309">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-309">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="e5c6c-310">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-310">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="e5c6c-311">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-311">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="e5c6c-312">[#12728]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-312">[#12728]</span></span>
  - <span data-ttu-id="e5c6c-313">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-313">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="e5c6c-314">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-314">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="e5c6c-315">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-315">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="e5c6c-316">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-316">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-317">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-317">Az.HDInsight</span></span>
 * <span data-ttu-id="e5c6c-318">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-318">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="e5c6c-319">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-319">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="e5c6c-320">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-320">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="e5c6c-321">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-321">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="e5c6c-322">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-322">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="e5c6c-323">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-323">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="e5c6c-324">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-324">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="e5c6c-325">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-325">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="e5c6c-326">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-326">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="e5c6c-327">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-327">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="e5c6c-328">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-328">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="e5c6c-329">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-329">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="e5c6c-330">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-330">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="e5c6c-331">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-331">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="e5c6c-332">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-332">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="e5c6c-333">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-333">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="e5c6c-334">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-334">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="e5c6c-335">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-335">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="e5c6c-336">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-336">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="e5c6c-337">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="e5c6c-337">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-338">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-338">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-339">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-339">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="e5c6c-340">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-340">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="e5c6c-341">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="e5c6c-341">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="e5c6c-342">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-342">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="e5c6c-343">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="e5c6c-343">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e5c6c-344">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-344">Az.ManagedServices</span></span>
* <span data-ttu-id="e5c6c-345">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-345">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-346">Az.Network</span></span>
* <span data-ttu-id="e5c6c-347">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-347">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="e5c6c-348">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-348">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="e5c6c-349">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-349">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="e5c6c-350">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-350">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="e5c6c-351">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-351">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="e5c6c-352">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-352">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="e5c6c-353">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="e5c6c-353">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="e5c6c-354">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-354">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="e5c6c-355">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-355">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="e5c6c-356">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-356">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="e5c6c-357">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-357">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="e5c6c-358">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-358">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="e5c6c-359">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-359">Added parameter '-Type'</span></span>
    - <span data-ttu-id="e5c6c-360">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-360">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="e5c6c-361">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-361">Added parameter '-Scope'</span></span>
* <span data-ttu-id="e5c6c-362">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-362">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-363">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-364">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-364">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="e5c6c-365">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-365">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-366">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-367">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-367">Fixed parsing bug</span></span>
* <span data-ttu-id="e5c6c-368">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-368">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="e5c6c-369">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-369">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="e5c6c-370">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-370">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="e5c6c-371">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-371">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="e5c6c-372">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-372">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="e5c6c-373">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-373">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="e5c6c-374">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-374">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="e5c6c-375">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-375">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-376">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-377">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-377">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="e5c6c-378">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-378">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="e5c6c-379">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-379">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-380">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-381">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="e5c6c-381">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="e5c6c-382">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-382">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-383">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-383">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-384">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-384">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="e5c6c-385">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-385">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="e5c6c-386">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="e5c6c-386">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="e5c6c-387">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-387">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="e5c6c-388">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-388">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="e5c6c-389">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-389">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="e5c6c-390">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-390">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="e5c6c-391">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-391">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="e5c6c-392">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-392">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="e5c6c-393">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-393">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="e5c6c-394">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="e5c6c-394">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="e5c6c-395">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-395">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="e5c6c-396">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-396">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="e5c6c-397">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-397">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="e5c6c-398">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-398">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="e5c6c-399">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-399">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="e5c6c-400">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-400">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="e5c6c-401">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="e5c6c-401">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="e5c6c-402">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-402">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="e5c6c-403">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-403">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="e5c6c-404">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-404">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="e5c6c-405">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-405">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-406">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-406">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-407">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-407">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="e5c6c-408">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-408">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="e5c6c-409">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="e5c6c-409">Thanks to our community contributors</span></span>
* <span data-ttu-id="e5c6c-410">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-410">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="e5c6c-411">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-411">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="e5c6c-412">(#13249)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-412">(#13249)</span></span>
* <span data-ttu-id="e5c6c-413">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-413">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="e5c6c-414">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-414">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="e5c6c-415">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-415">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="e5c6c-416">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-416">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="e5c6c-417">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-417">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="e5c6c-418">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-418">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="e5c6c-419">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-419">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="e5c6c-420">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-420">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="e5c6c-421">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-421">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="e5c6c-422">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-422">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-423">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-423">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-424">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-424">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-425">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-425">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-426">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-426">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-427">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-427">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-428">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-429">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-429">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="e5c6c-430">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-430">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="e5c6c-431">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-431">Az.Databricks</span></span>
* <span data-ttu-id="e5c6c-432">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-432">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="e5c6c-433">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-433">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-434">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-434">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-435">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-435">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-436">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-436">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-437">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-437">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-438">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-438">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-439">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-439">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="e5c6c-440">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-440">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="e5c6c-441">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-441">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="e5c6c-442">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-442">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="e5c6c-443">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-443">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="e5c6c-444">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-444">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-445">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-446">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-446">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-447">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-448">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="e5c6c-448">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e5c6c-449">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-449">Az.ManagedServices</span></span>
* <span data-ttu-id="e5c6c-450">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="e5c6c-450">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-451">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-452">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-452">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="e5c6c-453">[#12889]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-453">[#12889]</span></span>
* <span data-ttu-id="e5c6c-454">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-454">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="e5c6c-455">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-455">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-456">Az.Network</span></span>
* <span data-ttu-id="e5c6c-457">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-457">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="e5c6c-458">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-458">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-459">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-460">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-460">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e5c6c-461">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e5c6c-461">Az.RedisCache</span></span>
* <span data-ttu-id="e5c6c-462">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="e5c6c-462">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-463">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-463">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-464">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-464">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="e5c6c-465">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-465">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="e5c6c-466">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-466">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="e5c6c-467">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-467">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="e5c6c-468">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-468">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="e5c6c-469">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-469">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-470">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-471">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-471">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="e5c6c-472">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-472">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="e5c6c-473">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-473">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="e5c6c-474">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-474">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="e5c6c-475">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-475">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="e5c6c-476">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-476">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="e5c6c-477">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-477">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="e5c6c-478">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-478">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="e5c6c-479">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-479">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="e5c6c-480">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-480">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="e5c6c-481">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-481">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-482">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-482">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-483">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-483">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="e5c6c-484">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-484">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="e5c6c-485">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-485">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="e5c6c-486">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-486">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-487">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-488">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-488">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="e5c6c-489">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="e5c6c-489">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-490">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-490">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-491">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-491">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="e5c6c-492">[#12372]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-492">[#12372]</span></span>
* <span data-ttu-id="e5c6c-493">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-493">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="e5c6c-494">[#11239]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-494">[#11239]</span></span>
* <span data-ttu-id="e5c6c-495">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-495">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="e5c6c-496">[#11239]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-496">[#11239]</span></span>
* <span data-ttu-id="e5c6c-497">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-497">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="e5c6c-498">[#12371]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-498">[#12371]</span></span>
* <span data-ttu-id="e5c6c-499">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-499">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-500">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-500">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-501">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-501">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-502">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-503">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-503">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="e5c6c-504">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-504">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="e5c6c-505">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-505">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="e5c6c-506">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-506">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="e5c6c-507">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="e5c6c-507">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="e5c6c-508">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-508">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="e5c6c-509">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-509">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="e5c6c-510">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5c6c-510">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="e5c6c-511">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-511">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="e5c6c-512">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-512">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-513">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-513">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-514">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-514">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-515">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-515">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-516">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-516">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="e5c6c-517">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-517">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e5c6c-518">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e5c6c-518">Az.Functions</span></span>
* <span data-ttu-id="e5c6c-519">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-519">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="e5c6c-520">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-520">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="e5c6c-521">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-521">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-522">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-523">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="e5c6c-523">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="e5c6c-524">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-524">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="e5c6c-525">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-525">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="e5c6c-526">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-526">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-527">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-527">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-528">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-528">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-529">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-529">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-530">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-530">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-531">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-532">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-532">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="e5c6c-533">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-533">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="e5c6c-534">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="e5c6c-534">Az.Kusto</span></span>
* <span data-ttu-id="e5c6c-535">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-535">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-536">Az.Network</span></span>
* <span data-ttu-id="e5c6c-537">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="e5c6c-537">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="e5c6c-538">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-538">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="e5c6c-539">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-539">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="e5c6c-540">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-540">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="e5c6c-541">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-541">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="e5c6c-542">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="e5c6c-542">Added subscription level parameter set</span></span>
    - <span data-ttu-id="e5c6c-543">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-543">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="e5c6c-544">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-544">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="e5c6c-545">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-545">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="e5c6c-546">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-546">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="e5c6c-547">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-547">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="e5c6c-548">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-548">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="e5c6c-549">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-549">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="e5c6c-550">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-550">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="e5c6c-551">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-551">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="e5c6c-552">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-552">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="e5c6c-553">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-553">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="e5c6c-554">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-554">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="e5c6c-555">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-555">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="e5c6c-556">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-556">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="e5c6c-557">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-557">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="e5c6c-558">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-558">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="e5c6c-559">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-559">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="e5c6c-560">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-560">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-561">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-561">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-562">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-562">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-563">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-564">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="e5c6c-564">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="e5c6c-565">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-565">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="e5c6c-566">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-566">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="e5c6c-567">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-567">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-569">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-569">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="e5c6c-570">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-570">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="e5c6c-571">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-571">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="e5c6c-572">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-572">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="e5c6c-573">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-573">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="e5c6c-574">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-574">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="e5c6c-575">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-575">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="e5c6c-576">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-576">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="e5c6c-577">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-577">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="e5c6c-578">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-578">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="e5c6c-579">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-579">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="e5c6c-580">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-580">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="e5c6c-581">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-581">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="e5c6c-582">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-582">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="e5c6c-583">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-583">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="e5c6c-584">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-584">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-585">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-586">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-586">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="e5c6c-587">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-587">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-588">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-588">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-589">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-589">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="e5c6c-590">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-590">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="e5c6c-591">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-591">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="e5c6c-592">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-592">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="e5c6c-593">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-593">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="e5c6c-594">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-594">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="e5c6c-595">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-595">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-596">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-596">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-597">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-597">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-598">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-598">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="e5c6c-599">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-599">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="e5c6c-600">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="e5c6c-600">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="e5c6c-601">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-601">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="e5c6c-602">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="e5c6c-602">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="e5c6c-603">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-603">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-604">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-605">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-605">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="e5c6c-606">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="e5c6c-606">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="e5c6c-607">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-607">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-608">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-608">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="e5c6c-609">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-609">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="e5c6c-610">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-610">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="e5c6c-611">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="e5c6c-611">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="e5c6c-612">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-612">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-613">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-613">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="e5c6c-614">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-614">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="e5c6c-615">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-615">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="e5c6c-616">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-616">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="e5c6c-617">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-617">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="e5c6c-618">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-618">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="e5c6c-619">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-619">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="e5c6c-620">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="e5c6c-620">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="e5c6c-621">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="e5c6c-621">Thanks to our community contributors</span></span>
* <span data-ttu-id="e5c6c-622">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-622">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="e5c6c-623">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-623">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="e5c6c-624">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-624">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="e5c6c-625">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-625">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="e5c6c-626">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-626">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="e5c6c-627">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-627">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="e5c6c-628">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-628">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="e5c6c-629">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-629">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="e5c6c-630">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-630">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="e5c6c-631">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-631">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="e5c6c-632">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-632">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="e5c6c-633">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-633">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="e5c6c-634">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-634">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-635">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-635">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="e5c6c-636">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-636">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-637">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-637">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-638">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-638">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="e5c6c-639">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-639">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-640">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-640">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-641">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-641">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-642">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-642">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-643">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-643">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="e5c6c-644">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-644">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="e5c6c-645">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-645">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="e5c6c-646">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-646">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-647">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-647">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-648">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-648">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-649">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-650">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-650">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-651">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-652">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-652">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="e5c6c-653">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-653">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="e5c6c-654">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-654">Az.Maintenance</span></span>
* <span data-ttu-id="e5c6c-655">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-655">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="e5c6c-656">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-656">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e5c6c-657">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-657">Az.ManagedServices</span></span>
* <span data-ttu-id="e5c6c-658">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="e5c6c-658">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-659">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-659">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-660">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-660">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="e5c6c-661">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-661">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-662">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-663">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-663">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="e5c6c-664">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-664">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="e5c6c-665">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="e5c6c-665">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="e5c6c-666">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="e5c6c-666">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="e5c6c-667">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="e5c6c-667">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="e5c6c-668">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="e5c6c-668">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="e5c6c-669">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-669">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="e5c6c-670">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-670">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e5c6c-671">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e5c6c-671">Az.SignalR</span></span>
* <span data-ttu-id="e5c6c-672">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-672">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="e5c6c-673">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-673">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-674">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-674">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-675">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="e5c6c-675">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="e5c6c-676">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-676">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="e5c6c-677">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-677">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="e5c6c-678">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-678">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="e5c6c-679">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-679">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="e5c6c-680">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-680">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="e5c6c-681">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-681">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="e5c6c-682">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-682">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="e5c6c-683">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-683">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="e5c6c-684">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-684">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="e5c6c-685">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-685">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="e5c6c-686">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-686">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="e5c6c-687">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-687">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="e5c6c-688">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="e5c6c-688">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="e5c6c-689">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-689">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="e5c6c-690">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-690">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-691">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-692">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-692">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="e5c6c-693">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-693">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="e5c6c-694">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-694">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="e5c6c-695">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-695">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="e5c6c-696">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-696">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-697">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-697">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-698">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-698">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="e5c6c-699">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-699">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-700">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-700">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-701">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-701">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-702">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-702">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-703">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-703">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-704">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-704">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-705">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-705">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-706">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-706">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-707">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-707">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-708">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-708">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-709">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-709">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-710">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-710">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-711">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-711">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-712">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-712">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-713">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-714">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-714">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-715">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-716">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-716">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-717">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-717">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-718">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-718">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="e5c6c-719">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-719">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="e5c6c-720">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-720">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="e5c6c-721">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-721">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="e5c6c-722">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-722">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="e5c6c-723">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-723">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="e5c6c-724">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-724">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-725">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-725">Az.Network</span></span>
* <span data-ttu-id="e5c6c-726">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-726">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="e5c6c-727">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-727">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="e5c6c-728">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-728">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="e5c6c-729">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-729">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-730">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-730">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-731">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-731">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="e5c6c-732">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-732">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="e5c6c-733">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-733">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-735">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-735">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-736">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-736">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-737">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-737">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="e5c6c-738">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-738">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-739">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-739">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-740">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-740">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="e5c6c-741">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-741">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-742">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-742">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-743">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-743">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="e5c6c-744">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-744">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="e5c6c-745">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-745">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="e5c6c-746">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-746">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="e5c6c-747">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-747">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="e5c6c-748">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-748">Supported get single file share usage</span></span>
    - <span data-ttu-id="e5c6c-749">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-749">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="e5c6c-750">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-750">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-751">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-752">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-752">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="e5c6c-753">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-753">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-754">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-754">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-755">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-755">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-756">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-756">Az.AnalysisServices</span></span>
* <span data-ttu-id="e5c6c-757">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="e5c6c-757">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-758">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-758">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-759">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-759">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-760">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-761">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="e5c6c-761">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-762">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-763">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-763">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e5c6c-764">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e5c6c-764">Az.EventGrid</span></span>
* <span data-ttu-id="e5c6c-765">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-765">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="e5c6c-766">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-766">Added new features:</span></span>
    - <span data-ttu-id="e5c6c-767">輸入對應</span><span class="sxs-lookup"><span data-stu-id="e5c6c-767">Input mapping</span></span>
    - <span data-ttu-id="e5c6c-768">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-768">Event Delivery Schema</span></span>
    - <span data-ttu-id="e5c6c-769">私人連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-769">Private Link</span></span>
    - <span data-ttu-id="e5c6c-770">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-770">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="e5c6c-771">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="e5c6c-771">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="e5c6c-772">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="e5c6c-772">Azure Function As Destination</span></span>
    - <span data-ttu-id="e5c6c-773">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-773">WebHook Batching</span></span>
    - <span data-ttu-id="e5c6c-774">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-774">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="e5c6c-775">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="e5c6c-775">IpFiltering</span></span>
* <span data-ttu-id="e5c6c-776">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-776">Updated cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-777">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="e5c6c-777">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="e5c6c-778">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-778">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="e5c6c-779">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-779">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="e5c6c-780">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-780">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="e5c6c-781">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-781">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="e5c6c-782">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="e5c6c-782">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="e5c6c-783">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-783">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="e5c6c-784">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="e5c6c-784">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="e5c6c-785">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-785">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-786">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-786">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-787">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="e5c6c-787">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="e5c6c-788">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-788">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-789">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-789">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-790">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-790">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-791">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-791">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-792">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-792">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-793">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-793">Az.Network</span></span>
* <span data-ttu-id="e5c6c-794">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="e5c6c-794">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="e5c6c-795">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-795">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="e5c6c-796">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-796">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e5c6c-797">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-797">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e5c6c-798">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-798">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e5c6c-799">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-799">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e5c6c-800">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-800">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="e5c6c-801">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-801">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="e5c6c-802">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-802">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e5c6c-803">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-803">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e5c6c-804">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-804">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e5c6c-805">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-805">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e5c6c-806">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-806">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="e5c6c-807">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-807">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="e5c6c-808">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-808">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="e5c6c-809">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-809">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="e5c6c-810">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-810">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-811">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-812">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="e5c6c-812">Removed project reference to Authentication</span></span>
* <span data-ttu-id="e5c6c-813">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-813">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="e5c6c-814">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-814">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-815">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-816">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-816">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="e5c6c-817">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-817">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-818">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-818">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-819">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-819">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="e5c6c-820">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-820">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="e5c6c-821">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-821">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-822">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-823">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-823">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="e5c6c-824">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-824">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="e5c6c-825">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-825">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="e5c6c-826">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-826">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-827">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="e5c6c-827">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="e5c6c-828">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-828">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="e5c6c-829">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="e5c6c-829">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="e5c6c-830">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-830">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="e5c6c-831">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-831">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="e5c6c-832">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-832">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="e5c6c-833">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-833">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="e5c6c-834">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="e5c6c-834">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="e5c6c-835">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-835">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="e5c6c-836">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-836">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="e5c6c-837">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-837">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="e5c6c-838">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-838">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="e5c6c-839">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-839">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-840">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-840">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-841">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="e5c6c-841">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="e5c6c-842">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-842">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="e5c6c-843">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-843">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="e5c6c-844">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-844">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-845">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-845">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-846">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="e5c6c-846">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="e5c6c-847">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-847">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-848">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-849">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="e5c6c-849">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="e5c6c-850">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-850">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="e5c6c-851">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-851">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="e5c6c-852">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-852">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-853">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-853">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-854">透過對 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-854">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-855">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-855">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-856">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-856">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="e5c6c-857">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-857">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-858">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-858">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-859">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-859">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="e5c6c-860">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-860">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-861">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-861">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-862">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-862">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="e5c6c-863">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-863">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="e5c6c-864">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-864">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="e5c6c-865">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-865">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="e5c6c-866">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-866">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-867">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-868">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-868">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-869">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-869">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-870">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-870">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e5c6c-871">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e5c6c-871">Az.Functions</span></span>
* <span data-ttu-id="e5c6c-872">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-872">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-873">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-873">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-874">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-874">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e5c6c-875">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e5c6c-875">Az.HealthcareApis</span></span>
* <span data-ttu-id="e5c6c-876">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-876">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="e5c6c-877">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-877">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-878">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-879">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-879">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="e5c6c-880">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-880">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-881">Az.Network</span></span>
* <span data-ttu-id="e5c6c-882">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-882">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="e5c6c-883">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-883">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="e5c6c-884">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-884">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="e5c6c-885">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="e5c6c-885">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="e5c6c-886">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-886">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="e5c6c-887">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-887">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="e5c6c-888">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-888">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e5c6c-889">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-889">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e5c6c-890">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-890">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e5c6c-891">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-891">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="e5c6c-892">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-892">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="e5c6c-893">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-893">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="e5c6c-894">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-894">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="e5c6c-895">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-895">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="e5c6c-896">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-896">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="e5c6c-897">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-897">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="e5c6c-898">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-898">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="e5c6c-899">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-899">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="e5c6c-900">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-900">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="e5c6c-901">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-901">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="e5c6c-902">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-902">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="e5c6c-903">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-903">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="e5c6c-904">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="e5c6c-904">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="e5c6c-905">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-905">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="e5c6c-906">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-906">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="e5c6c-907">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-907">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="e5c6c-908">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-908">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="e5c6c-909">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="e5c6c-909">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="e5c6c-910">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-910">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-911">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-911">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-912">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-912">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-913">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-913">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-914">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-914">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-915">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-915">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="e5c6c-916">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-916">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="e5c6c-917">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-917">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="e5c6c-918">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-918">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e5c6c-919">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-919">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e5c6c-920">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-920">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e5c6c-921">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-921">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="e5c6c-922">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-922">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="e5c6c-923">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-923">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="e5c6c-924">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-924">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="e5c6c-925">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-925">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e5c6c-926">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-926">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e5c6c-927">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-927">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="e5c6c-928">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-928">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="e5c6c-929">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-929">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="e5c6c-930">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-930">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-931">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-931">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-932">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-932">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="e5c6c-933">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="e5c6c-933">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="e5c6c-934">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="e5c6c-934">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="e5c6c-935">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-935">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="e5c6c-936">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-936">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-937">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-937">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-938">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-938">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="e5c6c-939">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-939">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-940">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-940">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-941">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-941">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="e5c6c-942">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-942">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="e5c6c-943">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-943">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="e5c6c-944">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-944">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="e5c6c-945">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-945">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="e5c6c-946">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-946">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-947">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-947">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-948">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-948">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="e5c6c-949">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-949">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="e5c6c-950">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-950">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-951">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-952">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-952">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="e5c6c-953">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-953">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-954">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-954">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-955">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-955">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-956">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-956">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e5c6c-957">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-957">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="e5c6c-958">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-958">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="e5c6c-959">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-959">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="e5c6c-960">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-960">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="e5c6c-961">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="e5c6c-961">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="e5c6c-962">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-962">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-963">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-963">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-964">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-964">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-965">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-965">Az.AnalysisServices</span></span>
* <span data-ttu-id="e5c6c-966">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-966">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-967">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-967">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-968">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-968">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="e5c6c-969">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e5c6c-969">Az.Billing</span></span>
* <span data-ttu-id="e5c6c-970">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-970">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-971">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-971">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-972">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-972">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-973">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-974">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-974">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="e5c6c-975">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-975">Az.DataShare</span></span>
* <span data-ttu-id="e5c6c-976">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-976">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="e5c6c-977">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="e5c6c-977">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="e5c6c-978">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-978">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-979">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-980">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-980">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="e5c6c-981">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="e5c6c-981">Added optional parameters to</span></span> 
    - <span data-ttu-id="e5c6c-982">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-982">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="e5c6c-983">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-983">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-984">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-984">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-985">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="e5c6c-985">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e5c6c-986">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e5c6c-986">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e5c6c-987">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-987">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e5c6c-988">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e5c6c-988">Az.PrivateDns</span></span>
* <span data-ttu-id="e5c6c-989">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-989">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-990">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-990">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-991">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-991">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="e5c6c-992">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-992">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-993">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-994">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-994">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="e5c6c-995">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="e5c6c-995">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="e5c6c-996">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-996">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="e5c6c-997">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-997">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="e5c6c-998">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-998">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-999">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1000">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1000">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e5c6c-1001">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1001">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e5c6c-1002">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1002">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1003">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1004">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1004">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="e5c6c-1005">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1005">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e5c6c-1006">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1006">Highlights since the last release</span></span>
* <span data-ttu-id="e5c6c-1007">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1007">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="e5c6c-1008">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1008">General availability of Az.Functions</span></span> 
* <span data-ttu-id="e5c6c-1009">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1009">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1010">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1011">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1011">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="e5c6c-1012">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1012">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-1013">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1013">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-1014">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1014">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="e5c6c-1015">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1015">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="e5c6c-1016">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1016">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-1017">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1017">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-1018">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1018">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="e5c6c-1019">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1019">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="e5c6c-1020">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1020">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e5c6c-1021">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1021">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e5c6c-1022">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1022">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e5c6c-1023">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1023">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="e5c6c-1024">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1024">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e5c6c-1025">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1025">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e5c6c-1026">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1026">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e5c6c-1027">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1027">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e5c6c-1028">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1028">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="e5c6c-1029">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1029">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="e5c6c-1030">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1030">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="e5c6c-1031">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1031">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="e5c6c-1032">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1032">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="e5c6c-1033">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1033">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e5c6c-1034">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1034">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e5c6c-1035">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1035">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="e5c6c-1036">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1036">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="e5c6c-1037">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1037">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-1038">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1038">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-1039">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1039">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="e5c6c-1040">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1040">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="e5c6c-1041">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1041">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="e5c6c-1042">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1042">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="e5c6c-1043">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1043">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="e5c6c-1044">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1044">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="e5c6c-1045">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1045">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="e5c6c-1046">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1046">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="e5c6c-1047">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1047">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1048">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1049">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1049">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="e5c6c-1050">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1050">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="e5c6c-1051">重大變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1051">Breaking changes</span></span>
    - <span data-ttu-id="e5c6c-1052">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1052">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="e5c6c-1053">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1053">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="e5c6c-1054">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1054">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="e5c6c-1055">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1055">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="e5c6c-1056">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1056">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="e5c6c-1057">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1057">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="e5c6c-1058">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1058">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1059">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1060">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1060">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-1061">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1061">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-1062">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1062">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e5c6c-1063">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1063">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e5c6c-1064">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1064">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="e5c6c-1065">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1065">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e5c6c-1066">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1066">Az.Functions</span></span>
* <span data-ttu-id="e5c6c-1067">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1067">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-1068">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1068">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-1069">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1069">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e5c6c-1070">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1070">Az.HealthcareApis</span></span>
* <span data-ttu-id="e5c6c-1071">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1071">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1072">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1072">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1073">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1073">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="e5c6c-1074">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1074">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="e5c6c-1075">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1075">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="e5c6c-1076">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1076">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="e5c6c-1077">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1077">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="e5c6c-1078">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1078">New cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1079">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1079">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1080">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1080">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1081">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1081">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1082">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1082">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="e5c6c-1083">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1083">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="e5c6c-1084">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1084">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1085">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1085">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1086">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1086">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="e5c6c-1087">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1087">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="e5c6c-1088">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1088">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="e5c6c-1089">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1089">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="e5c6c-1090">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1090">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="e5c6c-1091">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1091">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="e5c6c-1092">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1092">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1093">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1093">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1094">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1094">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="e5c6c-1095">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1095">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="e5c6c-1096">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1096">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="e5c6c-1097">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1097">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="e5c6c-1098">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1098">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="e5c6c-1099">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1099">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="e5c6c-1100">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1100">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1101">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1101">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1102">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1102">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="e5c6c-1103">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1103">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="e5c6c-1104">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1104">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="e5c6c-1105">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1105">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="e5c6c-1106">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1106">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="e5c6c-1107">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1108">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1108">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e5c6c-1109">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1109">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e5c6c-1110">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1110">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e5c6c-1111">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1111">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="e5c6c-1112">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1112">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="e5c6c-1113">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1113">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="e5c6c-1114">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1114">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="e5c6c-1115">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1115">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="e5c6c-1116">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1116">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="e5c6c-1117">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1117">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="e5c6c-1118">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1118">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="e5c6c-1119">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1119">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e5c6c-1120">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1120">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e5c6c-1121">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1121">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e5c6c-1122">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1122">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="e5c6c-1123">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1123">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="e5c6c-1124">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1124">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="e5c6c-1125">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1125">Updated cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-1126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1126">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-1127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1127">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-1128">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1128">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="e5c6c-1129">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1129">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="e5c6c-1130">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1130">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="e5c6c-1131">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1131">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="e5c6c-1132">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1132">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="e5c6c-1133">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1133">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="e5c6c-1134">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1134">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="e5c6c-1135">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1135">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1136">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1137">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1137">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="e5c6c-1138">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1138">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="e5c6c-1139">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1139">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="e5c6c-1140">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1140">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="e5c6c-1141">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1141">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1142">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1143">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1143">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="e5c6c-1144">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1144">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="e5c6c-1145">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1145">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="e5c6c-1146">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1146">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="e5c6c-1147">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1147">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="e5c6c-1148">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1148">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="e5c6c-1149">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1149">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="e5c6c-1150">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1150">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="e5c6c-1151">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1151">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="e5c6c-1152">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1152">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="e5c6c-1153">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1153">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="e5c6c-1154">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1154">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="e5c6c-1155">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1155">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="e5c6c-1156">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1156">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="e5c6c-1157">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1157">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="e5c6c-1158">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1158">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="e5c6c-1159">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1159">'New-AzDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1160">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1160">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1161">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1161">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e5c6c-1162">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1162">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-1163">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1163">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-1164">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1164">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1165">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1165">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1166">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1166">Enhance performance of:</span></span>
    - <span data-ttu-id="e5c6c-1167">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1167">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e5c6c-1168">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1168">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e5c6c-1169">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1169">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e5c6c-1170">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1170">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e5c6c-1171">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1171">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e5c6c-1172">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1172">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e5c6c-1173">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1173">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e5c6c-1174">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1174">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="e5c6c-1175">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1175">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="e5c6c-1176">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1176">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1177">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1178">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1178">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-1179">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1179">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="e5c6c-1180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-1181">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1181">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="e5c6c-1182">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1182">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e5c6c-1183">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1183">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="e5c6c-1184">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1184">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="e5c6c-1185">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1185">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="e5c6c-1186">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1186">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="e5c6c-1187">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1187">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="e5c6c-1188">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1188">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="e5c6c-1189">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1189">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="e5c6c-1190">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1190">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="e5c6c-1191">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1191">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="e5c6c-1192">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1192">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="e5c6c-1193">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1193">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-1194">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1194">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="e5c6c-1195">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1195">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="e5c6c-1196">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1196">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e5c6c-1197">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1197">Supported failover Storage account</span></span>
    - <span data-ttu-id="e5c6c-1198">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1198">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="e5c6c-1199">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1199">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="e5c6c-1200">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1200">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="e5c6c-1201">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1201">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="e5c6c-1202">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1202">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e5c6c-1203">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1203">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="e5c6c-1204">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1204">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="e5c6c-1205">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1205">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e5c6c-1206">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1206">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e5c6c-1207">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1207">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="e5c6c-1208">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1208">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e5c6c-1209">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1209">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="e5c6c-1210">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1210">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e5c6c-1211">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1211">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e5c6c-1212">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1212">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="e5c6c-1213">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1213">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="e5c6c-1214">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1214">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="e5c6c-1215">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1215">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="e5c6c-1216">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1216">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e5c6c-1217">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1217">Az.TrafficManager</span></span>
* <span data-ttu-id="e5c6c-1218">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1218">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-1219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1219">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-1220">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1220">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="e5c6c-1221">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1221">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e5c6c-1222">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1222">Highlights since the last release</span></span>
* <span data-ttu-id="e5c6c-1223">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1223">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1224">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1224">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1225">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1225">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-1226">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1226">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-1227">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1227">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e5c6c-1228">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1228">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-1229">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1229">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-1230">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1230">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-1231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1231">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-1232">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1232">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1233">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1234">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1234">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1235">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1235">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1236">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1237">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1237">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1238">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1238">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="e5c6c-1239">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1239">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="e5c6c-1240">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1240">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="e5c6c-1241">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1241">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1242">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1242">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="e5c6c-1243">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1243">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="e5c6c-1244">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1244">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="e5c6c-1245">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1245">New cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1246">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1246">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-1247">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1247">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-1248">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1248">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e5c6c-1249">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1249">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="e5c6c-1250">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1250">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1251">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1252">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1252">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="e5c6c-1253">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1253">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="e5c6c-1254">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1254">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="e5c6c-1255">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1255">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="e5c6c-1256">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1256">Az.Maintenance</span></span>
* <span data-ttu-id="e5c6c-1257">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1257">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1258">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1259">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1259">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="e5c6c-1260">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1260">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e5c6c-1261">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1261">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e5c6c-1262">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1262">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e5c6c-1263">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1263">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e5c6c-1264">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1264">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e5c6c-1265">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1265">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e5c6c-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1267">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1268">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1268">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="e5c6c-1269">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1269">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e5c6c-1270">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1270">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e5c6c-1271">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1271">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="e5c6c-1272">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1272">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="e5c6c-1273">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1273">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="e5c6c-1274">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1274">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="e5c6c-1275">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1275">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="e5c6c-1276">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1276">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="e5c6c-1277">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1277">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e5c6c-1278">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1278">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="e5c6c-1279">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1279">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e5c6c-1280">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1280">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="e5c6c-1281">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1281">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="e5c6c-1282">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1282">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="e5c6c-1283">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1283">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-1284">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1284">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-1285">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1285">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="e5c6c-1286">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1286">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-1287">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1287">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-1288">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1288">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1289">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1290">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1290">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="e5c6c-1291">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1291">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1292">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1293">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1293">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e5c6c-1294">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1294">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="e5c6c-1295">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1295">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="e5c6c-1296">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1296">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e5c6c-1297">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1297">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="e5c6c-1298">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1298">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e5c6c-1299">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1299">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e5c6c-1300">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1300">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="e5c6c-1301">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1301">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e5c6c-1302">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1302">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="e5c6c-1303">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1303">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e5c6c-1304">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1304">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="e5c6c-1305">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1305">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="e5c6c-1306">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1306">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="e5c6c-1307">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1307">General</span></span>
* <span data-ttu-id="e5c6c-1308">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1308">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="e5c6c-1309">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1309">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="e5c6c-1310">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1310">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="e5c6c-1311">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1311">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="e5c6c-1312">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1312">Az.Billing</span></span>
  - <span data-ttu-id="e5c6c-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1313">Az.Compute</span></span>
  - <span data-ttu-id="e5c6c-1314">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1314">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="e5c6c-1315">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1315">Az.EventHub</span></span>
  - <span data-ttu-id="e5c6c-1316">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1316">Az.IotHub</span></span>
  - <span data-ttu-id="e5c6c-1317">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1317">Az.KeyVault</span></span>
  - <span data-ttu-id="e5c6c-1318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1318">Az.Monitor</span></span>
  - <span data-ttu-id="e5c6c-1319">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1319">Az.Network</span></span>
  - <span data-ttu-id="e5c6c-1320">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1320">Az.Resources</span></span>
  - <span data-ttu-id="e5c6c-1321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1321">Az.Storage</span></span>
  - <span data-ttu-id="e5c6c-1322">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1322">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-1323">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1323">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-1324">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1324">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="e5c6c-1325">您可以在[這裡](/azure-stack/operator/powershell-install-az-module)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1325">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="e5c6c-1326">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1326">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1327">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1328">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1328">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1329">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1330">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1330">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="e5c6c-1331">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1331">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="e5c6c-1332">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1332">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1333">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1333">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="e5c6c-1334">[#11354]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1334">[#11354]</span></span>
* <span data-ttu-id="e5c6c-1335">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1335">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="e5c6c-1336">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1336">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e5c6c-1337">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1337">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e5c6c-1338">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1338">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e5c6c-1339">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1339">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="e5c6c-1340">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1340">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="e5c6c-1341">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1341">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="e5c6c-1342">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1342">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="e5c6c-1343">[#11257]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1343">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1344">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1344">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1345">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1345">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="e5c6c-1346">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1346">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1347">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-1348">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1348">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="e5c6c-1349">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1349">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-1350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1350">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-1351">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1351">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1352">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1352">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1353">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1353">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="e5c6c-1354">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1354">New Cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1355">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1355">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="e5c6c-1356">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1356">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1357">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1357">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1358">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1358">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1359">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1359">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1360">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1360">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1361">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1362">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1362">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="e5c6c-1363">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1363">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e5c6c-1364">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1364">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e5c6c-1365">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1365">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="e5c6c-1366">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1366">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="e5c6c-1367">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1367">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-1368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1368">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-1369">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1369">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1371">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1371">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="e5c6c-1372">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1372">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="e5c6c-1373">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1373">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="e5c6c-1374">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1374">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="e5c6c-1375">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1375">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="e5c6c-1376">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1376">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1377">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1378">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1378">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="e5c6c-1379">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1379">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="e5c6c-1380">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1380">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="e5c6c-1381">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1381">Added example.</span></span>
* <span data-ttu-id="e5c6c-1382">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1382">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="e5c6c-1383">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1383">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1384">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1385">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1385">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="e5c6c-1386">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1386">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e5c6c-1387">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1387">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="e5c6c-1388">Az.Support</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1388">Az.Support</span></span>
* <span data-ttu-id="e5c6c-1389">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1389">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-1390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1390">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-1391">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1391">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="e5c6c-1392">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1392">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e5c6c-1393">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1393">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e5c6c-1394">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1394">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e5c6c-1395">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1395">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="e5c6c-1396">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1396">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1397">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1398">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1398">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="e5c6c-1399">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1399">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="e5c6c-1400">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1400">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-1401">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1401">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-1402">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1402">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="e5c6c-1403">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1403">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="e5c6c-1404">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1404">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="e5c6c-1405">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1405">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-1406">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1406">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-1407">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1407">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1408">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1409">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1409">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e5c6c-1410">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1410">New Cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1411">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1411">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1412">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1412">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1413">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1413">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1414">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1414">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="e5c6c-1415">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1415">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="e5c6c-1416">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1416">New Cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1417">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1417">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="e5c6c-1418">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1418">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="e5c6c-1419">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1419">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="e5c6c-1420">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1420">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="e5c6c-1421">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1421">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e5c6c-1422">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1422">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e5c6c-1423">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1423">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="e5c6c-1424">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1424">New Cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1425">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1425">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="e5c6c-1426">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1426">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="e5c6c-1427">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1427">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1428">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1429">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1429">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1430">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1431">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1431">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="e5c6c-1432">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1432">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="e5c6c-1433">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1433">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="e5c6c-1434">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1434">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1435">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1436">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1436">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="e5c6c-1437">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1437">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="e5c6c-1438">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1438">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="e5c6c-1439">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1439">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="e5c6c-1440">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1440">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="e5c6c-1441">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1441">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="e5c6c-1442">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1442">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="e5c6c-1443">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1443">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="e5c6c-1444">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1444">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e5c6c-1445">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1445">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e5c6c-1446">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1446">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="e5c6c-1447">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1447">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="e5c6c-1448">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1448">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="e5c6c-1449">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1449">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1450">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1451">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1451">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="e5c6c-1452">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1452">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="e5c6c-1453">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1453">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="e5c6c-1454">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1454">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="e5c6c-1455">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1455">Remove an LTR backup</span></span>
    - <span data-ttu-id="e5c6c-1456">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1456">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="e5c6c-1457">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1457">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="e5c6c-1458">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1458">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="e5c6c-1459">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1459">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1460">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1461">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1461">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="e5c6c-1462">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1462">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="e5c6c-1463">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1463">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="e5c6c-1464">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1464">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="e5c6c-1465">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1465">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-1466">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1466">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-1467">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1467">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="e5c6c-1468">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1468">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="e5c6c-1469">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1469">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="e5c6c-1470">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1470">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="e5c6c-1471">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1471">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="e5c6c-1472">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1472">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-1473">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1473">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-1474">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1474">Updated client side telemetry.</span></span>
* <span data-ttu-id="e5c6c-1475">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1475">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="e5c6c-1476">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1476">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1477">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1477">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1478">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1478">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-1479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1479">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-1480">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1480">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-1481">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1481">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-1482">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1482">Updated SDK to 7.0</span></span>
* <span data-ttu-id="e5c6c-1483">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1483">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1484">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1485">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1485">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-1486">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1486">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-1487">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1487">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1488">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1488">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1489">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1489">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e5c6c-1490">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1490">New Cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-1491">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1491">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1492">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1492">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1493">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1493">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e5c6c-1494">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1494">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1495">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1495">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1496">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1496">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1497">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1498">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1498">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1499">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1499">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="e5c6c-1500">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1500">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1501">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1501">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1502">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1502">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1503">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1503">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e5c6c-1504">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1504">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e5c6c-1505">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1505">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="e5c6c-1506">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1506">No new cmdlets are added.</span></span> <span data-ttu-id="e5c6c-1507">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1507">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1508">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1508">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1509">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1509">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1510">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1511">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1511">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="e5c6c-1512">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1512">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="e5c6c-1513">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1513">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="e5c6c-1514">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1514">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="e5c6c-1515">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1515">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="e5c6c-1516">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1516">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="e5c6c-1517">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1517">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="e5c6c-1518">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1518">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1519">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1520">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1520">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="e5c6c-1521">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1521">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="e5c6c-1522">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1522">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e5c6c-1523">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1523">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e5c6c-1524">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1524">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-1525">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1525">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-1526">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1526">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="e5c6c-1527">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1527">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-1528">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1528">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-1529">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1529">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="e5c6c-1530">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1530">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1531">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1532">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1532">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="e5c6c-1533">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1533">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-1534">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1534">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-1535">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1535">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="e5c6c-1536">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1536">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="e5c6c-1537"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1537">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="e5c6c-1538">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1538">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1539">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1540">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1540">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="e5c6c-1541">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1541">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="e5c6c-1542">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1542">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-1543">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1543">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="e5c6c-1544">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1544">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1545">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1546">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1546">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e5c6c-1547">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1547">Az.DeploymentManager</span></span>
* <span data-ttu-id="e5c6c-1548">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1548">Adds LIST operations for resources</span></span>
* <span data-ttu-id="e5c6c-1549">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1549">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-1550">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1550">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-1551">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1551">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1552">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1552">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1553">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1553">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1554">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1555">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1555">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="e5c6c-1556">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1556">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="e5c6c-1557">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1557">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-1558">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1558">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="e5c6c-1559">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1559">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="e5c6c-1560">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1560">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="e5c6c-1561">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1561">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="e5c6c-1562">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1562">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="e5c6c-1563">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1563">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="e5c6c-1565">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1565">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="e5c6c-1566">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1566">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="e5c6c-1567">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1567">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-1568">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1568">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-1569">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1569">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="e5c6c-1570">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1570">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="e5c6c-1571">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1571">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="e5c6c-1572">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1572">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1574">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1574">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="e5c6c-1575">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1575">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1576">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1576">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1577">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1577">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="e5c6c-1578">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1578">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1579">Az.Sql</span></span>
<span data-ttu-id="e5c6c-1580">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1580">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1581">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1582">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1582">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="e5c6c-1583">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1583">New-AzStorageAccount</span></span>
* <span data-ttu-id="e5c6c-1584">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1584">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="e5c6c-1585">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1585">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-1586">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1586">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-1587">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1587">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="e5c6c-1588">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1588">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="e5c6c-1589">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1589">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1590">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1591">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1591">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-1592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1592">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-1593">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1593">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1594">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1595">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1595">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e5c6c-1596">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1596">Az.ContainerInstance</span></span>
* <span data-ttu-id="e5c6c-1597">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1597">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e5c6c-1598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e5c6c-1599">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1599">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e5c6c-1600">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1600">Get the Edge Storage Container</span></span>
* <span data-ttu-id="e5c6c-1601">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1601">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e5c6c-1602">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1602">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="e5c6c-1603">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1603">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e5c6c-1604">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1604">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="e5c6c-1605">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1605">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e5c6c-1606">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1606">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="e5c6c-1607">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1607">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e5c6c-1608">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1608">Get the Edge Storage Account</span></span>
* <span data-ttu-id="e5c6c-1609">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1609">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e5c6c-1610">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1610">Create new Edge Storage Account</span></span>
* <span data-ttu-id="e5c6c-1611">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1611">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e5c6c-1612">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1612">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="e5c6c-1613">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1613">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="e5c6c-1614">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1614">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="e5c6c-1615">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1615">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="e5c6c-1616">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1616">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1617">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1618">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1618">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="e5c6c-1619">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1619">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="e5c6c-1620">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1620">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="e5c6c-1621">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1621">Az.DevTestLabs</span></span>
* <span data-ttu-id="e5c6c-1622">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1622">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1623">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-1624">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1624">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1625">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-1626">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1626">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e5c6c-1627">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1627">Az.MachineLearning</span></span>
* <span data-ttu-id="e5c6c-1628">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1628">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="e5c6c-1629">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1629">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="e5c6c-1630">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1630">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="e5c6c-1631">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1631">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="e5c6c-1632">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1632">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="e5c6c-1633">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1633">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="e5c6c-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="e5c6c-1635">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1635">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1636">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1637">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1637">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1638">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1638">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1639">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1639">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="e5c6c-1640">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1640">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e5c6c-1641">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1641">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e5c6c-1642">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1642">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1643">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1644">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1644">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1645">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1646">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1646">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="e5c6c-1647">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1647">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e5c6c-1648">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1648">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e5c6c-1649">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1649">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1650">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1651">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1651">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="e5c6c-1652">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1652">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="e5c6c-1653">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1653">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="e5c6c-1654">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1654">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="e5c6c-1655">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1655">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="e5c6c-1656">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1656">General</span></span>
* <span data-ttu-id="e5c6c-1657">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1657">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1658">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1658">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1659">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1659">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="e5c6c-1660">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1660">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-1661">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1661">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-1662">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1662">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1663">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1664">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1664">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-1665">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1665">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-1666">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1666">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="e5c6c-1667">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1667">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e5c6c-1668">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1668">Az.HealthcareApis</span></span>
* <span data-ttu-id="e5c6c-1669">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1669">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-1670">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1670">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-1671">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1671">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="e5c6c-1672">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1672">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="e5c6c-1673">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1673">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1674">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1674">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1675">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1675">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="e5c6c-1676">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1676">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="e5c6c-1677">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1677">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1678">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1678">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1679">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1679">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1680">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1680">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1681">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1681">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="e5c6c-1682">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1682">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1683">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1683">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1684">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1684">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1685">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1686">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1686">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="e5c6c-1687">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1687">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="e5c6c-1688">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1688">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="e5c6c-1689">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1689">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="e5c6c-1690">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1690">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="e5c6c-1691">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1691">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="e5c6c-1692">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1692">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="e5c6c-1693">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1693">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="e5c6c-1694">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1694">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="e5c6c-1695">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1695">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="e5c6c-1696">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1696">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="e5c6c-1697">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1697">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="e5c6c-1698">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1698">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="e5c6c-1699">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1699">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-1700">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1700">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-1701">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1701">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="e5c6c-1702">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1702">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1703">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1704">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1704">VM Reapply feature</span></span>
    - <span data-ttu-id="e5c6c-1705">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1705">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="e5c6c-1706">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1706">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="e5c6c-1707">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1707">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="e5c6c-1708">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1708">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="e5c6c-1709">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1709">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e5c6c-1710">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1710">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="e5c6c-1711">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1711">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="e5c6c-1712">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1712">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="e5c6c-1713">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1713">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="e5c6c-1714">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1714">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e5c6c-1715">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1715">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e5c6c-1716">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1716">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e5c6c-1717">取得訂單</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1717">Get the Order</span></span>
* <span data-ttu-id="e5c6c-1718">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1718">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e5c6c-1719">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1719">Create new Order</span></span>
* <span data-ttu-id="e5c6c-1720">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1720">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e5c6c-1721">移除訂單</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1721">Remove the Order</span></span>
* <span data-ttu-id="e5c6c-1722">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1722">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="e5c6c-1723">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1723">Now creates Local Share</span></span>
* <span data-ttu-id="e5c6c-1724">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1724">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="e5c6c-1725">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1725">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="e5c6c-1726">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1726">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="e5c6c-1727">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1727">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="e5c6c-1728">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1728">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e5c6c-1729">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1729">Gets the information about Triggers</span></span>
* <span data-ttu-id="e5c6c-1730">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1730">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e5c6c-1731">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1731">Create new Triggers</span></span>
* <span data-ttu-id="e5c6c-1732">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1732">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e5c6c-1733">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1733">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1734">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1734">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1735">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1735">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="e5c6c-1736">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1736">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-1737">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1737">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-1738">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1738">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-1739">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1739">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-1740">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1740">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-1741">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1741">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-1742">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1742">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="e5c6c-1743">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1743">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="e5c6c-1744">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1744">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="e5c6c-1745">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1745">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1746">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1747">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1747">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e5c6c-1748">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1748">Az.PrivateDns</span></span>
* <span data-ttu-id="e5c6c-1749">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1749">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1751">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1751">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="e5c6c-1752">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1752">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="e5c6c-1753">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1753">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e5c6c-1754">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1754">Az.RedisCache</span></span>
* <span data-ttu-id="e5c6c-1755">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1755">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="e5c6c-1756">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1756">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1757">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1757">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1758">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1758">Az.Resources</span></span>
- <span data-ttu-id="e5c6c-1759">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1759">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="e5c6c-1760">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1760">Updated create policy definition help example</span></span>
- <span data-ttu-id="e5c6c-1761">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1761">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="e5c6c-1762">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1762">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="e5c6c-1763">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1763">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1764">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1764">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1765">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1765">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="e5c6c-1766">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1766">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="e5c6c-1767">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1767">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="e5c6c-1768">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1768">General</span></span>
* <span data-ttu-id="e5c6c-1769">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1769">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1770">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1771">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1771">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e5c6c-1772">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1772">Az.Advisor</span></span>
* <span data-ttu-id="e5c6c-1773">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1773">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-1774">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1774">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-1775">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1775">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="e5c6c-1776">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1776">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="e5c6c-1777">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1777">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="e5c6c-1778">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1778">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="e5c6c-1779">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1779">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="e5c6c-1780">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1780">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="e5c6c-1781">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1781">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="e5c6c-1782">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1782">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="e5c6c-1783">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1783">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="e5c6c-1784">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1784">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e5c6c-1785">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1785">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="e5c6c-1786">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1786">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="e5c6c-1787">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1787">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e5c6c-1788">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1788">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="e5c6c-1789">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1789">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="e5c6c-1790">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1790">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="e5c6c-1791">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1791">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="e5c6c-1792">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1792">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="e5c6c-1793">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1793">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="e5c6c-1794">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1794">This operation is no longer supported.</span></span>
* <span data-ttu-id="e5c6c-1795">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1795">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e5c6c-1796">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1796">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e5c6c-1797">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1797">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="e5c6c-1798">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1798">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="e5c6c-1799">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1799">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="e5c6c-1800">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1800">New non-verified images are also now returned.</span></span> <span data-ttu-id="e5c6c-1801">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1801">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="e5c6c-1802">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1802">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="e5c6c-1803">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1803">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="e5c6c-1804">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1804">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="e5c6c-1805">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1805">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="e5c6c-1806">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1806">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="e5c6c-1807">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1807">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="e5c6c-1808">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1808">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="e5c6c-1809">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1809">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="e5c6c-1810">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1810">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-1811">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1811">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-1812">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1812">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="e5c6c-1813">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1813">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1814">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1814">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1815">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1815">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="e5c6c-1816">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1816">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="e5c6c-1817">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1817">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="e5c6c-1818">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1818">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e5c6c-1819">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1819">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="e5c6c-1820">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1820">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="e5c6c-1821">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1821">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="e5c6c-1822">重大變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1822">Breaking changes</span></span>
    - <span data-ttu-id="e5c6c-1823">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1823">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="e5c6c-1824">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1824">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1825">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1826">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1826">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-1828">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1828">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="e5c6c-1829">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1829">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="e5c6c-1830">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1830">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="e5c6c-1831">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1831">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="e5c6c-1832">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1832">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="e5c6c-1833">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1833">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-1834">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1834">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-1835">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1835">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-1836">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1836">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-1837">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1837">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="e5c6c-1838">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1838">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="e5c6c-1839">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1839">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="e5c6c-1840">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1840">Removed five cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-1841">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1841">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e5c6c-1842">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1842">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e5c6c-1843">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1843">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e5c6c-1844">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1844">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="e5c6c-1845">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1845">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="e5c6c-1846">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1846">Added three cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-1847">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1847">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e5c6c-1848">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1848">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e5c6c-1849">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1849">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="e5c6c-1850">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1850">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="e5c6c-1851">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1851">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="e5c6c-1852">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1852">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="e5c6c-1853">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1853">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="e5c6c-1854">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1854">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="e5c6c-1855">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1855">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="e5c6c-1856">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1856">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="e5c6c-1857">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1857">Added some scenario test cases.</span></span>
* <span data-ttu-id="e5c6c-1858">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1858">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1859">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1859">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1860">重大變更：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1860">Breaking changes:</span></span>
    - <span data-ttu-id="e5c6c-1861">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1861">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e5c6c-1862">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1862">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e5c6c-1863">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1863">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e5c6c-1864">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1864">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e5c6c-1865">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1865">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="e5c6c-1866">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1866">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="e5c6c-1867">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1867">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="e5c6c-1868">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1868">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="e5c6c-1869">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1869">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e5c6c-1870">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1870">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e5c6c-1871">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1871">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e5c6c-1872">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1872">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-1873">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1873">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-1874">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1874">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1875">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1875">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="e5c6c-1876">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1876">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="e5c6c-1877">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1877">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1878">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1878">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1879">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1879">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1880">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1880">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1881">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1881">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-1882">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1882">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1883">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-1884">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1884">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1885">Az.Network</span></span>
* <span data-ttu-id="e5c6c-1886">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1886">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="e5c6c-1887">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1887">Updated cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-1888">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1888">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-1889">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1889">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-1890">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1890">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-1891">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1891">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-1892">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1892">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e5c6c-1893">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1893">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="e5c6c-1894">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1894">New cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-1895">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1895">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="e5c6c-1896">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1896">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="e5c6c-1897">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1897">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="e5c6c-1898">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1898">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="e5c6c-1899">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1899">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="e5c6c-1900">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1900">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="e5c6c-1901">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1901">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="e5c6c-1902">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1902">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="e5c6c-1903">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1903">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1904">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1904">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="e5c6c-1905">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1905">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e5c6c-1906">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1906">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e5c6c-1907">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1907">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e5c6c-1908">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1908">Set-AzVirtualHub</span></span>
* <span data-ttu-id="e5c6c-1909">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1909">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="e5c6c-1910">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1910">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e5c6c-1911">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1911">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e5c6c-1912">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1912">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e5c6c-1913">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1913">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="e5c6c-1914">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1914">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="e5c6c-1915">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1915">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="e5c6c-1916">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1916">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1917">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1917">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="e5c6c-1918">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1918">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e5c6c-1919">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1919">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e5c6c-1920">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1920">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e5c6c-1921">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1921">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e5c6c-1922">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1922">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e5c6c-1923">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1923">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="e5c6c-1924">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1924">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="e5c6c-1925">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1925">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1926">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1926">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="e5c6c-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="e5c6c-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="e5c6c-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="e5c6c-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="e5c6c-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="e5c6c-1932">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1932">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e5c6c-1933">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1933">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="e5c6c-1934">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1934">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="e5c6c-1935">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1935">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="e5c6c-1936">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1936">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="e5c6c-1937">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1937">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e5c6c-1938">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1938">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="e5c6c-1939">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1939">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="e5c6c-1940">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1940">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="e5c6c-1941">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1941">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="e5c6c-1942">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1942">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="e5c6c-1943">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1943">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-1944">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1944">New-AzIpGroup</span></span>
        - <span data-ttu-id="e5c6c-1945">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1945">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="e5c6c-1946">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1946">Get-AzIpGroup</span></span>
        - <span data-ttu-id="e5c6c-1947">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1947">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-1949">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1949">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-1950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1950">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-1951">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1951">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="e5c6c-1952">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1952">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="e5c6c-1953">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1953">Removed deprecated aliases:</span></span>
* <span data-ttu-id="e5c6c-1954">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1954">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="e5c6c-1955">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1955">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="e5c6c-1956">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1956">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e5c6c-1957">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1957">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="e5c6c-1958">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1958">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="e5c6c-1959">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1959">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-1960">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1960">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-1961">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1961">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="e5c6c-1962">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1962">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e5c6c-1963">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1963">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e5c6c-1964">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1964">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="e5c6c-1965">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1965">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="e5c6c-1966">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1966">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="e5c6c-1967">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1967">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e5c6c-1968">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1968">General</span></span>
* <span data-ttu-id="e5c6c-1969">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1969">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-1970">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1970">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-1971">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1971">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-1972">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1972">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-1973">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1973">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e5c6c-1974">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1974">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-1975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1975">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-1976">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1976">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-1977">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1977">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-1978">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1978">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-1979">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1979">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-1980">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1980">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e5c6c-1981">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1981">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e5c6c-1982">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1982">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="e5c6c-1983">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1983">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-1984">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1984">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-1985">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1985">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e5c6c-1986">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1986">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e5c6c-1987">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1987">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-1989">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1989">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e5c6c-1990">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1990">Az.HealthcareApis</span></span>
* <span data-ttu-id="e5c6c-1991">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1991">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e5c6c-1992">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1992">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e5c6c-1993">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1993">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e5c6c-1994">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1994">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-1995">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1995">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-1996">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1996">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e5c6c-1997">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1997">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-1998">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1998">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-1999">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e5c6c-1999">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e5c6c-2000">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2000">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e5c6c-2001">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2001">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e5c6c-2002">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2002">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2003">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2004">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2004">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e5c6c-2005">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2005">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e5c6c-2006">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2006">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-2007">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2007">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e5c6c-2008">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2008">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e5c6c-2009">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2009">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e5c6c-2010">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2010">Updated cmdlets:</span></span>
        - <span data-ttu-id="e5c6c-2011">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2011">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e5c6c-2012">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2012">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e5c6c-2013">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2013">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e5c6c-2014">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2014">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e5c6c-2015">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2015">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e5c6c-2016">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2016">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e5c6c-2017">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2017">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e5c6c-2018">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2018">Az.RedisCache</span></span>
* <span data-ttu-id="e5c6c-2019">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2019">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2020">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2021">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2021">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2022">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2022">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2023">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2023">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e5c6c-2024">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2024">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e5c6c-2025">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2025">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e5c6c-2026">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2026">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e5c6c-2027">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2027">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-2028">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2028">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-2029">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2029">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2030">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2030">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2031">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2031">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e5c6c-2032">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2032">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-2033">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2033">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-2034">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2034">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e5c6c-2035">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2035">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e5c6c-2036">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2036">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2037">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2038">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2038">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e5c6c-2039">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2039">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e5c6c-2040">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2040">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2041">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2041">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2042">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2042">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e5c6c-2043">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2043">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e5c6c-2044">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2044">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e5c6c-2045">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2045">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e5c6c-2046">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2046">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e5c6c-2047">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2047">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e5c6c-2048">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2048">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e5c6c-2049">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2049">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e5c6c-2050">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2050">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2051">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2051">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2052">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2052">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e5c6c-2053">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2053">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-2054">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2054">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-2055">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2055">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-2056">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2056">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-2057">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2057">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e5c6c-2058">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2058">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e5c6c-2059">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2059">New cmdlets are:</span></span>
    - <span data-ttu-id="e5c6c-2060">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2060">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e5c6c-2061">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2061">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e5c6c-2062">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2062">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e5c6c-2063">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2063">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2064">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2064">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-2065">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2065">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e5c6c-2066">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2066">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e5c6c-2067">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2067">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e5c6c-2068">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2068">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e5c6c-2069">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2069">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e5c6c-2070">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2070">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e5c6c-2071">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2071">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e5c6c-2072">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2072">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e5c6c-2073">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2073">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e5c6c-2074">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2074">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e5c6c-2075">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2075">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e5c6c-2076">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2076">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e5c6c-2077">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2077">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e5c6c-2078">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2078">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e5c6c-2079">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2079">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e5c6c-2080">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2080">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e5c6c-2081">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2081">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e5c6c-2082">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2082">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e5c6c-2083">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2083">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e5c6c-2084">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2084">Overall improved help files</span></span>
* <span data-ttu-id="e5c6c-2085">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2085">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2086">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2086">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2087">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2087">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="e5c6c-2088">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2088">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e5c6c-2089">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2089">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e5c6c-2090">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2090">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e5c6c-2091">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2091">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e5c6c-2092">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2092">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e5c6c-2093">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2093">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e5c6c-2094">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2094">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e5c6c-2095">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2095">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e5c6c-2096">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2096">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e5c6c-2097">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2097">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e5c6c-2098">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2098">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e5c6c-2099">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2099">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2100">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2100">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e5c6c-2101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2101">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e5c6c-2102">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2102">Updated cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-2103">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2103">New-VpnSite</span></span>
        - <span data-ttu-id="e5c6c-2104">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2104">Update-VpnSite</span></span>
        - <span data-ttu-id="e5c6c-2105">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2105">New-VpnConnection</span></span>
        - <span data-ttu-id="e5c6c-2106">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2106">Update-VpnConnection</span></span>
* <span data-ttu-id="e5c6c-2107">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2107">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2108">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2109">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2109">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e5c6c-2110">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2110">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2111">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2112">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2112">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-2113">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2113">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-2114">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2114">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e5c6c-2115">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2115">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e5c6c-2116">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2116">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e5c6c-2117">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2117">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e5c6c-2118">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2118">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e5c6c-2119">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2119">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e5c6c-2120">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2120">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e5c6c-2121">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2121">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e5c6c-2122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2122">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e5c6c-2123">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2123">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e5c6c-2124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2124">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e5c6c-2125">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2125">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e5c6c-2126">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2126">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e5c6c-2127">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2127">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e5c6c-2128">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2128">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e5c6c-2129">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2129">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e5c6c-2130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2130">Az.SignalR</span></span>
* <span data-ttu-id="e5c6c-2131">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2131">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2132">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2133">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2133">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e5c6c-2134">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2134">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e5c6c-2135">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2135">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e5c6c-2136">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2136">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e5c6c-2137">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2137">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2138">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2139">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2139">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e5c6c-2140">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2140">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e5c6c-2141">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2141">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e5c6c-2142">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2142">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e5c6c-2143">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2143">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e5c6c-2144">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2144">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e5c6c-2145">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2145">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e5c6c-2146">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2146">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e5c6c-2147">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2147">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e5c6c-2148">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2148">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e5c6c-2149">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2149">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2150">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2150">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2151">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2151">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e5c6c-2152">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2152">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e5c6c-2153">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2153">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e5c6c-2154">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2154">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e5c6c-2155">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2155">General</span></span>
* <span data-ttu-id="e5c6c-2156">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2156">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2157">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2157">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2158">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2158">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-2159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2159">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-2160">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2160">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e5c6c-2161">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2161">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-2162">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2162">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-2163">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2163">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e5c6c-2164">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2164">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e5c6c-2165">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2165">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e5c6c-2166">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2166">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e5c6c-2167">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2167">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-2168">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2168">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-2169">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2169">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-2170">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2170">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-2171">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2171">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2172">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2172">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2173">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2173">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e5c6c-2174">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2174">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e5c6c-2175">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2175">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e5c6c-2176">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2176">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e5c6c-2177">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2177">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e5c6c-2178">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2178">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e5c6c-2179">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2179">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e5c6c-2180">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2180">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2181">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2181">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2182">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2182">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e5c6c-2183">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2183">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e5c6c-2184">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2184">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e5c6c-2185">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2185">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-2186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2186">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-2187">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2187">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-2188">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2188">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-2189">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2189">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e5c6c-2190">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2190">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e5c6c-2191">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2191">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e5c6c-2192">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2192">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e5c6c-2193">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2193">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e5c6c-2194">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2194">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2195">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2195">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-2196">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2196">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2197">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2198">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2198">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e5c6c-2199">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2199">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e5c6c-2200">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2200">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e5c6c-2201">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2201">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e5c6c-2202">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2202">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="e5c6c-2203">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2203">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e5c6c-2204">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2204">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2205">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2205">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2206">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2206">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e5c6c-2207">新增了範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2207">Added example</span></span>
    - <span data-ttu-id="e5c6c-2208">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2208">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e5c6c-2209">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2209">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e5c6c-2210">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2210">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2211">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2211">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2212">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2212">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2213">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2214">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2214">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e5c6c-2215">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2215">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e5c6c-2216">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2216">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e5c6c-2217">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2217">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-2218">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2218">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-2219">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2219">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e5c6c-2220">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2220">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e5c6c-2221">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2221">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-2222">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2222">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-2223">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2223">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e5c6c-2224">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2224">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e5c6c-2225">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2225">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e5c6c-2226">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2226">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e5c6c-2227">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2227">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e5c6c-2228">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2228">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2229">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2229">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2230">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2230">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2231">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2231">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2232">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2232">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e5c6c-2233">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2233">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e5c6c-2234">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2234">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e5c6c-2235">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2235">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e5c6c-2236">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2236">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e5c6c-2237">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2237">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2238">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2238">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2239">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2239">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e5c6c-2240">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2240">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2241">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2242">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2242">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e5c6c-2243">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2243">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e5c6c-2244">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2244">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2245">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2245">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2246">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2246">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-2247">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2247">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-2248">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2248">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2249">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2250">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2250">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e5c6c-2251">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2251">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e5c6c-2252">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2252">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e5c6c-2253">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2253">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2254">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2254">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2255">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2255">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e5c6c-2256">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2256">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2257">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-2258">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2258">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e5c6c-2259">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2259">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-2260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2260">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-2261">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2261">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e5c6c-2262">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2262">Az.LogicApp</span></span>
* <span data-ttu-id="e5c6c-2263">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2263">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e5c6c-2264">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2264">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e5c6c-2265">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2265">Az.ManagedServices</span></span>
* <span data-ttu-id="e5c6c-2266">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2266">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2267">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2268">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2268">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e5c6c-2269">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2269">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2270">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2270">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e5c6c-2271">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2271">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e5c6c-2272">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2272">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-2273">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2273">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-2274">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2274">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-2275">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2275">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e5c6c-2276">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2276">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e5c6c-2277">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2277">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e5c6c-2278">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2278">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e5c6c-2279">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2279">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e5c6c-2280">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2280">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e5c6c-2281">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2281">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e5c6c-2282">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2282">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e5c6c-2283">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2283">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e5c6c-2284">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2284">Updated cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2285">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2285">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e5c6c-2286">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2286">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e5c6c-2287">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2287">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e5c6c-2288">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2288">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e5c6c-2289">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2289">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e5c6c-2290">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2290">Updated cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-2291">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2291">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e5c6c-2292">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2292">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e5c6c-2293">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2293">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e5c6c-2294">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2294">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e5c6c-2295">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2295">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e5c6c-2296">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2296">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2297">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2297">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2298">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2298">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="e5c6c-2299">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2299">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2300">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2300">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2301">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2301">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e5c6c-2302">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2302">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e5c6c-2303">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2303">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e5c6c-2304">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2304">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e5c6c-2305">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2305">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e5c6c-2306">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2306">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e5c6c-2307">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2307">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e5c6c-2308">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2308">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e5c6c-2309">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2309">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e5c6c-2310">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2310">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2311">Az.Resources</span></span>
- <span data-ttu-id="e5c6c-2312">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2312">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e5c6c-2313">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2313">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-2314">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2314">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-2315">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2315">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e5c6c-2316">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2316">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2317">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2318">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2318">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e5c6c-2319">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2319">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e5c6c-2320">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2320">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2321">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2322">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2322">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2323">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-2324">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2324">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e5c6c-2325">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2325">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2326">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2327">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2327">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e5c6c-2328">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2328">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e5c6c-2329">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2329">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e5c6c-2330">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2330">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2331">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2332">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2332">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e5c6c-2333">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2333">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e5c6c-2334">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2334">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e5c6c-2335">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2335">Az.Advisor</span></span>
* <span data-ttu-id="e5c6c-2336">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2336">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e5c6c-2337">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2337">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-2338">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2338">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-2339">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2339">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e5c6c-2340">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2340">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e5c6c-2341">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2341">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e5c6c-2342">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2342">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e5c6c-2343">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2343">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e5c6c-2344">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2344">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e5c6c-2345">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2345">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2346">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2346">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2347">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2347">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2348">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2349">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2349">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2350">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2350">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2351">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2351">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e5c6c-2352">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2352">Az.EventGrid</span></span>
* <span data-ttu-id="e5c6c-2353">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2353">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-2354">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2354">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-2355">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2355">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2356">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2357">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2357">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e5c6c-2358">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2358">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-2359">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2359">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-2360">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2360">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e5c6c-2361">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2361">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2362">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2362">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2363">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2363">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2364">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2365">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2365">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2366">Az.Resources</span></span>
    - <span data-ttu-id="e5c6c-2367">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2367">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e5c6c-2368">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2368">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e5c6c-2369">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2369">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e5c6c-2370">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2370">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-2372">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2372">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2373">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2374">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2374">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e5c6c-2375">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2375">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e5c6c-2376">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2376">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e5c6c-2377">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2377">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e5c6c-2378">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2378">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e5c6c-2379">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2379">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e5c6c-2380">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2380">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e5c6c-2381">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2381">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e5c6c-2382">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2382">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2383">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2384">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2384">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e5c6c-2385">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2385">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e5c6c-2386">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2386">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e5c6c-2387">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2387">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e5c6c-2388">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2388">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e5c6c-2389">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2389">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e5c6c-2390">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2390">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e5c6c-2391">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2391">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e5c6c-2392">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2392">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e5c6c-2393">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2393">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e5c6c-2394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2394">Az.StorageSync</span></span>
* <span data-ttu-id="e5c6c-2395">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2395">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e5c6c-2396">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2396">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2397">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2398">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2398">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e5c6c-2399">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2399">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e5c6c-2400">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2400">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e5c6c-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e5c6c-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2403">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2403">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2404">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2404">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e5c6c-2405">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2405">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e5c6c-2406">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2406">Az.Dns</span></span>
* <span data-ttu-id="e5c6c-2407">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2407">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e5c6c-2408">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2408">Az.EventGrid</span></span>
* <span data-ttu-id="e5c6c-2409">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2409">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e5c6c-2410">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2410">New cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-2411">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2411">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e5c6c-2412">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2412">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e5c6c-2413">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2413">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e5c6c-2414">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2414">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e5c6c-2415">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2415">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e5c6c-2416">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2416">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e5c6c-2417">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2417">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e5c6c-2418">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2418">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e5c6c-2419">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2419">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e5c6c-2420">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2420">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e5c6c-2421">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2421">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e5c6c-2422">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2422">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e5c6c-2423">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2423">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e5c6c-2424">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2424">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="e5c6c-2425">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2425">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e5c6c-2426">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2426">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e5c6c-2427">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2427">Updated cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e5c6c-2429">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2429">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e5c6c-2430">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2430">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e5c6c-2431">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2431">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e5c6c-2432">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2432">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e5c6c-2433">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2433">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e5c6c-2434">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2434">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e5c6c-2435">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2435">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e5c6c-2436">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2436">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="e5c6c-2437">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2437">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e5c6c-2438">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2438">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e5c6c-2439">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2439">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e5c6c-2440">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2440">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e5c6c-2441">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2441">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-2442">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2442">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-2443">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2443">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e5c6c-2444">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2444">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e5c6c-2445">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2445">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e5c6c-2446">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2446">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2447">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2447">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2448">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2448">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e5c6c-2449">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2449">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e5c6c-2451">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2451">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e5c6c-2452">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2452">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2453">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2453">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e5c6c-2454">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2454">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e5c6c-2455">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2455">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2456">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2456">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e5c6c-2457">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2457">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e5c6c-2458">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2458">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e5c6c-2459">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2459">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e5c6c-2460">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2460">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e5c6c-2461">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2461">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e5c6c-2462">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2462">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2463">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2463">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e5c6c-2464">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2464">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e5c6c-2465">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2465">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e5c6c-2466">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2466">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e5c6c-2467">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2467">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e5c6c-2468">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2468">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e5c6c-2469">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2469">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e5c6c-2470">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2470">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e5c6c-2471">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2471">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e5c6c-2472">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2472">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e5c6c-2473">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2473">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e5c6c-2474">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2474">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e5c6c-2475">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2475">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e5c6c-2476">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2476">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e5c6c-2477">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2477">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e5c6c-2478">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2478">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e5c6c-2479">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2479">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e5c6c-2480">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2480">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e5c6c-2481">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2481">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-2482">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2482">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e5c6c-2483">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2483">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e5c6c-2484">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2484">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e5c6c-2485">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2485">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="e5c6c-2486">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2486">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="e5c6c-2487">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2487">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e5c6c-2488">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2488">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e5c6c-2489">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2489">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2490">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2490">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2491">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2491">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2492">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2493">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2493">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e5c6c-2494">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2494">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e5c6c-2495">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2495">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e5c6c-2496">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2496">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-2497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2497">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-2498">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2498">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2499">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2499">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2500">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2500">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e5c6c-2501">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2501">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e5c6c-2502">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2502">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e5c6c-2503">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2503">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e5c6c-2504">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2504">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e5c6c-2505">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2505">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e5c6c-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e5c6c-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2508">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2508">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2509">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2509">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e5c6c-2510">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2510">New-AzStorageAccount</span></span>
* <span data-ttu-id="e5c6c-2511">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2511">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e5c6c-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2513">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2513">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2514">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2514">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e5c6c-2515">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2515">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e5c6c-2516">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2516">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e5c6c-2517">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2517">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-2518">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2518">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2519">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2520">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2520">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e5c6c-2521">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2521">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-2522">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2522">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-2523">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2523">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e5c6c-2524">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2524">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2525">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2526">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2526">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e5c6c-2527">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2527">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-2528">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2528">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-2529">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2529">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2530">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2531">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2531">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-2532">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2532">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-2533">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2533">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-2534">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2534">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-2535">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2535">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e5c6c-2536">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2536">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2537">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2538">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2538">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e5c6c-2539">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2539">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e5c6c-2540">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2540">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e5c6c-2541">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2541">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2542">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2543">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2543">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e5c6c-2544">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2544">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-2545">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2545">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-2546">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2546">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e5c6c-2547">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2547">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e5c6c-2548">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2548">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e5c6c-2549">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2549">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e5c6c-2550">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2550">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e5c6c-2551">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2551">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e5c6c-2552">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2552">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e5c6c-2553">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2553">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e5c6c-2554">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2554">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e5c6c-2555">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2555">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e5c6c-2556">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2556">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e5c6c-2557">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2557">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e5c6c-2558">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2558">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e5c6c-2559">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2559">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e5c6c-2560">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2560">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e5c6c-2561">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2561">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e5c6c-2562">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2562">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e5c6c-2563">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2563">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e5c6c-2564">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2564">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="e5c6c-2565">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2565">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e5c6c-2566">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2566">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e5c6c-2567">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2567">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e5c6c-2568">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2568">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e5c6c-2569">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2569">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="e5c6c-2570">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2570">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e5c6c-2571">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2571">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e5c6c-2572">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2572">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e5c6c-2573">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2573">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e5c6c-2574">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2574">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e5c6c-2575">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2575">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e5c6c-2576">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2576">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="e5c6c-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e5c6c-2578">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2578">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e5c6c-2579">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2579">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e5c6c-2580">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2580">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e5c6c-2581">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2581">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e5c6c-2582">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2582">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e5c6c-2583">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2583">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e5c6c-2584">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2584">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e5c6c-2585">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2585">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e5c6c-2586">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2586">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e5c6c-2587">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2587">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e5c6c-2588">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2588">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e5c6c-2589">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2589">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e5c6c-2590">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2590">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e5c6c-2591">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2591">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e5c6c-2592">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2592">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e5c6c-2593">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2593">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e5c6c-2594">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2594">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e5c6c-2595">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2595">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e5c6c-2596">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2596">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e5c6c-2597">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2597">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e5c6c-2598">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2598">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e5c6c-2599">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2599">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e5c6c-2600">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2600">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e5c6c-2601">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2601">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e5c6c-2602">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2602">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e5c6c-2603">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2603">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e5c6c-2604">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2604">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e5c6c-2605">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2605">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e5c6c-2606">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2606">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e5c6c-2607">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2607">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e5c6c-2608">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2608">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e5c6c-2609">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2609">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e5c6c-2610">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2610">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e5c6c-2611">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2611">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e5c6c-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e5c6c-2613">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2613">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e5c6c-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e5c6c-2615">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2615">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e5c6c-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e5c6c-2617">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2617">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e5c6c-2618">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2618">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e5c6c-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e5c6c-2620">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2620">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="e5c6c-2621">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2621">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e5c6c-2622">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2622">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2623">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2623">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2624">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2624">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e5c6c-2625">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2625">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e5c6c-2626">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2626">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e5c6c-2627">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2627">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e5c6c-2628">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2628">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e5c6c-2629">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2629">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e5c6c-2630">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2630">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2631">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2631">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2632">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2632">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e5c6c-2633">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2633">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-2634">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2634">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-2635">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2635">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2636">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-2637">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2637">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2638">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2638">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2639">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2639">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e5c6c-2640">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2640">Updated cmdlet:</span></span>
        - <span data-ttu-id="e5c6c-2641">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2641">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e5c6c-2642">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2642">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2643">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2644">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2644">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2645">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2646">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2646">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e5c6c-2647">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2647">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2648">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2648">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2649">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2649">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-2650">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2650">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-2651">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2651">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e5c6c-2652">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2652">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2653">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2654">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2654">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e5c6c-2655">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2655">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e5c6c-2656">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2656">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e5c6c-2657">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2657">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e5c6c-2658">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2658">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e5c6c-2659">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2659">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="e5c6c-2660">重大變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2660">Breaking changes</span></span>
    - <span data-ttu-id="e5c6c-2661">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2661">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e5c6c-2662">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2662">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e5c6c-2663">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2663">Az.DeploymentManager</span></span>
* <span data-ttu-id="e5c6c-2664">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2664">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e5c6c-2665">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2665">Az.Dns</span></span>
* <span data-ttu-id="e5c6c-2666">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2666">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e5c6c-2667">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2667">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e5c6c-2668">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2668">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-2669">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2669">Az.FrontDoor</span></span>
* <span data-ttu-id="e5c6c-2670">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2670">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e5c6c-2671">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2671">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-2672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2672">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-2673">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2673">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e5c6c-2674">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2674">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e5c6c-2675">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2675">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e5c6c-2676">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2676">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e5c6c-2677">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2677">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e5c6c-2678">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2678">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e5c6c-2679">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2679">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2680">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-2681">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2681">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="e5c6c-2682">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2682">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e5c6c-2683">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2683">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e5c6c-2684">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2684">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e5c6c-2685">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2685">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e5c6c-2686">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2686">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e5c6c-2687">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2687">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e5c6c-2688">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2688">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e5c6c-2689">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2689">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e5c6c-2690">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2690">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e5c6c-2691">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2691">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e5c6c-2692">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2692">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e5c6c-2693">[更多](/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2693">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e5c6c-2694">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2694">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2695">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2695">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2696">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2696">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e5c6c-2697">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2697">New cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2698">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2698">New-AzNatGateway</span></span>
        - <span data-ttu-id="e5c6c-2699">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2699">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e5c6c-2700">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2700">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e5c6c-2701">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2701">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e5c6c-2702">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2702">Updated cmdlets</span></span>
        - <span data-ttu-id="e5c6c-2703">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2703">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e5c6c-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e5c6c-2705">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2705">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e5c6c-2706">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2706">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e5c6c-2707">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2707">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-2708">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2708">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-2709">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2709">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e5c6c-2710">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2710">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e5c6c-2711">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2711">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2712">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2713">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2713">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e5c6c-2714">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2714">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e5c6c-2715">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2715">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e5c6c-2716">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2716">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e5c6c-2717">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2717">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e5c6c-2718">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2718">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e5c6c-2719">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2719">Az.Relay</span></span>
* <span data-ttu-id="e5c6c-2720">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2720">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-2721">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2721">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-2722">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2722">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2723">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2724">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2724">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e5c6c-2725">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2725">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e5c6c-2726">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2726">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e5c6c-2727">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2727">New-AzStorageAccount</span></span>
* <span data-ttu-id="e5c6c-2728">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2728">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e5c6c-2729">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2729">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e5c6c-2730">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2730">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e5c6c-2731">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2731">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2732">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2732">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2733">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2733">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e5c6c-2734">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2734">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e5c6c-2735">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2735">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-2736">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2736">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-2737">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2737">General availability of `Az` module</span></span>
* <span data-ttu-id="e5c6c-2738">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2738">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e5c6c-2739">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2739">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e5c6c-2740">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2740">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e5c6c-2741">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2741">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e5c6c-2742">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2742">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2743">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2743">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2744">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2744">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2745">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2745">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e5c6c-2746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2746">Az.Batch</span></span>
* <span data-ttu-id="e5c6c-2747">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2747">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2748">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-2749">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2749">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-2750">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2750">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-2751">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2751">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2752">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2753">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2753">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e5c6c-2754">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2754">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2755">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2755">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2756">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2756">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2757">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2757">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-2758">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2758">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-2759">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2759">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e5c6c-2760">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2760">Az.EventGrid</span></span>
* <span data-ttu-id="e5c6c-2761">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2761">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-2762">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2762">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-2763">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2763">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e5c6c-2764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2764">Az.HDInsight</span></span>
* <span data-ttu-id="e5c6c-2765">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2765">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-2766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2766">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-2767">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2767">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-2768">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2768">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-2769">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2769">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2770">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2770">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e5c6c-2771">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2771">Az.MachineLearning</span></span>
* <span data-ttu-id="e5c6c-2772">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2772">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e5c6c-2773">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2773">Az.Media</span></span>
* <span data-ttu-id="e5c6c-2774">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2774">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2775">Az.Monitor</span></span>
  * <span data-ttu-id="e5c6c-2776">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2776">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e5c6c-2777">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2777">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e5c6c-2778">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2778">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e5c6c-2779">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2779">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e5c6c-2780">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2780">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e5c6c-2781">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2781">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e5c6c-2782">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2782">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2783">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2784">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2784">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2785">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2785">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e5c6c-2786">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2786">Az.NotificationHubs</span></span>
* <span data-ttu-id="e5c6c-2787">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2787">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2788">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2788">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2789">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2789">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e5c6c-2790">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2790">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e5c6c-2791">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2791">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2792">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2793">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2793">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2794">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2794">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e5c6c-2795">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2795">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e5c6c-2796">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2796">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e5c6c-2797">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2797">Az.RedisCache</span></span>
* <span data-ttu-id="e5c6c-2798">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2798">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2799">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2800">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2800">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2801">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2801">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2802">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2802">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e5c6c-2803">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2803">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2804">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2804">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e5c6c-2805">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2805">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e5c6c-2806">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2806">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e5c6c-2807">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2807">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e5c6c-2808">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2808">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2809">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2810">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2810">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e5c6c-2811">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2811">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e5c6c-2812">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2812">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e5c6c-2813">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2813">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e5c6c-2814">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2814">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-2815">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2815">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-2816">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2816">General availability of `Az` module</span></span>
* <span data-ttu-id="e5c6c-2817">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2817">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e5c6c-2818">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2818">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e5c6c-2819">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2819">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e5c6c-2820">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2820">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e5c6c-2821">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2821">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2822">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2822">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2823">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2823">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2824">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2824">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-2825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2825">Az.AnalysisServices</span></span>
* <span data-ttu-id="e5c6c-2826">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2826">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e5c6c-2827">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2827">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2828">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2828">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2829">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2829">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e5c6c-2830">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2830">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e5c6c-2831">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2831">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2832">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2833">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2833">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e5c6c-2834">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2834">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e5c6c-2835">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2835">Az.ContainerInstance</span></span>
* <span data-ttu-id="e5c6c-2836">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2836">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2837">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2837">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2838">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2838">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e5c6c-2839">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2839">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2840">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2841">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2841">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e5c6c-2842">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2842">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e5c6c-2843">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2843">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e5c6c-2844">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2844">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e5c6c-2845">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2845">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e5c6c-2846">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2846">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2847">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2848">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2848">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2849">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2850">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2850">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e5c6c-2851">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2851">New-AzStorageContext</span></span>
* <span data-ttu-id="e5c6c-2852">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2852">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e5c6c-2853">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2853">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e5c6c-2854">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2854">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e5c6c-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e5c6c-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e5c6c-2857">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2857">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e5c6c-2858">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2858">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e5c6c-2859">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2859">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e5c6c-2860">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2860">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e5c6c-2861">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2861">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e5c6c-2862">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2862">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e5c6c-2863">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2863">Highlights since the last major release</span></span>
* <span data-ttu-id="e5c6c-2864">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2864">General availability of `Az` module</span></span>
* <span data-ttu-id="e5c6c-2865">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2865">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e5c6c-2866">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2866">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e5c6c-2867">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2867">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e5c6c-2868">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2868">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e5c6c-2869">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2869">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2870">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2870">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2871">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2872">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2872">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e5c6c-2873">動態分組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2873">Dynamic grouping</span></span>
    * <span data-ttu-id="e5c6c-2874">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2874">Pre-Post script</span></span>
    * <span data-ttu-id="e5c6c-2875">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2875">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2876">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2877">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2877">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e5c6c-2878">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2878">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-2879">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2879">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-2880">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2880">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2881">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2882">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2882">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e5c6c-2883">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2883">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2884">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2885">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2885">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e5c6c-2886">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2886">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2887">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2887">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2888">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2888">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e5c6c-2889">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2889">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2890">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2890">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2891">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2891">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2892">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2893">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2893">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e5c6c-2894">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2894">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e5c6c-2895">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2895">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e5c6c-2896">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2896">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e5c6c-2897">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2897">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e5c6c-2898">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2898">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e5c6c-2899">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2899">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2900">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2900">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2901">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2901">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="e5c6c-2902">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2902">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2903">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2904">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2904">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e5c6c-2905">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2905">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2906">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2907">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2907">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e5c6c-2908">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2908">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e5c6c-2909">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2909">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-2910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2910">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-2911">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2911">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2912">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2913">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2913">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-2914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2914">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-2915">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2915">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e5c6c-2916">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2916">Az.LogicApp</span></span>
* <span data-ttu-id="e5c6c-2917">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2917">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2918">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2919">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2919">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2920">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-2921">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2921">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e5c6c-2922">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2922">SDK Update</span></span>
* <span data-ttu-id="e5c6c-2923">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2923">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e5c6c-2924">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2924">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2925">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2926">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2926">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e5c6c-2927">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2927">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e5c6c-2928">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2928">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e5c6c-2929">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2929">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e5c6c-2930">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2930">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e5c6c-2931">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2931">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2932">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2933">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2933">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e5c6c-2934">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2934">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-2935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2935">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-2936">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2936">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e5c6c-2937">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2937">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-2938">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2938">Az.AnalysisServices</span></span>
* <span data-ttu-id="e5c6c-2939">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2939">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2940">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-2941">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2941">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e5c6c-2942">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2942">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e5c6c-2943">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2943">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-2944">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2944">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-2945">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2945">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2946">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2946">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2947">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2947">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e5c6c-2948">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2948">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e5c6c-2949">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2949">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e5c6c-2950">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2950">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-2951">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2951">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-2952">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2952">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e5c6c-2953">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2953">Az.EventHub</span></span>
* <span data-ttu-id="e5c6c-2954">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2954">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-2955">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2955">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-2956">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2956">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e5c6c-2957">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2957">Az.LogicApp</span></span>
* <span data-ttu-id="e5c6c-2958">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2958">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e5c6c-2959">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2959">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e5c6c-2960">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2960">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e5c6c-2961">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2961">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e5c6c-2962">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2962">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e5c6c-2963">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2963">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e5c6c-2964">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2964">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e5c6c-2965">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2965">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e5c6c-2966">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2966">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e5c6c-2967">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2967">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e5c6c-2968">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2968">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e5c6c-2969">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2969">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e5c6c-2970">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2970">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e5c6c-2971">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2971">Az.Monitor</span></span>
* <span data-ttu-id="e5c6c-2972">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2972">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2973">Az.Network</span></span>
* <span data-ttu-id="e5c6c-2974">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2974">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-2975">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2975">Az.OperationalInsights</span></span>
* <span data-ttu-id="e5c6c-2976">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2976">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e5c6c-2977">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2977">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="e5c6c-2978">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2978">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-2979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2979">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-2980">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2980">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e5c6c-2981">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2981">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e5c6c-2982">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2982">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e5c6c-2983">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2983">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-2984">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2984">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-2985">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2985">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e5c6c-2986">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2986">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-2987">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2987">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-2988">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2988">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e5c6c-2989">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2989">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-2990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2990">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-2991">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2991">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-2992">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2992">Az.AnalysisServices</span></span>
<span data-ttu-id="e5c6c-2993">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2993">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2994">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-2995">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2995">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e5c6c-2996">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2996">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e5c6c-2997">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2997">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-2998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2998">Az.RecoveryServices</span></span>
<span data-ttu-id="e5c6c-2999">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-2999">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3000">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3001">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3001">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="e5c6c-3002">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3002">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e5c6c-3003">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3003">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="e5c6c-3004">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3004">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-3005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3005">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-3006">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3006">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e5c6c-3007">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3007">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e5c6c-3008">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3008">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e5c6c-3009">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3009">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-3010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3010">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-3011">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3011">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e5c6c-3012">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3012">Az.AnalysisServices</span></span>
* <span data-ttu-id="e5c6c-3013">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3013">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-3014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3014">Az.RecoveryServices</span></span>
* <span data-ttu-id="e5c6c-3015">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3015">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e5c6c-3016">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3016">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-3017">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3017">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-3018">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3018">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e5c6c-3019">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3019">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e5c6c-3020">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3020">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e5c6c-3021">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3021">Az.Aks</span></span>
* <span data-ttu-id="e5c6c-3022">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3022">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e5c6c-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3023">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-3024">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3024">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e5c6c-3025">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3025">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e5c6c-3026">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3026">Az.Cdn</span></span>
* <span data-ttu-id="e5c6c-3027">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3027">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3028">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3029">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3029">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e5c6c-3030">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3030">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e5c6c-3031">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3031">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e5c6c-3032">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3032">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e5c6c-3033">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3033">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e5c6c-3034">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3034">Az.DataFactory</span></span>
* <span data-ttu-id="e5c6c-3035">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3035">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3036">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3036">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-3037">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3037">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e5c6c-3038">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3038">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e5c6c-3039">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3039">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-3040">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3040">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-3041">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3041">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-3042">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3042">Az.KeyVault</span></span>
* <span data-ttu-id="e5c6c-3043">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3043">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3044">Az.Network</span></span>
* <span data-ttu-id="e5c6c-3045">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3045">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3046">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3046">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3047">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3047">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e5c6c-3048">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3048">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e5c6c-3049">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3049">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e5c6c-3050">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3050">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e5c6c-3051">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3051">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e5c6c-3052">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3052">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e5c6c-3053">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3053">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-3054">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3054">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-3055">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3055">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e5c6c-3056">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3056">Fix some error messages.</span></span>
* <span data-ttu-id="e5c6c-3057">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3057">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e5c6c-3058">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3058">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e5c6c-3059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3059">Az.SignalR</span></span>
* <span data-ttu-id="e5c6c-3060">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3060">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-3061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3061">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-3062">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3062">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e5c6c-3063">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3063">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e5c6c-3064">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3064">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e5c6c-3065">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3065">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-3066">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3066">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-3067">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3067">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e5c6c-3068">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3068">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e5c6c-3069">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3069">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e5c6c-3070">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3070">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e5c6c-3071">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3071">Az.TrafficManager</span></span>
* <span data-ttu-id="e5c6c-3072">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3072">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-3073">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3073">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-3074">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3074">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e5c6c-3075">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3075">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e5c6c-3076">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3076">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e5c6c-3077">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3077">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e5c6c-3078">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3078">Az.Accounts</span></span>
* <span data-ttu-id="e5c6c-3079">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3079">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-3080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3080">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3081">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3081">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e5c6c-3082">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3082">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e5c6c-3083">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3083">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3084">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-3085">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3085">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e5c6c-3086">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3086">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e5c6c-3087">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3087">Az.EventGrid</span></span>
* <span data-ttu-id="e5c6c-3088">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3088">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e5c6c-3089">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3089">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e5c6c-3090">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3090">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e5c6c-3091">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3091">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e5c6c-3092">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3092">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e5c6c-3093">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3093">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e5c6c-3094">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3094">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e5c6c-3095">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3095">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e5c6c-3096">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3096">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e5c6c-3097">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3097">Dead letter endpoint.</span></span>
* <span data-ttu-id="e5c6c-3098">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3098">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e5c6c-3099">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3099">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e5c6c-3100">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3100">Az.IotHub</span></span>
* <span data-ttu-id="e5c6c-3101">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3101">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e5c6c-3102">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3102">Az.LogicApp</span></span>
* <span data-ttu-id="e5c6c-3103">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3103">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3104">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3104">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3105">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3105">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e5c6c-3106">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3106">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e5c6c-3107">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3107">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e5c6c-3108">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3108">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e5c6c-3109">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3109">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e5c6c-3110">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3110">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e5c6c-3111">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3111">Az.SignalR</span></span>
* <span data-ttu-id="e5c6c-3112">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3112">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-3113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3113">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-3114">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3114">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e5c6c-3115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3115">Az.Storage</span></span>
* <span data-ttu-id="e5c6c-3116">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3116">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e5c6c-3117">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3117">New-AzStorageContext</span></span>
* <span data-ttu-id="e5c6c-3118">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3118">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e5c6c-3119">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3119">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-3120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3120">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-3121">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3121">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e5c6c-3122">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3122">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e5c6c-3123">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3123">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e5c6c-3124">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3124">General</span></span>

- <span data-ttu-id="e5c6c-3125">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3125">General Availability of Az Module</span></span>
- <span data-ttu-id="e5c6c-3126">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3126">Online help for each module</span></span>
- <span data-ttu-id="e5c6c-3127">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3127">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e5c6c-3128">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3128">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e5c6c-3129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3129">Az.Accounts</span></span>
- <span data-ttu-id="e5c6c-3130">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3130">Changed from Az.Profile</span></span>
- <span data-ttu-id="e5c6c-3131">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3131">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-3132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3132">Az.ApiManagement</span></span>
- <span data-ttu-id="e5c6c-3133">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3133">Fixes for #7002</span></span>
- <span data-ttu-id="e5c6c-3134">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e5c6c-3135">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3135">Az.Batch</span></span>
- <span data-ttu-id="e5c6c-3136">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3136">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e5c6c-3137">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3137">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e5c6c-3138">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3138">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e5c6c-3139">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3139">Az.Billing</span></span>
- <span data-ttu-id="e5c6c-3140">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3140">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e5c6c-3141">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3141">Az.CognitivServices</span></span>
- <span data-ttu-id="e5c6c-3142">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3142">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e5c6c-3143">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3143">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e5c6c-3144">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3144">Az.ContainerInstance</span></span>
- <span data-ttu-id="e5c6c-3145">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3145">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e5c6c-3146">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3146">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e5c6c-3147">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3148">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3148">Az.DataLakeStore</span></span>
- <span data-ttu-id="e5c6c-3149">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e5c6c-3150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3150">Az.Monitor</span></span>
- <span data-ttu-id="e5c6c-3151">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3151">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e5c6c-3152">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3152">Az.KeyVault</span></span>
- <span data-ttu-id="e5c6c-3153">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3153">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e5c6c-3154">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3154">Az.MachineLearning</span></span>
- <span data-ttu-id="e5c6c-3155">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3155">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e5c6c-3156">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3156">Az.Media</span></span>
- <span data-ttu-id="e5c6c-3157">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3157">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3158">Az.Network</span></span>
<span data-ttu-id="e5c6c-3159">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3159">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e5c6c-3160">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3160">New cmdlets added:</span></span>
        - <span data-ttu-id="e5c6c-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3166">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3166">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e5c6c-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e5c6c-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e5c6c-3169">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3169">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e5c6c-3170">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3170">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e5c6c-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e5c6c-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e5c6c-3173">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3173">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e5c6c-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e5c6c-3175">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3175">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e5c6c-3176">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3176">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e5c6c-3177">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3177">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e5c6c-3178">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3178">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e5c6c-3179">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3179">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e5c6c-3180">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3180">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e5c6c-3181">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3181">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e5c6c-3182">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3182">Az.OperationalInsights</span></span>
- <span data-ttu-id="e5c6c-3183">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3183">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e5c6c-3184">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3184">Az.Profile</span></span>
- <span data-ttu-id="e5c6c-3185">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3185">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-3186">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3186">Az.RecoveryServices</span></span>
- <span data-ttu-id="e5c6c-3187">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3187">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e5c6c-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3188">Az.Resources</span></span>
- <span data-ttu-id="e5c6c-3189">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3189">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-3190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3190">Az.ServiceFabric</span></span>
- <span data-ttu-id="e5c6c-3191">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3191">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e5c6c-3192">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3192">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e5c6c-3193">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3193">Az.SIgnalR</span></span>
- <span data-ttu-id="e5c6c-3194">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3194">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e5c6c-3195">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3195">Az.Sql</span></span>
- <span data-ttu-id="e5c6c-3196">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3196">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e5c6c-3197">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3197">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e5c6c-3198">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3198">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e5c6c-3199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3199">Az.Storage</span></span>
- <span data-ttu-id="e5c6c-3200">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3200">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e5c6c-3201">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3201">Az.Websites</span></span>
- <span data-ttu-id="e5c6c-3202">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3202">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e5c6c-3203">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3203">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e5c6c-3204">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3204">General</span></span>

* <span data-ttu-id="e5c6c-3205">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3205">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e5c6c-3206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3206">Az.Compute</span></span>

* <span data-ttu-id="e5c6c-3207">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3207">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3208">Az.DataLakeStore</span></span>

* <span data-ttu-id="e5c6c-3209">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3209">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e5c6c-3210">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3210">Az.FrontDoor</span></span>

* <span data-ttu-id="e5c6c-3211">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3211">Fixed some broken links</span></span>
    - <span data-ttu-id="e5c6c-3212">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3212">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e5c6c-3213">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3213">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e5c6c-3214">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3214">Az.RecoveryServices</span></span>

* <span data-ttu-id="e5c6c-3215">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3215">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e5c6c-3216">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3216">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e5c6c-3217">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3217">Az.Resources</span></span>

* <span data-ttu-id="e5c6c-3218">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3218">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e5c6c-3219">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3219">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e5c6c-3220">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3220">Az.Sql</span></span>

* <span data-ttu-id="e5c6c-3221">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3221">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e5c6c-3222">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3222">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e5c6c-3223">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3223">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e5c6c-3224">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3224">Az.Storage</span></span>

* <span data-ttu-id="e5c6c-3225">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3225">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e5c6c-3226">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3226">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e5c6c-3227">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3227">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e5c6c-3228">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3228">Support Static Website configuration</span></span>
    - <span data-ttu-id="e5c6c-3229">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3229">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e5c6c-3230">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3230">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e5c6c-3231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3231">Az.Websites</span></span>

* <span data-ttu-id="e5c6c-3232">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3232">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="e5c6c-3233">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3233">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e5c6c-3234">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3234">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e5c6c-3235">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3235">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e5c6c-3236">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3236">Az.ApiManagement</span></span>
* <span data-ttu-id="e5c6c-3237">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3237">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e5c6c-3238">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3238">Az.Automation</span></span>
* <span data-ttu-id="e5c6c-3239">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3239">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e5c6c-3240">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3240">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e5c6c-3241">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3241">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e5c6c-3242">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3242">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e5c6c-3243">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3243">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e5c6c-3244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3244">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3245">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3245">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e5c6c-3246">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3246">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e5c6c-3247">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3247">Az.ContainerInstance</span></span>
* <span data-ttu-id="e5c6c-3248">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3248">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e5c6c-3249">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3249">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e5c6c-3250">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3250">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3251">Az.Network</span></span>
* <span data-ttu-id="e5c6c-3252">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3252">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e5c6c-3253">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3253">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e5c6c-3254">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3254">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="e5c6c-3255">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3255">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e5c6c-3256">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3256">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e5c6c-3257">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3257">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e5c6c-3258">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3258">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e5c6c-3259">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3259">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e5c6c-3260">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3260">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e5c6c-3261">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3261">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e5c6c-3262">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3262">Az.Relay</span></span>
* <span data-ttu-id="e5c6c-3263">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3263">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e5c6c-3264">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3264">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3265">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3265">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e5c6c-3266">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3266">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e5c6c-3267">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3267">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-3268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3268">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-3269">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3269">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e5c6c-3270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3270">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-3271">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3271">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e5c6c-3272">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3272">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e5c6c-3273">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3273">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e5c6c-3274">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3274">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e5c6c-3275">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3275">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e5c6c-3276">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3276">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e5c6c-3277">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3277">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e5c6c-3278">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3278">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e5c6c-3279">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3279">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e5c6c-3280">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3280">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e5c6c-3281">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3281">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e5c6c-3282">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3282">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e5c6c-3283">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3283">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e5c6c-3284">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3284">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e5c6c-3285">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3285">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e5c6c-3286">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3286">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e5c6c-3287">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3287">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e5c6c-3288">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3288">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e5c6c-3289">一般</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3289">General</span></span>
* <span data-ttu-id="e5c6c-3290">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3290">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e5c6c-3291">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3291">Az.Profile</span></span>
* <span data-ttu-id="e5c6c-3292">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3292">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e5c6c-3293">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3293">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e5c6c-3294">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3294">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e5c6c-3295">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3295">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e5c6c-3296">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3296">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e5c6c-3297">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3297">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e5c6c-3298">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3298">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-3299">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3299">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-3300">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3300">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-3301">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3301">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3302">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3302">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e5c6c-3303">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3303">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e5c6c-3304">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3304">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3305">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-3306">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3306">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e5c6c-3307">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3307">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e5c6c-3308">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3308">Az.Insights</span></span>
* <span data-ttu-id="e5c6c-3309">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3309">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e5c6c-3310">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3310">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e5c6c-3311">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3311">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e5c6c-3312">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3312">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3313">Az.Network</span></span>
* <span data-ttu-id="e5c6c-3314">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3314">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e5c6c-3315">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3315">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e5c6c-3316">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3316">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e5c6c-3317">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3317">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e5c6c-3318">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3318">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e5c6c-3319">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3319">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e5c6c-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e5c6c-3321">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3321">Az.PolicyInsights</span></span>
* <span data-ttu-id="e5c6c-3322">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3322">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3323">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3323">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3324">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3324">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e5c6c-3325">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3325">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e5c6c-3326">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3326">Az.ServiceBus</span></span>
* <span data-ttu-id="e5c6c-3327">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3327">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e5c6c-3328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3328">Az.ServiceFabric</span></span>
* <span data-ttu-id="e5c6c-3329">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3329">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e5c6c-3330">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3330">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e5c6c-3331">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3331">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e5c6c-3332">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3332">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e5c6c-3333">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3333">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e5c6c-3334">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3334">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e5c6c-3335">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3335">Az.Profile</span></span>
* <span data-ttu-id="e5c6c-3336">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3336">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e5c6c-3337">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3337">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-3338">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3338">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3339">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3339">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e5c6c-3340">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3340">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e5c6c-3341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3341">Az.DataLakeStore</span></span>
* <span data-ttu-id="e5c6c-3342">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3342">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e5c6c-3343">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3343">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e5c6c-3344">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3344">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e5c6c-3345">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3345">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e5c6c-3346">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3346">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3347">Az.Network</span></span>
* <span data-ttu-id="e5c6c-3348">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3348">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e5c6c-3349">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3349">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3350">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3350">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3351">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3351">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e5c6c-3352">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3352">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e5c6c-3353">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3353">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e5c6c-3354">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3354">Azure.Storage</span></span>
* <span data-ttu-id="e5c6c-3355">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3355">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e5c6c-3356">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3356">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e5c6c-3357">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3357">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e5c6c-3358">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3358">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e5c6c-3359">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3359">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e5c6c-3360">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3360">Az.CognitiveServices</span></span>
* <span data-ttu-id="e5c6c-3361">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3361">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e5c6c-3362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3362">Az.Compute</span></span>
* <span data-ttu-id="e5c6c-3363">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3363">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e5c6c-3364">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3364">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e5c6c-3365">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3365">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e5c6c-3366">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3366">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e5c6c-3367">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3367">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e5c6c-3368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3368">Az.Network</span></span>
* <span data-ttu-id="e5c6c-3369">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3369">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e5c6c-3370">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3370">new cmdlets added</span></span>
    - <span data-ttu-id="e5c6c-3371">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3371">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e5c6c-3372">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3372">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e5c6c-3373">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3373">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e5c6c-3374">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3374">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e5c6c-3375">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3375">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e5c6c-3376">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3376">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e5c6c-3377">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3377">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e5c6c-3378">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3378">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e5c6c-3379">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3379">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e5c6c-3380">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3380">Az.RedisCache</span></span>
* <span data-ttu-id="e5c6c-3381">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3381">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e5c6c-3382">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3382">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e5c6c-3383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3383">Az.Resources</span></span>
* <span data-ttu-id="e5c6c-3384">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3384">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e5c6c-3385">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3385">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e5c6c-3386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3386">Az.Sql</span></span>
* <span data-ttu-id="e5c6c-3387">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3387">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e5c6c-3388">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3388">Az.Websites</span></span>
* <span data-ttu-id="e5c6c-3389">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3389">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e5c6c-3390">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3390">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e5c6c-3391">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3391">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e5c6c-3392">初始版本</span><span class="sxs-lookup"><span data-stu-id="e5c6c-3392">Initial Release</span></span>