---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237622"
---
# <a name="release-notes"></a><span data-ttu-id="4bc7e-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="4bc7e-103">Release notes</span></span>

<span data-ttu-id="4bc7e-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="4bc7e-105">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="4bc7e-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4bc7e-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4bc7e-106">AzureRM.Profile</span></span>
* <span data-ttu-id="4bc7e-107">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="4bc7e-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="4bc7e-108">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="4bc7e-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="4bc7e-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4bc7e-109">Azure.Storage</span></span>
* <span data-ttu-id="4bc7e-110">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4bc7e-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4bc7e-111">AzureRM.Compute</span></span>
* <span data-ttu-id="4bc7e-112">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="4bc7e-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="4bc7e-113">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bc7e-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="4bc7e-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4bc7e-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="4bc7e-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4bc7e-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="4bc7e-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4bc7e-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="4bc7e-117">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="4bc7e-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="4bc7e-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4bc7e-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="4bc7e-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4bc7e-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="4bc7e-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4bc7e-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="4bc7e-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4bc7e-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="4bc7e-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="4bc7e-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="4bc7e-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4bc7e-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="4bc7e-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4bc7e-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="4bc7e-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="4bc7e-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="4bc7e-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4bc7e-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="4bc7e-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4bc7e-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="4bc7e-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4bc7e-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="4bc7e-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4bc7e-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="4bc7e-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4bc7e-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="4bc7e-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4bc7e-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="4bc7e-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bc7e-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="4bc7e-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4bc7e-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="4bc7e-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="4bc7e-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="4bc7e-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4bc7e-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="4bc7e-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4bc7e-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="4bc7e-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bc7e-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="4bc7e-138">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="4bc7e-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bc7e-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4bc7e-140">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="4bc7e-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="4bc7e-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bc7e-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="4bc7e-142">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="4bc7e-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="4bc7e-143">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="4bc7e-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="4bc7e-144">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="4bc7e-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="4bc7e-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4bc7e-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4bc7e-146">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="4bc7e-147">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4bc7e-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4bc7e-148">AzureRM.Sql</span></span>
* <span data-ttu-id="4bc7e-149">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="4bc7e-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="4bc7e-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4bc7e-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="4bc7e-151">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4bc7e-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="4bc7e-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="4bc7e-152">AzureRM.Websites</span></span>
* <span data-ttu-id="4bc7e-153">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="4bc7e-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="4bc7e-154">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="4bc7e-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="4bc7e-155">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="4bc7e-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="4bc7e-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bc7e-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="4bc7e-157">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="4bc7e-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="4bc7e-158">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="4bc7e-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4bc7e-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4bc7e-159">AzureRM.Profile</span></span>
* <span data-ttu-id="4bc7e-160">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="4bc7e-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4bc7e-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4bc7e-161">AzureRM.Compute</span></span>
* <span data-ttu-id="4bc7e-162">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="4bc7e-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="4bc7e-163">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bc7e-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="4bc7e-164">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="4bc7e-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4bc7e-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="4bc7e-166">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="4bc7e-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="4bc7e-167">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="4bc7e-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="4bc7e-168">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="4bc7e-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="4bc7e-169">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="4bc7e-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="4bc7e-170">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="4bc7e-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="4bc7e-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bc7e-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4bc7e-172">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="4bc7e-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="4bc7e-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4bc7e-173">AzureRM.Network</span></span>
* <span data-ttu-id="4bc7e-174">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="4bc7e-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="4bc7e-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="4bc7e-175">AzureRM.Resources</span></span>
* <span data-ttu-id="4bc7e-176">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="4bc7e-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="4bc7e-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="4bc7e-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="4bc7e-178">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="4bc7e-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="4bc7e-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4bc7e-179">AzureRM.Sql</span></span>
* <span data-ttu-id="4bc7e-180">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bc7e-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="4bc7e-181">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4bc7e-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="4bc7e-182">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4bc7e-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="4bc7e-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4bc7e-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="4bc7e-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bc7e-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="4bc7e-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4bc7e-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="4bc7e-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="4bc7e-186">AzureRM.Websites</span></span>
* <span data-ttu-id="4bc7e-187">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="4bc7e-188">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="4bc7e-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4bc7e-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4bc7e-189">AzureRM.Profile</span></span>
* <span data-ttu-id="4bc7e-190">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="4bc7e-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="4bc7e-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bc7e-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="4bc7e-192">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="4bc7e-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bc7e-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="4bc7e-194">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="4bc7e-195">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="4bc7e-196">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="4bc7e-197">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="4bc7e-198">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="4bc7e-199">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="4bc7e-200">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="4bc7e-200">Added support for MSI identity</span></span>
* <span data-ttu-id="4bc7e-201">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="4bc7e-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="4bc7e-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="4bc7e-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="4bc7e-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bc7e-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="4bc7e-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="4bc7e-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="4bc7e-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4bc7e-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="4bc7e-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="4bc7e-206">AzureRM.Batch</span></span>
* <span data-ttu-id="4bc7e-207">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="4bc7e-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="4bc7e-208">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="4bc7e-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="4bc7e-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="4bc7e-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="4bc7e-210">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="4bc7e-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="4bc7e-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bc7e-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="4bc7e-212">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="4bc7e-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="4bc7e-213">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="4bc7e-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="4bc7e-214">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="4bc7e-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="4bc7e-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4bc7e-215">AzureRM.Network</span></span>
* <span data-ttu-id="4bc7e-216">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="4bc7e-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="4bc7e-217">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="4bc7e-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="4bc7e-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bc7e-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="4bc7e-219">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="4bc7e-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bc7e-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4bc7e-221">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="4bc7e-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bc7e-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4bc7e-223">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="4bc7e-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="4bc7e-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4bc7e-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="4bc7e-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bc7e-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="4bc7e-226">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="4bc7e-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4bc7e-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4bc7e-227">AzureRM.Sql</span></span>
* <span data-ttu-id="4bc7e-228">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="4bc7e-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="4bc7e-229">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="4bc7e-230">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="4bc7e-231">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="4bc7e-232">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="4bc7e-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="4bc7e-233">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4bc7e-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="4bc7e-234">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4bc7e-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="4bc7e-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4bc7e-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="4bc7e-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bc7e-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="4bc7e-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4bc7e-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="4bc7e-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4bc7e-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="4bc7e-239">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="4bc7e-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>