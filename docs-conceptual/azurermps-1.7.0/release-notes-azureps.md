---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9f31fe404cca1162d5e4898287261f1bcbfa0f3a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821848"
---
# <a name="release-notes"></a><span data-ttu-id="ada1f-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="ada1f-103">Release notes</span></span>

<span data-ttu-id="ada1f-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="ada1f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="ada1f-105">1.7.0 版</span><span class="sxs-lookup"><span data-stu-id="ada1f-105">Version 1.7.0</span></span>

* <span data-ttu-id="ada1f-106">**所有 Cmdlet 的 -Force、–Confirm 和 $ConfirmPreference 參數行為變更我們正根據 PowerShell 指導方針變更此實作。對於大多數的 Cmdlet 而言，這表示移除 Force 參數，而要略過 ShouldProcess 提示，使用者必須在其 PowerShell 指令碼中包含 ‘-Confirm:$false’ 參數。**</span><span class="sxs-lookup"><span data-stu-id="ada1f-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="ada1f-107">此變更可處理下列問題︰</span><span class="sxs-lookup"><span data-stu-id="ada1f-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="ada1f-108">正確實作 –WhatIf 功能，可讓使用者判斷 Cmdlet 或指令碼的效果，而不需進行任何實際的變更</span><span class="sxs-lookup"><span data-stu-id="ada1f-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="ada1f-109">使用全工作階段的 $ConfirmPreference 控制提示，以便根據預期變更的影響來提示使用者 (如 Cmdlet 的 ConfirmImpact 設定所回報)</span><span class="sxs-lookup"><span data-stu-id="ada1f-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="ada1f-110">使用 –Confirm 參數進行 Cmdlet 特有的確認提示控制</span><span class="sxs-lookup"><span data-stu-id="ada1f-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="ada1f-111">在所有 Cmdlet 中一致使用 ShouldContinue 和 –Force 參數，僅適用於由於變更的特質而需要使用者提示的動作 (例如，刪除隱藏的檔案)</span><span class="sxs-lookup"><span data-stu-id="ada1f-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="ada1f-112">與其他的 PowerShell Cmdlet 一致，其他 Cmdlet 的 PowerShell 指令碼知識會立即套用至 Azure PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ada1f-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="ada1f-113">**請注意，現在要「自動略過所有情況下的所有提示」，Azure PowerShell Cmdlet 會要求使用者提供兩個參數︰**</span><span class="sxs-lookup"><span data-stu-id="ada1f-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="ada1f-114">Azure 計算</span><span class="sxs-lookup"><span data-stu-id="ada1f-114">Azure Compute</span></span>
  - <span data-ttu-id="ada1f-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="ada1f-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="ada1f-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="ada1f-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="ada1f-117">Restart-AzureVM 的 -Redeploy 參數</span><span class="sxs-lookup"><span data-stu-id="ada1f-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="ada1f-118">Move-AzureService、Move-AzureStorageAccount 和 Move-AzureVirtualNetwork 的 -Validate 參數</span><span class="sxs-lookup"><span data-stu-id="ada1f-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="ada1f-119">如同以往，擴充 Cmdlet 的名稱和版本參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ada1f-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="ada1f-120">New-AzureVM 可以從 VM 物件取得授權類型。</span><span class="sxs-lookup"><span data-stu-id="ada1f-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="ada1f-121">Azure 儲存體</span><span class="sxs-lookup"><span data-stu-id="ada1f-121">Azure Storage</span></span>
  - <span data-ttu-id="ada1f-122">將 Tags 參數變更為 Tag，並新增參數別名 Tags</span><span class="sxs-lookup"><span data-stu-id="ada1f-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="ada1f-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="ada1f-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ada1f-125">Azure 網路</span><span class="sxs-lookup"><span data-stu-id="ada1f-125">Azure Network</span></span>
  - <span data-ttu-id="ada1f-126">已針對虛擬網路對等互連新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ada1f-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="ada1f-127">Azure Redis 快取</span><span class="sxs-lookup"><span data-stu-id="ada1f-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="ada1f-128">已針對 Reset-AzureRmRedisCache 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ada1f-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="ada1f-129">已針對 Export-AzureRmRedisCache 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ada1f-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="ada1f-130">已針對 Import-AzureRmRedisCache 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ada1f-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="ada1f-131">已將 New-AzureRmRedisCache Cmdlet 修改為包含 vNet 的參數變更</span><span class="sxs-lookup"><span data-stu-id="ada1f-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="ada1f-132">Azure SQL DB 備份/還原</span><span class="sxs-lookup"><span data-stu-id="ada1f-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="ada1f-133">LTR (長期保留) 備份功能的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ada1f-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="ada1f-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="ada1f-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="ada1f-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ada1f-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="ada1f-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="ada1f-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="ada1f-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ada1f-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="ada1f-138">Restore-AzureRmSqlDatabase 現在支援已刪除資料庫的時間點還原</span><span class="sxs-lookup"><span data-stu-id="ada1f-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="ada1f-139">Restore-AzureRmSqlDatabase 現在支援從長期保留備份還原</span><span class="sxs-lookup"><span data-stu-id="ada1f-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="ada1f-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="ada1f-140">Azure LogicApp</span></span>
  - <span data-ttu-id="ada1f-141">已新增 LogicApp 整合帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ada1f-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="ada1f-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ada1f-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="ada1f-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ada1f-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="ada1f-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ada1f-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="ada1f-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="ada1f-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ada1f-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="ada1f-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ada1f-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="ada1f-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ada1f-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="ada1f-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ada1f-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="ada1f-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ada1f-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="ada1f-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="ada1f-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ada1f-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="ada1f-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ada1f-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="ada1f-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ada1f-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="ada1f-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ada1f-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="ada1f-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ada1f-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="ada1f-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="ada1f-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ada1f-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="ada1f-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ada1f-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="ada1f-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ada1f-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="ada1f-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ada1f-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="ada1f-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ada1f-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="ada1f-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ada1f-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="ada1f-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ada1f-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="ada1f-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ada1f-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="ada1f-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ada1f-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="ada1f-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ada1f-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="ada1f-168">大幅改善檔案和資料夾上傳及下載的效能。</span><span class="sxs-lookup"><span data-stu-id="ada1f-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="ada1f-169">這包括小幅變更參數名稱 (針對下載) 以及包含兩個新參數 (針對上傳)︰</span><span class="sxs-lookup"><span data-stu-id="ada1f-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="ada1f-170">NumThreads -> PerFileThreadCount，用來指出要在單一檔案中使用的執行緒數目</span><span class="sxs-lookup"><span data-stu-id="ada1f-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="ada1f-171">ConcurrentFileCount，用來指出要上傳/下載平行資料夾上傳/下載檔案數目。</span><span class="sxs-lookup"><span data-stu-id="ada1f-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="ada1f-172">預設執行緒值現在的設計是針對大部分的檔案大小提供更理想的全面性輸送量。</span><span class="sxs-lookup"><span data-stu-id="ada1f-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="ada1f-173">如果效能不如預期，可以修改上述的值以符合需求。</span><span class="sxs-lookup"><span data-stu-id="ada1f-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="ada1f-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ada1f-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="ada1f-175">若未使用引數呼叫 Get-AzureRMDataLakeAnalyticsDataSource，現在會傳回所有的資料來源。</span><span class="sxs-lookup"><span data-stu-id="ada1f-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="ada1f-176">這項變更也會從 Cmdlet 中移除資料來源類型參數。</span><span class="sxs-lookup"><span data-stu-id="ada1f-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="ada1f-177">這項變更會導致使用下列屬性針對清單作業傳回新物件︰</span><span class="sxs-lookup"><span data-stu-id="ada1f-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="ada1f-178">Type：資料來源的類型</span><span class="sxs-lookup"><span data-stu-id="ada1f-178">Type, the type of data source</span></span>
    + <span data-ttu-id="ada1f-179">Name：資料來源的名稱</span><span class="sxs-lookup"><span data-stu-id="ada1f-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="ada1f-180">IsDefault：如果這是帳戶的預設資料來源，則設定為 true</span><span class="sxs-lookup"><span data-stu-id="ada1f-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="ada1f-181">Get-AzureRMDataLakeAnalyticsJob 已修正根據 submittedBefore 和 submittedAfter 篩選時，某些日期時間位移值的清單。</span><span class="sxs-lookup"><span data-stu-id="ada1f-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="ada1f-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="ada1f-182">Web Apps</span></span>
  - <span data-ttu-id="ada1f-183">新增 Swap-AzureRmWebAppSlot Cmdlet 以便進行定期交換和使用預覽交換</span><span class="sxs-lookup"><span data-stu-id="ada1f-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="ada1f-184">擴充 Set-AzureRmWebAppSlot Cmdlet 以支援自動交換</span><span class="sxs-lookup"><span data-stu-id="ada1f-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="ada1f-185">Azure API 管理</span><span class="sxs-lookup"><span data-stu-id="ada1f-185">Azure API Management</span></span>
  - <span data-ttu-id="ada1f-186">已修正 AzureChinaCloud 的 Azure Api 管理部署 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ada1f-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="ada1f-187">已移除 Cmdlet Set-AzureRmApiManagementTenantGitAccess，因為預設會啟用 Git 存取。</span><span class="sxs-lookup"><span data-stu-id="ada1f-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="ada1f-188">Azure 復原服務備份</span><span class="sxs-lookup"><span data-stu-id="ada1f-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="ada1f-189">已新增 Azure SQL 工作負載的支援</span><span class="sxs-lookup"><span data-stu-id="ada1f-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="ada1f-190">已新增備份及還原已加密 Azure VM 的支援</span><span class="sxs-lookup"><span data-stu-id="ada1f-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="ada1f-191">Backup-AzureRmRecoveryServicesBackupItem - 已新增復原點的選擇性保留時間功能</span><span class="sxs-lookup"><span data-stu-id="ada1f-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="ada1f-192">Get-AzureRmRecoveryServicesBackupContainer 和 Get-AzureRmRecoveryServicesBackupItem Cmdlet 中的小幅篩選相關錯誤修正</span><span class="sxs-lookup"><span data-stu-id="ada1f-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="ada1f-193">Azure 自動化</span><span class="sxs-lookup"><span data-stu-id="ada1f-193">Azure Automation</span></span>
  - <span data-ttu-id="ada1f-194">已新增 Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ada1f-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
