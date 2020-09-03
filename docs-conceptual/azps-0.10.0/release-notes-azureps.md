---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: f0a8c70ac16c99235b9497cddd03ec4796b40482
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239344"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="80d97-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="80d97-104">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="80d97-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="80d97-105">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-105">General</span></span>
* <span data-ttu-id="80d97-106">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="80d97-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="80d97-107">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="80d97-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="80d97-108">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="80d97-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="80d97-109">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="80d97-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="80d97-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="80d97-110">Az.Billing</span></span>
  - <span data-ttu-id="80d97-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-111">Az.Compute</span></span>
  - <span data-ttu-id="80d97-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="80d97-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="80d97-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-113">Az.EventHub</span></span>
  - <span data-ttu-id="80d97-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-114">Az.IotHub</span></span>
  - <span data-ttu-id="80d97-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-115">Az.KeyVault</span></span>
  - <span data-ttu-id="80d97-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-116">Az.Monitor</span></span>
  - <span data-ttu-id="80d97-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-117">Az.Network</span></span>
  - <span data-ttu-id="80d97-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-118">Az.Resources</span></span>
  - <span data-ttu-id="80d97-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-119">Az.Storage</span></span>
  - <span data-ttu-id="80d97-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-120">Az.Websites</span></span>
* <span data-ttu-id="80d97-121">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="80d97-122">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="80d97-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="80d97-123">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="80d97-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-124">Az.Accounts</span></span>
* <span data-ttu-id="80d97-125">從 ADAL 升級至 MSAL</span><span class="sxs-lookup"><span data-stu-id="80d97-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="80d97-126">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="80d97-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-127">Az.Accounts</span></span>
* <span data-ttu-id="80d97-128">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="80d97-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-129">Az.Compute</span></span>
* <span data-ttu-id="80d97-130">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="80d97-131">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="80d97-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="80d97-132">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="80d97-133">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="80d97-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="80d97-134">[#11354]</span></span>
* <span data-ttu-id="80d97-135">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="80d97-136">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="80d97-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="80d97-137">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="80d97-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="80d97-138">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="80d97-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="80d97-139">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="80d97-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="80d97-140">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="80d97-141">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="80d97-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="80d97-142">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="80d97-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="80d97-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="80d97-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-144">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-145">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="80d97-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="80d97-146">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="80d97-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-148">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="80d97-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="80d97-149">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="80d97-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-150">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-151">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="80d97-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-152">Az.IotHub</span></span>
* <span data-ttu-id="80d97-153">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="80d97-154">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="80d97-155">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="80d97-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="80d97-156">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="80d97-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-157">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-158">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="80d97-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-159">Az.Monitor</span></span>
* <span data-ttu-id="80d97-160">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="80d97-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-161">Az.Network</span></span>
* <span data-ttu-id="80d97-162">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="80d97-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="80d97-163">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="80d97-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="80d97-164">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="80d97-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="80d97-165">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="80d97-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="80d97-166">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="80d97-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="80d97-167">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-169">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-171">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="80d97-172">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="80d97-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="80d97-173">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="80d97-174">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="80d97-175">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="80d97-176">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-177">Az.Resources</span></span>
* <span data-ttu-id="80d97-178">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="80d97-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="80d97-179">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="80d97-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="80d97-180">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="80d97-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="80d97-181">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="80d97-181">Added example.</span></span>
* <span data-ttu-id="80d97-182">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="80d97-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="80d97-183">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-184">Az.Sql</span></span>
* <span data-ttu-id="80d97-185">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="80d97-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="80d97-186">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="80d97-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="80d97-187">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="80d97-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="80d97-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="80d97-188">Az.Support</span></span>
* <span data-ttu-id="80d97-189">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="80d97-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-190">Az.Websites</span></span>
* <span data-ttu-id="80d97-191">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="80d97-192">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="80d97-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="80d97-193">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="80d97-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="80d97-194">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="80d97-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="80d97-195">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="80d97-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="80d97-196">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="80d97-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-197">Az.Accounts</span></span>
* <span data-ttu-id="80d97-198">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="80d97-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="80d97-199">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="80d97-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="80d97-200">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="80d97-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="80d97-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-201">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-202">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="80d97-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="80d97-203">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="80d97-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="80d97-204">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="80d97-205">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="80d97-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-207">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="80d97-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-208">Az.IotHub</span></span>
* <span data-ttu-id="80d97-209">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="80d97-210">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="80d97-211">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-212">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-213">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-214">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="80d97-215">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="80d97-216">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="80d97-217">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="80d97-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="80d97-218">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="80d97-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="80d97-219">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="80d97-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="80d97-220">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="80d97-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="80d97-221">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="80d97-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="80d97-222">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="80d97-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="80d97-223">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="80d97-224">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="80d97-225">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="80d97-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="80d97-226">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="80d97-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="80d97-227">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-228">Az.Monitor</span></span>
* <span data-ttu-id="80d97-229">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="80d97-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-230">Az.Network</span></span>
* <span data-ttu-id="80d97-231">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="80d97-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="80d97-232">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="80d97-233">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="80d97-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="80d97-234">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="80d97-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-235">Az.Resources</span></span>
* <span data-ttu-id="80d97-236">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="80d97-237">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="80d97-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="80d97-238">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="80d97-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="80d97-239">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="80d97-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="80d97-240">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="80d97-241">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="80d97-242">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="80d97-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="80d97-243">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d97-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="80d97-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d97-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="80d97-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d97-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="80d97-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d97-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="80d97-247">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="80d97-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="80d97-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="80d97-249">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="80d97-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-250">Az.Sql</span></span>
* <span data-ttu-id="80d97-251">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="80d97-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="80d97-252">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="80d97-253">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="80d97-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="80d97-254">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="80d97-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="80d97-255">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="80d97-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="80d97-256">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="80d97-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="80d97-257">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="80d97-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="80d97-258">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="80d97-259">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="80d97-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-260">Az.Storage</span></span>
* <span data-ttu-id="80d97-261">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="80d97-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="80d97-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="80d97-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="80d97-263">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="80d97-264">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="80d97-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="80d97-265">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="80d97-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-266">Az.Websites</span></span>
* <span data-ttu-id="80d97-267">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="80d97-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="80d97-268">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="80d97-269">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="80d97-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="80d97-270">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="80d97-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="80d97-271">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="80d97-272">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="80d97-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-273">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-273">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-274">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="80d97-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="80d97-275">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="80d97-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="80d97-276">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-277">Az.Accounts</span></span>
* <span data-ttu-id="80d97-278">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="80d97-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-279">Az.Automation</span></span>
* <span data-ttu-id="80d97-280">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-282">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="80d97-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="80d97-283">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-284">Az.Compute</span></span>
* <span data-ttu-id="80d97-285">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="80d97-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-286">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-287">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="80d97-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-288">Az.IotHub</span></span>
* <span data-ttu-id="80d97-289">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="80d97-290">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="80d97-291">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-292">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-293">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="80d97-294">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="80d97-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-295">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-296">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="80d97-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-297">Az.Monitor</span></span>
* <span data-ttu-id="80d97-298">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="80d97-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="80d97-299">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="80d97-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="80d97-300">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="80d97-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-301">Az.Network</span></span>
* <span data-ttu-id="80d97-302">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="80d97-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="80d97-303">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="80d97-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="80d97-304">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="80d97-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="80d97-305">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="80d97-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="80d97-306">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-306">No new cmdlets are added.</span></span> <span data-ttu-id="80d97-307">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="80d97-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-309">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-310">Az.Resources</span></span>
* <span data-ttu-id="80d97-311">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="80d97-312">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="80d97-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="80d97-313">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="80d97-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="80d97-314">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="80d97-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="80d97-315">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="80d97-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="80d97-316">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="80d97-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="80d97-317">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="80d97-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="80d97-318">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="80d97-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-319">Az.Sql</span></span>
* <span data-ttu-id="80d97-320">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="80d97-321">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="80d97-322">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="80d97-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="80d97-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="80d97-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="80d97-324">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="80d97-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="80d97-325">Az.StorageSync</span></span>
* <span data-ttu-id="80d97-326">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="80d97-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="80d97-327">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="80d97-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-328">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-328">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-329">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="80d97-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="80d97-330">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="80d97-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-331">Az.Accounts</span></span>
* <span data-ttu-id="80d97-332">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="80d97-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="80d97-333">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="80d97-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="80d97-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-334">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-335">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="80d97-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="80d97-336">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="80d97-336">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="80d97-337">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="80d97-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="80d97-338">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="80d97-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-339">Az.Compute</span></span>
* <span data-ttu-id="80d97-340">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="80d97-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="80d97-341">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="80d97-342">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="80d97-343">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="80d97-344">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-345">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-346">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="80d97-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="80d97-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="80d97-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="80d97-348">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="80d97-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="80d97-349">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="80d97-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-350">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-351">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="80d97-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-352">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-353">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="80d97-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-354">Az.Network</span></span>
* <span data-ttu-id="80d97-355">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="80d97-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="80d97-356">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="80d97-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="80d97-357">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="80d97-358">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="80d97-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="80d97-359">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="80d97-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="80d97-360">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="80d97-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="80d97-361">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="80d97-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="80d97-362">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="80d97-363">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-363">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="80d97-365">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="80d97-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="80d97-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="80d97-367">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-369">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="80d97-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="80d97-370">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="80d97-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="80d97-371">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="80d97-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="80d97-372">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="80d97-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-374">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="80d97-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="80d97-375">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-376">Az.Resources</span></span>
* <span data-ttu-id="80d97-377">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="80d97-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="80d97-378">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-379">Az.Sql</span></span>
<span data-ttu-id="80d97-380">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="80d97-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-381">Az.Storage</span></span>
* <span data-ttu-id="80d97-382">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="80d97-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="80d97-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="80d97-384">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="80d97-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="80d97-385">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="80d97-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-386">Az.Websites</span></span>
* <span data-ttu-id="80d97-387">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="80d97-388">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="80d97-389">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="80d97-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-390">Az.Accounts</span></span>
* <span data-ttu-id="80d97-391">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-392">Az.Cdn</span></span>
* <span data-ttu-id="80d97-393">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="80d97-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-394">Az.Compute</span></span>
* <span data-ttu-id="80d97-395">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="80d97-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="80d97-397">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="80d97-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="80d97-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="80d97-399">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="80d97-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="80d97-400">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="80d97-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="80d97-401">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="80d97-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="80d97-402">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="80d97-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="80d97-403">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="80d97-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="80d97-404">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="80d97-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="80d97-405">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="80d97-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="80d97-406">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="80d97-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="80d97-407">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="80d97-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="80d97-408">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="80d97-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="80d97-409">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="80d97-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="80d97-410">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="80d97-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="80d97-411">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="80d97-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="80d97-412">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="80d97-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="80d97-413">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="80d97-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="80d97-414">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="80d97-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="80d97-415">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="80d97-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="80d97-416">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="80d97-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-417">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-418">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="80d97-419">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="80d97-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="80d97-420">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="80d97-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="80d97-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="80d97-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="80d97-422">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="80d97-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-423">Az.EventHub</span></span>
* <span data-ttu-id="80d97-424">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="80d97-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-425">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-426">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="80d97-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="80d97-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="80d97-427">Az.MachineLearning</span></span>
* <span data-ttu-id="80d97-428">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="80d97-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="80d97-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="80d97-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="80d97-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="80d97-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="80d97-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="80d97-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="80d97-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="80d97-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="80d97-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="80d97-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="80d97-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="80d97-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="80d97-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-436">Az.Network</span></span>
* <span data-ttu-id="80d97-437">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="80d97-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-439">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="80d97-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="80d97-440">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="80d97-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="80d97-441">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="80d97-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="80d97-442">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="80d97-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-443">Az.Resources</span></span>
* <span data-ttu-id="80d97-444">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="80d97-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-445">Az.Sql</span></span>
* <span data-ttu-id="80d97-446">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="80d97-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="80d97-447">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="80d97-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="80d97-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="80d97-449">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="80d97-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-450">Az.Storage</span></span>
* <span data-ttu-id="80d97-451">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="80d97-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="80d97-453">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="80d97-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="80d97-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="80d97-455">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="80d97-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="80d97-456">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-456">General</span></span>
* <span data-ttu-id="80d97-457">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="80d97-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-458">Az.Accounts</span></span>
* <span data-ttu-id="80d97-459">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="80d97-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="80d97-460">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="80d97-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-461">Az.Batch</span></span>
* <span data-ttu-id="80d97-462">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="80d97-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-463">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-464">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="80d97-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-465">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-466">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="80d97-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="80d97-467">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="80d97-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="80d97-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="80d97-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="80d97-469">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="80d97-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-470">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-471">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="80d97-472">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="80d97-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="80d97-473">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-474">Az.Monitor</span></span>
* <span data-ttu-id="80d97-475">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="80d97-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="80d97-476">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="80d97-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="80d97-477">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="80d97-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-478">Az.Network</span></span>
* <span data-ttu-id="80d97-479">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="80d97-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-480">Az.Resources</span></span>
* <span data-ttu-id="80d97-481">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="80d97-482">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-483">Az.Sql</span></span>
* <span data-ttu-id="80d97-484">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="80d97-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-485">Az.Storage</span></span>
* <span data-ttu-id="80d97-486">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="80d97-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="80d97-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="80d97-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="80d97-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="80d97-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="80d97-489">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="80d97-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="80d97-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="80d97-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="80d97-491">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="80d97-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="80d97-492">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="80d97-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="80d97-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="80d97-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="80d97-495">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="80d97-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="80d97-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="80d97-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="80d97-497">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="80d97-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="80d97-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="80d97-499">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="80d97-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-500">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-500">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-501">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="80d97-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="80d97-502">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="80d97-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-503">Az.Compute</span></span>
* <span data-ttu-id="80d97-504">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="80d97-504">VM Reapply feature</span></span>
    - <span data-ttu-id="80d97-505">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="80d97-506">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="80d97-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="80d97-507">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="80d97-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="80d97-508">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="80d97-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="80d97-509">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="80d97-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="80d97-510">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="80d97-511">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="80d97-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="80d97-512">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="80d97-513">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="80d97-514">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="80d97-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="80d97-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="80d97-516">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="80d97-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="80d97-517">取得訂單</span><span class="sxs-lookup"><span data-stu-id="80d97-517">Get the Order</span></span>
* <span data-ttu-id="80d97-518">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="80d97-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="80d97-519">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="80d97-519">Create new Order</span></span>
* <span data-ttu-id="80d97-520">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="80d97-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="80d97-521">移除訂單</span><span class="sxs-lookup"><span data-stu-id="80d97-521">Remove the Order</span></span>
* <span data-ttu-id="80d97-522">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="80d97-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="80d97-523">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="80d97-523">Now creates Local Share</span></span>
* <span data-ttu-id="80d97-524">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="80d97-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="80d97-525">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="80d97-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="80d97-526">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="80d97-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="80d97-527">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="80d97-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="80d97-528">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="80d97-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="80d97-529">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="80d97-530">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="80d97-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="80d97-531">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="80d97-531">Create new Triggers</span></span>
* <span data-ttu-id="80d97-532">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="80d97-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="80d97-533">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="80d97-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-534">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-535">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="80d97-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="80d97-536">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="80d97-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-538">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="80d97-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-539">Az.EventHub</span></span>
* <span data-ttu-id="80d97-540">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="80d97-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-541">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-542">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="80d97-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="80d97-543">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="80d97-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="80d97-544">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="80d97-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="80d97-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="80d97-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-546">Az.Network</span></span>
* <span data-ttu-id="80d97-547">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="80d97-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="80d97-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="80d97-548">Az.PrivateDns</span></span>
* <span data-ttu-id="80d97-549">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="80d97-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-551">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="80d97-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="80d97-552">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="80d97-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="80d97-553">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="80d97-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="80d97-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="80d97-554">Az.RedisCache</span></span>
* <span data-ttu-id="80d97-555">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="80d97-556">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="80d97-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="80d97-557">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="80d97-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-558">Az.Resources</span></span>
- <span data-ttu-id="80d97-559">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="80d97-560">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="80d97-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="80d97-561">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="80d97-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="80d97-562">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="80d97-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="80d97-563">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="80d97-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-564">Az.Sql</span></span>
* <span data-ttu-id="80d97-565">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="80d97-566">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80d97-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="80d97-567">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="80d97-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="80d97-568">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-568">General</span></span>
* <span data-ttu-id="80d97-569">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="80d97-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-570">Az.Accounts</span></span>
* <span data-ttu-id="80d97-571">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="80d97-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="80d97-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="80d97-572">Az.Advisor</span></span>
* <span data-ttu-id="80d97-573">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="80d97-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="80d97-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-574">Az.Batch</span></span>
* <span data-ttu-id="80d97-575">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="80d97-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="80d97-576">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="80d97-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="80d97-577">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="80d97-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="80d97-578">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="80d97-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="80d97-579">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="80d97-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="80d97-580">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="80d97-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="80d97-581">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="80d97-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="80d97-582">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="80d97-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="80d97-583">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="80d97-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="80d97-584">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="80d97-585">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="80d97-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="80d97-586">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="80d97-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="80d97-587">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="80d97-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="80d97-588">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="80d97-589">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="80d97-590">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="80d97-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="80d97-591">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="80d97-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="80d97-592">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="80d97-593">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="80d97-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="80d97-594">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="80d97-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="80d97-595">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="80d97-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="80d97-596">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="80d97-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="80d97-597">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="80d97-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="80d97-598">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="80d97-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="80d97-599">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="80d97-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="80d97-600">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="80d97-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="80d97-601">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80d97-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="80d97-602">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="80d97-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="80d97-603">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="80d97-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="80d97-604">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="80d97-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="80d97-605">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="80d97-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="80d97-606">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="80d97-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="80d97-607">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="80d97-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="80d97-608">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="80d97-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="80d97-609">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="80d97-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="80d97-610">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="80d97-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-611">Az.Cdn</span></span>
* <span data-ttu-id="80d97-612">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="80d97-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="80d97-613">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="80d97-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-614">Az.Compute</span></span>
* <span data-ttu-id="80d97-615">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="80d97-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="80d97-616">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="80d97-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="80d97-617">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="80d97-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="80d97-618">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="80d97-619">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="80d97-620">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="80d97-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="80d97-621">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="80d97-622">重大變更</span><span class="sxs-lookup"><span data-stu-id="80d97-622">Breaking changes</span></span>
    - <span data-ttu-id="80d97-623">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="80d97-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="80d97-624">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="80d97-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-625">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-626">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="80d97-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-628">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="80d97-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="80d97-629">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="80d97-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="80d97-630">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="80d97-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="80d97-631">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="80d97-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="80d97-632">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="80d97-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="80d97-633">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-634">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-635">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="80d97-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-636">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-637">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="80d97-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="80d97-638">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="80d97-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="80d97-639">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="80d97-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="80d97-640">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="80d97-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="80d97-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="80d97-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="80d97-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="80d97-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="80d97-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="80d97-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="80d97-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="80d97-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="80d97-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="80d97-646">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="80d97-647">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="80d97-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="80d97-648">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="80d97-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="80d97-649">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="80d97-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="80d97-650">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="80d97-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="80d97-651">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="80d97-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="80d97-652">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="80d97-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="80d97-653">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="80d97-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="80d97-654">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="80d97-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="80d97-655">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="80d97-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="80d97-656">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="80d97-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="80d97-657">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="80d97-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="80d97-658">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="80d97-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-659">Az.IotHub</span></span>
* <span data-ttu-id="80d97-660">重大變更：</span><span class="sxs-lookup"><span data-stu-id="80d97-660">Breaking changes:</span></span>
    - <span data-ttu-id="80d97-661">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="80d97-662">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="80d97-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="80d97-663">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="80d97-664">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="80d97-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="80d97-665">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="80d97-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="80d97-666">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="80d97-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="80d97-667">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="80d97-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="80d97-668">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="80d97-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="80d97-669">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="80d97-670">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="80d97-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="80d97-671">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="80d97-672">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="80d97-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-674">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="80d97-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-675">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="80d97-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="80d97-676">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="80d97-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="80d97-677">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="80d97-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-678">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="80d97-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-679">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="80d97-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-680">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="80d97-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-681">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-682">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="80d97-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-683">Az.Resources</span></span>
* <span data-ttu-id="80d97-684">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="80d97-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-685">Az.Network</span></span>
* <span data-ttu-id="80d97-686">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="80d97-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="80d97-687">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="80d97-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="80d97-693">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="80d97-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="80d97-694">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-694">New cmdlet:</span></span>
        - <span data-ttu-id="80d97-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="80d97-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="80d97-696">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="80d97-697">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="80d97-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="80d97-698">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="80d97-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="80d97-699">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="80d97-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="80d97-700">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="80d97-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="80d97-701">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="80d97-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="80d97-702">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="80d97-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="80d97-703">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-703">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="80d97-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="80d97-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="80d97-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="80d97-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="80d97-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="80d97-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="80d97-709">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="80d97-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="80d97-710">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="80d97-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="80d97-711">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="80d97-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="80d97-712">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="80d97-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="80d97-713">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="80d97-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="80d97-714">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="80d97-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="80d97-715">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="80d97-716">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-716">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="80d97-718">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="80d97-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="80d97-719">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="80d97-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="80d97-720">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="80d97-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="80d97-721">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="80d97-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="80d97-722">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="80d97-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="80d97-723">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="80d97-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="80d97-724">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="80d97-725">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-725">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="80d97-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="80d97-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="80d97-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="80d97-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="80d97-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="80d97-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="80d97-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="80d97-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="80d97-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="80d97-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="80d97-732">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="80d97-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="80d97-733">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="80d97-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="80d97-734">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="80d97-735">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="80d97-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="80d97-736">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="80d97-737">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="80d97-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="80d97-738">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="80d97-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="80d97-739">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="80d97-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="80d97-740">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="80d97-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="80d97-741">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="80d97-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="80d97-742">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="80d97-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="80d97-743">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-743">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="80d97-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="80d97-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="80d97-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-749">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="80d97-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-750">Az.Sql</span></span>
* <span data-ttu-id="80d97-751">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="80d97-752">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="80d97-753">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="80d97-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="80d97-754">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="80d97-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="80d97-755">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="80d97-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="80d97-756">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="80d97-757">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="80d97-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="80d97-758">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="80d97-759">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="80d97-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-760">Az.Storage</span></span>
* <span data-ttu-id="80d97-761">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="80d97-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="80d97-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="80d97-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="80d97-764">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="80d97-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="80d97-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="80d97-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="80d97-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="80d97-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="80d97-767">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="80d97-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="80d97-768">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-768">General</span></span>
* <span data-ttu-id="80d97-769">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="80d97-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-770">Az.Accounts</span></span>
* <span data-ttu-id="80d97-771">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="80d97-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="80d97-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-772">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-773">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="80d97-774">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-775">Az.Automation</span></span>
* <span data-ttu-id="80d97-776">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="80d97-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-777">Az.Batch</span></span>
* <span data-ttu-id="80d97-778">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="80d97-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-779">Az.Compute</span></span>
* <span data-ttu-id="80d97-780">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="80d97-781">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="80d97-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="80d97-782">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="80d97-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="80d97-783">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="80d97-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-784">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-785">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="80d97-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="80d97-786">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="80d97-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="80d97-787">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="80d97-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-789">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="80d97-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="80d97-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="80d97-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="80d97-791">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="80d97-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="80d97-792">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="80d97-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="80d97-793">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="80d97-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="80d97-794">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="80d97-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-795">Az.IotHub</span></span>
* <span data-ttu-id="80d97-796">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="80d97-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="80d97-797">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="80d97-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-798">Az.Monitor</span></span>
* <span data-ttu-id="80d97-799">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="80d97-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="80d97-800">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="80d97-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="80d97-801">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="80d97-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="80d97-802">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="80d97-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-803">Az.Network</span></span>
* <span data-ttu-id="80d97-804">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="80d97-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="80d97-805">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="80d97-806">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-806">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="80d97-808">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="80d97-809">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="80d97-810">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="80d97-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="80d97-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="80d97-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="80d97-814">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="80d97-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="80d97-815">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="80d97-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="80d97-816">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="80d97-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="80d97-817">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="80d97-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="80d97-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="80d97-818">Az.RedisCache</span></span>
* <span data-ttu-id="80d97-819">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="80d97-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-820">Az.Sql</span></span>
* <span data-ttu-id="80d97-821">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-822">Az.Storage</span></span>
* <span data-ttu-id="80d97-823">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="80d97-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="80d97-824">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="80d97-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="80d97-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="80d97-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="80d97-826">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="80d97-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="80d97-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="80d97-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="80d97-828">Az.StorageSync</span></span>
* <span data-ttu-id="80d97-829">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="80d97-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-830">Az.Websites</span></span>
* <span data-ttu-id="80d97-831">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="80d97-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="80d97-832">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="80d97-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="80d97-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-833">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-834">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="80d97-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="80d97-835">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="80d97-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="80d97-836">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="80d97-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-837">Az.Automation</span></span>
* <span data-ttu-id="80d97-838">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="80d97-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="80d97-839">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="80d97-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="80d97-840">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="80d97-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-841">Az.Compute</span></span>
* <span data-ttu-id="80d97-842">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="80d97-843">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="80d97-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="80d97-844">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="80d97-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="80d97-845">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="80d97-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="80d97-846">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="80d97-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="80d97-847">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="80d97-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="80d97-848">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="80d97-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="80d97-849">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="80d97-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="80d97-850">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-851">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-852">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="80d97-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="80d97-853">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="80d97-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-854">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-855">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="80d97-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-856">Az.IotHub</span></span>
* <span data-ttu-id="80d97-857">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="80d97-858">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="80d97-859">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="80d97-859">New cmdlets are:</span></span>
    - <span data-ttu-id="80d97-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="80d97-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="80d97-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="80d97-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="80d97-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="80d97-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="80d97-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="80d97-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-864">Az.Monitor</span></span>
* <span data-ttu-id="80d97-865">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="80d97-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="80d97-866">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="80d97-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="80d97-867">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="80d97-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="80d97-868">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="80d97-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="80d97-869">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="80d97-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="80d97-870">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="80d97-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="80d97-871">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="80d97-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="80d97-872">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="80d97-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="80d97-873">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="80d97-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="80d97-874">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="80d97-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="80d97-875">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="80d97-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="80d97-876">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="80d97-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="80d97-877">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="80d97-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="80d97-878">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="80d97-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="80d97-879">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="80d97-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="80d97-880">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="80d97-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="80d97-881">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="80d97-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="80d97-882">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="80d97-883">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="80d97-884">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="80d97-884">Overall improved help files</span></span>
* <span data-ttu-id="80d97-885">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-886">Az.Network</span></span>
* <span data-ttu-id="80d97-887">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="80d97-888">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="80d97-889">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="80d97-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="80d97-890">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="80d97-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="80d97-891">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="80d97-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="80d97-892">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="80d97-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="80d97-893">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="80d97-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="80d97-894">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="80d97-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="80d97-895">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="80d97-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="80d97-896">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="80d97-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="80d97-897">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="80d97-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="80d97-898">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="80d97-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="80d97-899">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-899">New cmdlets</span></span>
        - <span data-ttu-id="80d97-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="80d97-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="80d97-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="80d97-902">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="80d97-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="80d97-903">New-VpnSite</span></span>
        - <span data-ttu-id="80d97-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="80d97-904">Update-VpnSite</span></span>
        - <span data-ttu-id="80d97-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-905">New-VpnConnection</span></span>
        - <span data-ttu-id="80d97-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-906">Update-VpnConnection</span></span>
* <span data-ttu-id="80d97-907">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-909">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="80d97-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="80d97-910">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="80d97-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-911">Az.Resources</span></span>
* <span data-ttu-id="80d97-912">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="80d97-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-914">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="80d97-915">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="80d97-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="80d97-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="80d97-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="80d97-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="80d97-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="80d97-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="80d97-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="80d97-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="80d97-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="80d97-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="80d97-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="80d97-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="80d97-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="80d97-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="80d97-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="80d97-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="80d97-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="80d97-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="80d97-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="80d97-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="80d97-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="80d97-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="80d97-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="80d97-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="80d97-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="80d97-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="80d97-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="80d97-929">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="80d97-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="80d97-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="80d97-930">Az.SignalR</span></span>
* <span data-ttu-id="80d97-931">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-932">Az.Sql</span></span>
* <span data-ttu-id="80d97-933">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="80d97-934">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="80d97-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="80d97-935">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="80d97-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="80d97-936">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="80d97-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="80d97-937">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="80d97-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-938">Az.Storage</span></span>
* <span data-ttu-id="80d97-939">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="80d97-940">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="80d97-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="80d97-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="80d97-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="80d97-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="80d97-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="80d97-943">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="80d97-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="80d97-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="80d97-945">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="80d97-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="80d97-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="80d97-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="80d97-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="80d97-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="80d97-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-950">Az.Websites</span></span>
* <span data-ttu-id="80d97-951">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="80d97-952">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="80d97-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="80d97-953">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="80d97-954">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="80d97-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="80d97-955">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-955">General</span></span>
* <span data-ttu-id="80d97-956">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="80d97-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-957">Az.Accounts</span></span>
* <span data-ttu-id="80d97-958">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="80d97-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="80d97-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="80d97-959">Az.Aks</span></span>
* <span data-ttu-id="80d97-960">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="80d97-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="80d97-961">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="80d97-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="80d97-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-962">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-963">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="80d97-964">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="80d97-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="80d97-965">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="80d97-966">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="80d97-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="80d97-967">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="80d97-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="80d97-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-968">Az.Batch</span></span>
* <span data-ttu-id="80d97-969">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="80d97-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-970">Az.Cdn</span></span>
* <span data-ttu-id="80d97-971">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-972">Az.Compute</span></span>
* <span data-ttu-id="80d97-973">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="80d97-974">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="80d97-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="80d97-975">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="80d97-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="80d97-976">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="80d97-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="80d97-977">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="80d97-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="80d97-978">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="80d97-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="80d97-979">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="80d97-980">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="80d97-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-981">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-982">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="80d97-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="80d97-983">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="80d97-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="80d97-984">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="80d97-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="80d97-985">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="80d97-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-987">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="80d97-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-988">Az.EventHub</span></span>
* <span data-ttu-id="80d97-989">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="80d97-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="80d97-990">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="80d97-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="80d97-991">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="80d97-992">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="80d97-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="80d97-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="80d97-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="80d97-994">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="80d97-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-995">Az.Monitor</span></span>
* <span data-ttu-id="80d97-996">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-997">Az.Network</span></span>
* <span data-ttu-id="80d97-998">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="80d97-999">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="80d97-1000">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="80d97-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="80d97-1001">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="80d97-1002">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="80d97-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="80d97-1003">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="80d97-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="80d97-1004">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1006">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="80d97-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="80d97-1007">新增了範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1007">Added example</span></span>
    - <span data-ttu-id="80d97-1008">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="80d97-1009">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="80d97-1010">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1012">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1013">Az.Resources</span></span>
* <span data-ttu-id="80d97-1014">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="80d97-1015">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="80d97-1016">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="80d97-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="80d97-1017">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-1019">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="80d97-1020">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="80d97-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="80d97-1021">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="80d97-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-1023">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="80d97-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="80d97-1024">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="80d97-1025">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="80d97-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="80d97-1026">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="80d97-1027">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="80d97-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="80d97-1028">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1029">Az.Sql</span></span>
* <span data-ttu-id="80d97-1030">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="80d97-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1031">Az.Storage</span></span>
* <span data-ttu-id="80d97-1032">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="80d97-1033">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="80d97-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="80d97-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="80d97-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="80d97-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="80d97-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="80d97-1036">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="80d97-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="80d97-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="80d97-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1038">Az.Websites</span></span>
* <span data-ttu-id="80d97-1039">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="80d97-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="80d97-1040">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1041">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1042">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="80d97-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="80d97-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="80d97-1044">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1045">Az.Automation</span></span>
* <span data-ttu-id="80d97-1046">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-1048">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1049">Az.Compute</span></span>
* <span data-ttu-id="80d97-1050">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="80d97-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80d97-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="80d97-1052">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="80d97-1053">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="80d97-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1054">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1055">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="80d97-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="80d97-1056">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1057">Az.EventHub</span></span>
* <span data-ttu-id="80d97-1058">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="80d97-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="80d97-1059">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1060">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-1061">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="80d97-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="80d97-1062">Az.LogicApp</span></span>
* <span data-ttu-id="80d97-1063">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="80d97-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="80d97-1064">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="80d97-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="80d97-1066">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1067">Az.Network</span></span>
* <span data-ttu-id="80d97-1068">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="80d97-1069">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1069">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d97-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="80d97-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="80d97-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="80d97-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="80d97-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="80d97-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="80d97-1078">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="80d97-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="80d97-1079">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="80d97-1080">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="80d97-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="80d97-1081">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="80d97-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="80d97-1082">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="80d97-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="80d97-1083">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="80d97-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="80d97-1084">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="80d97-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="80d97-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="80d97-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="80d97-1088">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="80d97-1089">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="80d97-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="80d97-1090">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="80d97-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="80d97-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="80d97-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="80d97-1094">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="80d97-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="80d97-1095">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="80d97-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="80d97-1096">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="80d97-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1098">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="80d97-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="80d97-1099">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="80d97-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1101">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="80d97-1102">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="80d97-1103">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="80d97-1104">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="80d97-1105">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="80d97-1106">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="80d97-1107">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="80d97-1108">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="80d97-1109">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="80d97-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="80d97-1110">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="80d97-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1111">Az.Resources</span></span>
- <span data-ttu-id="80d97-1112">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="80d97-1113">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="80d97-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-1115">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="80d97-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="80d97-1116">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1117">Az.Sql</span></span>
* <span data-ttu-id="80d97-1118">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="80d97-1119">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="80d97-1120">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="80d97-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1121">Az.Storage</span></span>
* <span data-ttu-id="80d97-1122">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="80d97-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="80d97-1123">Az.StorageSync</span></span>
* <span data-ttu-id="80d97-1124">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="80d97-1125">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="80d97-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1126">Az.Websites</span></span>
* <span data-ttu-id="80d97-1127">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="80d97-1128">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="80d97-1129">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="80d97-1130">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1131">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1132">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="80d97-1133">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="80d97-1134">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="80d97-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="80d97-1135">Az.Advisor</span></span>
* <span data-ttu-id="80d97-1136">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="80d97-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="80d97-1137">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="80d97-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="80d97-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-1139">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="80d97-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="80d97-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="80d97-1141">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="80d97-1142">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="80d97-1143">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="80d97-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="80d97-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="80d97-1145">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1146">Az.Automation</span></span>
* <span data-ttu-id="80d97-1147">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="80d97-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1148">Az.Compute</span></span>
* <span data-ttu-id="80d97-1149">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1150">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1151">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="80d97-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="80d97-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="80d97-1152">Az.EventGrid</span></span>
* <span data-ttu-id="80d97-1153">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1154">Az.IotHub</span></span>
* <span data-ttu-id="80d97-1155">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1156">Az.Network</span></span>
* <span data-ttu-id="80d97-1157">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="80d97-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="80d97-1158">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-1160">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="80d97-1161">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="80d97-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1163">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="80d97-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1165">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="80d97-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1166">Az.Resources</span></span>
    - <span data-ttu-id="80d97-1167">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="80d97-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="80d97-1168">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="80d97-1169">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="80d97-1170">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="80d97-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-1172">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="80d97-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1173">Az.Sql</span></span>
* <span data-ttu-id="80d97-1174">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="80d97-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="80d97-1175">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="80d97-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="80d97-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="80d97-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="80d97-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="80d97-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="80d97-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="80d97-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="80d97-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="80d97-1182">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="80d97-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1183">Az.Storage</span></span>
* <span data-ttu-id="80d97-1184">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="80d97-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="80d97-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="80d97-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="80d97-1186">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="80d97-1187">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="80d97-1188">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="80d97-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="80d97-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="80d97-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="80d97-1191">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="80d97-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="80d97-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="80d97-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="80d97-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="80d97-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="80d97-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="80d97-1194">Az.StorageSync</span></span>
* <span data-ttu-id="80d97-1195">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="80d97-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="80d97-1196">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1197">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1198">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="80d97-1199">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="80d97-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="80d97-1200">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="80d97-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="80d97-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="80d97-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="80d97-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1203">Az.Compute</span></span>
* <span data-ttu-id="80d97-1204">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="80d97-1205">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="80d97-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="80d97-1206">Az.Dns</span></span>
* <span data-ttu-id="80d97-1207">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="80d97-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="80d97-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="80d97-1208">Az.EventGrid</span></span>
* <span data-ttu-id="80d97-1209">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="80d97-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="80d97-1210">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1210">New cmdlets:</span></span>
    - <span data-ttu-id="80d97-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="80d97-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="80d97-1212">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="80d97-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="80d97-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="80d97-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="80d97-1214">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="80d97-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="80d97-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="80d97-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="80d97-1216">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="80d97-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="80d97-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="80d97-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="80d97-1218">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="80d97-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="80d97-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="80d97-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="80d97-1220">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="80d97-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="80d97-1221">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="80d97-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="80d97-1222">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="80d97-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="80d97-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="80d97-1224">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="80d97-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="80d97-1225">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="80d97-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="80d97-1226">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="80d97-1227">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="80d97-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="80d97-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="80d97-1229">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d97-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="80d97-1230">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d97-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="80d97-1231">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="80d97-1232">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="80d97-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="80d97-1233">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="80d97-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="80d97-1234">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="80d97-1235">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="80d97-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="80d97-1236">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="80d97-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="80d97-1237">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="80d97-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="80d97-1238">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="80d97-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="80d97-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="80d97-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="80d97-1240">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d97-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="80d97-1241">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d97-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="80d97-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="80d97-1244">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="80d97-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="80d97-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="80d97-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="80d97-1246">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="80d97-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1247">Az.Network</span></span>
* <span data-ttu-id="80d97-1248">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="80d97-1249">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1249">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="80d97-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="80d97-1251">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="80d97-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="80d97-1252">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1252">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="80d97-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="80d97-1254">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="80d97-1255">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1255">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="80d97-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="80d97-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="80d97-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="80d97-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="80d97-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="80d97-1261">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d97-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="80d97-1262">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1262">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d97-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="80d97-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d97-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="80d97-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d97-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="80d97-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="80d97-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="80d97-1267">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="80d97-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="80d97-1268">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="80d97-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="80d97-1269">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="80d97-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="80d97-1270">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="80d97-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="80d97-1271">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="80d97-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="80d97-1272">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="80d97-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="80d97-1273">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="80d97-1274">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="80d97-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="80d97-1275">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="80d97-1276">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="80d97-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="80d97-1277">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="80d97-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="80d97-1278">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="80d97-1279">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="80d97-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="80d97-1280">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="80d97-1281">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="80d97-1282">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="80d97-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="80d97-1283">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="80d97-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="80d97-1284">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="80d97-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="80d97-1285">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="80d97-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="80d97-1286">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="80d97-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="80d97-1287">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="80d97-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="80d97-1288">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="80d97-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="80d97-1289">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="80d97-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1291">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="80d97-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1292">Az.Resources</span></span>
* <span data-ttu-id="80d97-1293">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="80d97-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="80d97-1294">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="80d97-1295">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="80d97-1296">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="80d97-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-1298">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1299">Az.Sql</span></span>
* <span data-ttu-id="80d97-1300">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="80d97-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="80d97-1301">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="80d97-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="80d97-1302">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="80d97-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="80d97-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="80d97-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="80d97-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="80d97-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="80d97-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="80d97-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="80d97-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="80d97-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="80d97-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="80d97-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1308">Az.Storage</span></span>
* <span data-ttu-id="80d97-1309">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="80d97-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="80d97-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="80d97-1311">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="80d97-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1313">Az.Websites</span></span>
* <span data-ttu-id="80d97-1314">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="80d97-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="80d97-1315">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="80d97-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="80d97-1316">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="80d97-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-1317">Az.Cdn</span></span>
* <span data-ttu-id="80d97-1318">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="80d97-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1319">Az.Compute</span></span>
* <span data-ttu-id="80d97-1320">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="80d97-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="80d97-1321">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="80d97-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1322">Az.EventHub</span></span>
* <span data-ttu-id="80d97-1323">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="80d97-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="80d97-1324">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d97-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1325">Az.Network</span></span>
* <span data-ttu-id="80d97-1326">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="80d97-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="80d97-1327">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="80d97-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-1329">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1331">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="80d97-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-1333">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d97-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-1335">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="80d97-1336">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1337">Az.Sql</span></span>
* <span data-ttu-id="80d97-1338">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="80d97-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="80d97-1339">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="80d97-1340">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="80d97-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="80d97-1341">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1342">Az.Websites</span></span>
* <span data-ttu-id="80d97-1343">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="80d97-1344">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="80d97-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-1346">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="80d97-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="80d97-1347">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="80d97-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="80d97-1348">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="80d97-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="80d97-1349">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="80d97-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="80d97-1350">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="80d97-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="80d97-1351">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="80d97-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="80d97-1352">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="80d97-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="80d97-1353">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="80d97-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="80d97-1354">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="80d97-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="80d97-1355">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="80d97-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="80d97-1356">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="80d97-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="80d97-1357">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="80d97-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="80d97-1358">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="80d97-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="80d97-1359">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="80d97-1360">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="80d97-1361">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="80d97-1362">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="80d97-1363">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="80d97-1364">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="80d97-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="80d97-1365">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="80d97-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="80d97-1366">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="80d97-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="80d97-1367">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="80d97-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="80d97-1368">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="80d97-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="80d97-1369">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="80d97-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="80d97-1370">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="80d97-1371">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="80d97-1372">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="80d97-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="80d97-1373">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="80d97-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="80d97-1374">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="80d97-1375">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="80d97-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="80d97-1376">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="80d97-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="80d97-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="80d97-1378">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="80d97-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="80d97-1379">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="80d97-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="80d97-1380">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="80d97-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="80d97-1381">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="80d97-1382">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="80d97-1383">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="80d97-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="80d97-1384">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="80d97-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="80d97-1385">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="80d97-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="80d97-1386">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="80d97-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="80d97-1387">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="80d97-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="80d97-1388">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="80d97-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="80d97-1389">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="80d97-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="80d97-1390">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="80d97-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="80d97-1391">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="80d97-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="80d97-1392">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="80d97-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="80d97-1393">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="80d97-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="80d97-1394">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="80d97-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="80d97-1395">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="80d97-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="80d97-1396">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="80d97-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="80d97-1397">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="80d97-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="80d97-1398">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="80d97-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="80d97-1399">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="80d97-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="80d97-1400">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="80d97-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="80d97-1401">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="80d97-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="80d97-1402">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="80d97-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="80d97-1403">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="80d97-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="80d97-1404">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="80d97-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="80d97-1405">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="80d97-1406">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="80d97-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="80d97-1407">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="80d97-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="80d97-1408">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="80d97-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="80d97-1409">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="80d97-1410">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="80d97-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="80d97-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="80d97-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="80d97-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="80d97-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="80d97-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="80d97-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="80d97-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="80d97-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="80d97-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="80d97-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="80d97-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="80d97-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="80d97-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="80d97-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="80d97-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="80d97-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="80d97-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="80d97-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="80d97-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="80d97-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="80d97-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="80d97-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="80d97-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1423">Az.Automation</span></span>
* <span data-ttu-id="80d97-1424">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="80d97-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="80d97-1425">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="80d97-1426">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="80d97-1427">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="80d97-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="80d97-1428">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="80d97-1429">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="80d97-1430">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="80d97-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1431">Az.Compute</span></span>
* <span data-ttu-id="80d97-1432">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="80d97-1433">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="80d97-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-1435">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="80d97-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-1436">Az.Monitor</span></span>
* <span data-ttu-id="80d97-1437">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1438">Az.Network</span></span>
* <span data-ttu-id="80d97-1439">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="80d97-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="80d97-1440">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="80d97-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="80d97-1442">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="80d97-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1443">Az.Resources</span></span>
* <span data-ttu-id="80d97-1444">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="80d97-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1445">Az.Sql</span></span>
* <span data-ttu-id="80d97-1446">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="80d97-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="80d97-1447">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1448">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1449">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-1451">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="80d97-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="80d97-1452">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="80d97-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1453">Az.Compute</span></span>
* <span data-ttu-id="80d97-1454">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="80d97-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="80d97-1455">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="80d97-1456">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="80d97-1457">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="80d97-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="80d97-1458">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="80d97-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="80d97-1459">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="80d97-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="80d97-1460">重大變更</span><span class="sxs-lookup"><span data-stu-id="80d97-1460">Breaking changes</span></span>
    - <span data-ttu-id="80d97-1461">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="80d97-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="80d97-1462">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="80d97-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="80d97-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="80d97-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="80d97-1464">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="80d97-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="80d97-1465">Az.Dns</span></span>
* <span data-ttu-id="80d97-1466">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="80d97-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="80d97-1467">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="80d97-1468">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="80d97-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="80d97-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="80d97-1470">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="80d97-1471">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="80d97-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="80d97-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-1472">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-1473">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="80d97-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="80d97-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="80d97-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="80d97-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="80d97-1476">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="80d97-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="80d97-1477">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="80d97-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="80d97-1478">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="80d97-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="80d97-1479">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="80d97-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-1480">Az.Monitor</span></span>
* <span data-ttu-id="80d97-1481">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="80d97-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="80d97-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="80d97-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="80d97-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="80d97-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="80d97-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="80d97-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="80d97-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="80d97-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="80d97-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="80d97-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="80d97-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="80d97-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="80d97-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="80d97-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="80d97-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="80d97-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="80d97-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="80d97-1493">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="80d97-1494">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1495">Az.Network</span></span>
* <span data-ttu-id="80d97-1496">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="80d97-1497">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1497">New cmdlets</span></span>
        - <span data-ttu-id="80d97-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="80d97-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="80d97-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="80d97-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="80d97-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="80d97-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="80d97-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="80d97-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="80d97-1502">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="80d97-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="80d97-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="80d97-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="80d97-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="80d97-1505">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="80d97-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="80d97-1506">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="80d97-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="80d97-1507">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="80d97-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-1509">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="80d97-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="80d97-1510">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="80d97-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="80d97-1511">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="80d97-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1513">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="80d97-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="80d97-1514">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="80d97-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="80d97-1515">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="80d97-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="80d97-1516">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="80d97-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="80d97-1517">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="80d97-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="80d97-1518">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="80d97-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="80d97-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="80d97-1519">Az.Relay</span></span>
* <span data-ttu-id="80d97-1520">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-1522">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1523">Az.Storage</span></span>
* <span data-ttu-id="80d97-1524">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="80d97-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="80d97-1525">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="80d97-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="80d97-1526">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="80d97-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="80d97-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="80d97-1528">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="80d97-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="80d97-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="80d97-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="80d97-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1532">Az.Websites</span></span>
* <span data-ttu-id="80d97-1533">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="80d97-1534">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="80d97-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="80d97-1535">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-1536">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-1537">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="80d97-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="80d97-1538">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="80d97-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="80d97-1539">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="80d97-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="80d97-1540">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="80d97-1541">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="80d97-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="80d97-1542">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="80d97-1543">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1544">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1545">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="80d97-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="80d97-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-1546">Az.Batch</span></span>
* <span data-ttu-id="80d97-1547">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-1548">Az.Cdn</span></span>
* <span data-ttu-id="80d97-1549">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-1551">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1552">Az.Compute</span></span>
* <span data-ttu-id="80d97-1553">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="80d97-1554">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1555">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1556">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1557">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="80d97-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-1559">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="80d97-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="80d97-1560">Az.EventGrid</span></span>
* <span data-ttu-id="80d97-1561">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1562">Az.EventHub</span></span>
* <span data-ttu-id="80d97-1563">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="80d97-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="80d97-1564">Az.HDInsight</span></span>
* <span data-ttu-id="80d97-1565">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1566">Az.IotHub</span></span>
* <span data-ttu-id="80d97-1567">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1568">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-1569">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1570">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="80d97-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="80d97-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="80d97-1572">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="80d97-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="80d97-1573">Az.Media</span></span>
* <span data-ttu-id="80d97-1574">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-1575">Az.Monitor</span></span>
  * <span data-ttu-id="80d97-1576">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="80d97-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="80d97-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="80d97-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="80d97-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="80d97-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="80d97-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="80d97-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="80d97-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="80d97-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="80d97-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="80d97-1582">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="80d97-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1583">Az.Network</span></span>
* <span data-ttu-id="80d97-1584">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1585">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="80d97-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="80d97-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="80d97-1587">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1589">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="80d97-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="80d97-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="80d97-1591">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1593">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1594">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="80d97-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="80d97-1595">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="80d97-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="80d97-1596">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="80d97-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="80d97-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="80d97-1597">Az.RedisCache</span></span>
* <span data-ttu-id="80d97-1598">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1599">Az.Resources</span></span>
* <span data-ttu-id="80d97-1600">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1601">Az.Sql</span></span>
* <span data-ttu-id="80d97-1602">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="80d97-1603">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1604">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="80d97-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="80d97-1605">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="80d97-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="80d97-1606">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="80d97-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="80d97-1607">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="80d97-1608">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="80d97-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1609">Az.Websites</span></span>
* <span data-ttu-id="80d97-1610">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="80d97-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="80d97-1611">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="80d97-1612">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="80d97-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="80d97-1613">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="80d97-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="80d97-1614">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-1615">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-1616">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="80d97-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="80d97-1617">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="80d97-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="80d97-1618">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="80d97-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="80d97-1619">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="80d97-1620">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="80d97-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="80d97-1621">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="80d97-1622">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="80d97-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1623">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1624">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="80d97-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="80d97-1626">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="80d97-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="80d97-1627">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="80d97-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1628">Az.Automation</span></span>
* <span data-ttu-id="80d97-1629">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="80d97-1630">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="80d97-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="80d97-1631">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="80d97-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1632">Az.Compute</span></span>
* <span data-ttu-id="80d97-1633">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="80d97-1634">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="80d97-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="80d97-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="80d97-1636">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="80d97-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1637">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1638">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="80d97-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="80d97-1639">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1640">Az.Resources</span></span>
* <span data-ttu-id="80d97-1641">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="80d97-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="80d97-1642">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="80d97-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="80d97-1643">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="80d97-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="80d97-1644">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="80d97-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="80d97-1645">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="80d97-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="80d97-1646">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="80d97-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1647">Az.Sql</span></span>
* <span data-ttu-id="80d97-1648">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="80d97-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1649">Az.Storage</span></span>
* <span data-ttu-id="80d97-1650">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="80d97-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="80d97-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="80d97-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="80d97-1652">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="80d97-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="80d97-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="80d97-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="80d97-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="80d97-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="80d97-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="80d97-1657">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="80d97-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="80d97-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="80d97-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="80d97-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="80d97-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="80d97-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="80d97-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="80d97-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="80d97-1662">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="80d97-1663">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="80d97-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="80d97-1664">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="80d97-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="80d97-1665">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="80d97-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="80d97-1666">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="80d97-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="80d97-1667">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="80d97-1668">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="80d97-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="80d97-1669">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="80d97-1670">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1671">Az.Automation</span></span>
* <span data-ttu-id="80d97-1672">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="80d97-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="80d97-1673">動態分組</span><span class="sxs-lookup"><span data-stu-id="80d97-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="80d97-1674">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="80d97-1674">Pre-Post script</span></span>
    * <span data-ttu-id="80d97-1675">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="80d97-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1676">Az.Compute</span></span>
* <span data-ttu-id="80d97-1677">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="80d97-1678">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="80d97-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1679">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-1680">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1681">Az.Network</span></span>
* <span data-ttu-id="80d97-1682">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="80d97-1683">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="80d97-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1685">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="80d97-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="80d97-1686">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1687">Az.Resources</span></span>
* <span data-ttu-id="80d97-1688">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="80d97-1689">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="80d97-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1690">Az.Sql</span></span>
* <span data-ttu-id="80d97-1691">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="80d97-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1692">Az.Storage</span></span>
* <span data-ttu-id="80d97-1693">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="80d97-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="80d97-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="80d97-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="80d97-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="80d97-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="80d97-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="80d97-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="80d97-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="80d97-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1700">Az.Websites</span></span>
* <span data-ttu-id="80d97-1701">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="80d97-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="80d97-1702">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1703">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1704">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="80d97-1705">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1706">Az.Automation</span></span>
* <span data-ttu-id="80d97-1707">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="80d97-1708">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="80d97-1709">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="80d97-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-1710">Az.Cdn</span></span>
* <span data-ttu-id="80d97-1711">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1712">Az.Compute</span></span>
* <span data-ttu-id="80d97-1713">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1714">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1715">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="80d97-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="80d97-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="80d97-1716">Az.LogicApp</span></span>
* <span data-ttu-id="80d97-1717">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="80d97-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1718">Az.Network</span></span>
* <span data-ttu-id="80d97-1719">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1721">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="80d97-1722">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="80d97-1722">SDK Update</span></span>
* <span data-ttu-id="80d97-1723">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="80d97-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="80d97-1724">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="80d97-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1725">Az.Resources</span></span>
* <span data-ttu-id="80d97-1726">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="80d97-1727">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="80d97-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="80d97-1728">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="80d97-1729">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="80d97-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="80d97-1730">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="80d97-1731">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="80d97-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1732">Az.Sql</span></span>
* <span data-ttu-id="80d97-1733">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="80d97-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="80d97-1734">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="80d97-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1735">Az.Storage</span></span>
* <span data-ttu-id="80d97-1736">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80d97-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="80d97-1737">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="80d97-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="80d97-1739">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1740">Az.Automation</span></span>
* <span data-ttu-id="80d97-1741">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="80d97-1742">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="80d97-1743">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="80d97-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-1745">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="80d97-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1746">Az.Compute</span></span>
* <span data-ttu-id="80d97-1747">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="80d97-1748">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="80d97-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="80d97-1749">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="80d97-1750">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="80d97-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-1752">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="80d97-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1753">Az.EventHub</span></span>
* <span data-ttu-id="80d97-1754">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="80d97-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1755">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-1756">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="80d97-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="80d97-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="80d97-1757">Az.LogicApp</span></span>
* <span data-ttu-id="80d97-1758">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="80d97-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="80d97-1759">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="80d97-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="80d97-1760">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="80d97-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="80d97-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="80d97-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="80d97-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="80d97-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="80d97-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="80d97-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="80d97-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="80d97-1765">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="80d97-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="80d97-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="80d97-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="80d97-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="80d97-1770">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="80d97-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="80d97-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-1771">Az.Monitor</span></span>
* <span data-ttu-id="80d97-1772">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1773">Az.Network</span></span>
* <span data-ttu-id="80d97-1774">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="80d97-1776">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="80d97-1777">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="80d97-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="80d97-1778">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="80d97-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1779">Az.Resources</span></span>
* <span data-ttu-id="80d97-1780">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="80d97-1781">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="80d97-1782">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="80d97-1783">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1784">Az.Sql</span></span>
* <span data-ttu-id="80d97-1785">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="80d97-1786">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="80d97-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1787">Az.Websites</span></span>
* <span data-ttu-id="80d97-1788">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="80d97-1789">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1790">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1791">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="80d97-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="80d97-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="80d97-1793">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="80d97-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1794">Az.Compute</span></span>
* <span data-ttu-id="80d97-1795">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="80d97-1796">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="80d97-1797">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="80d97-1799">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="80d97-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1800">Az.Resources</span></span>
* <span data-ttu-id="80d97-1801">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="80d97-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="80d97-1802">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="80d97-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="80d97-1803">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="80d97-1804">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="80d97-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1805">Az.Sql</span></span>
* <span data-ttu-id="80d97-1806">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="80d97-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="80d97-1807">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="80d97-1808">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="80d97-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="80d97-1809">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1810">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1811">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="80d97-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="80d97-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="80d97-1813">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="80d97-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="80d97-1815">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="80d97-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="80d97-1816">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1817">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1818">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="80d97-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="80d97-1819">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="80d97-1820">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="80d97-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="80d97-1821">Az.Aks</span></span>
* <span data-ttu-id="80d97-1822">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="80d97-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-1823">Az.Automation</span></span>
* <span data-ttu-id="80d97-1824">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="80d97-1825">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="80d97-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="80d97-1826">Az.Cdn</span></span>
* <span data-ttu-id="80d97-1827">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1828">Az.Compute</span></span>
* <span data-ttu-id="80d97-1829">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="80d97-1830">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="80d97-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="80d97-1831">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="80d97-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80d97-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="80d97-1833">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="80d97-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="80d97-1834">Az.DataFactory</span></span>
* <span data-ttu-id="80d97-1835">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="80d97-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-1837">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="80d97-1838">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="80d97-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="80d97-1839">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1840">Az.IotHub</span></span>
* <span data-ttu-id="80d97-1841">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="80d97-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1842">Az.KeyVault</span></span>
* <span data-ttu-id="80d97-1843">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1844">Az.Network</span></span>
* <span data-ttu-id="80d97-1845">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1846">Az.Resources</span></span>
* <span data-ttu-id="80d97-1847">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="80d97-1848">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="80d97-1849">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="80d97-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="80d97-1850">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="80d97-1851">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="80d97-1852">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="80d97-1853">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="80d97-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-1855">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="80d97-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="80d97-1856">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="80d97-1856">Fix some error messages.</span></span>
* <span data-ttu-id="80d97-1857">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="80d97-1858">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="80d97-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="80d97-1859">Az.SignalR</span></span>
* <span data-ttu-id="80d97-1860">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1861">Az.Sql</span></span>
* <span data-ttu-id="80d97-1862">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="80d97-1863">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="80d97-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="80d97-1864">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="80d97-1865">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="80d97-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1866">Az.Storage</span></span>
* <span data-ttu-id="80d97-1867">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="80d97-1868">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="80d97-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="80d97-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="80d97-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="80d97-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="80d97-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="80d97-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="80d97-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="80d97-1872">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1873">Az.Websites</span></span>
* <span data-ttu-id="80d97-1874">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="80d97-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="80d97-1875">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="80d97-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="80d97-1876">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="80d97-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="80d97-1877">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="80d97-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1878">Az.Accounts</span></span>
* <span data-ttu-id="80d97-1879">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="80d97-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-1880">Az.Compute</span></span>
* <span data-ttu-id="80d97-1881">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="80d97-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="80d97-1882">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="80d97-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="80d97-1883">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-1885">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="80d97-1886">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="80d97-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="80d97-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="80d97-1887">Az.EventGrid</span></span>
* <span data-ttu-id="80d97-1888">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="80d97-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="80d97-1889">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="80d97-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="80d97-1890">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="80d97-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="80d97-1891">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="80d97-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="80d97-1892">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="80d97-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="80d97-1893">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="80d97-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="80d97-1894">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="80d97-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="80d97-1895">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="80d97-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="80d97-1896">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="80d97-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="80d97-1897">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="80d97-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="80d97-1898">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="80d97-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="80d97-1899">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="80d97-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="80d97-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="80d97-1900">Az.IotHub</span></span>
* <span data-ttu-id="80d97-1901">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="80d97-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="80d97-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="80d97-1902">Az.LogicApp</span></span>
* <span data-ttu-id="80d97-1903">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1904">Az.Resources</span></span>
* <span data-ttu-id="80d97-1905">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="80d97-1906">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="80d97-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="80d97-1907">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="80d97-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="80d97-1908">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="80d97-1909">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="80d97-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="80d97-1910">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="80d97-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="80d97-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="80d97-1911">Az.SignalR</span></span>
* <span data-ttu-id="80d97-1912">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1913">Az.Sql</span></span>
* <span data-ttu-id="80d97-1914">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="80d97-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="80d97-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1915">Az.Storage</span></span>
* <span data-ttu-id="80d97-1916">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="80d97-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="80d97-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="80d97-1918">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="80d97-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="80d97-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="80d97-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-1920">Az.Websites</span></span>
* <span data-ttu-id="80d97-1921">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="80d97-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="80d97-1922">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="80d97-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="80d97-1923">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="80d97-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="80d97-1924">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-1924">General</span></span>

- <span data-ttu-id="80d97-1925">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="80d97-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="80d97-1926">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="80d97-1926">Online help for each module</span></span>
- <span data-ttu-id="80d97-1927">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="80d97-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="80d97-1928">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="80d97-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1929">Az.Accounts</span></span>
- <span data-ttu-id="80d97-1930">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="80d97-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="80d97-1931">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="80d97-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="80d97-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="80d97-1933">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="80d97-1933">Fixes for #7002</span></span>
- <span data-ttu-id="80d97-1934">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="80d97-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="80d97-1935">Az.Batch</span></span>
- <span data-ttu-id="80d97-1936">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="80d97-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="80d97-1937">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="80d97-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="80d97-1938">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="80d97-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="80d97-1939">Az.Billing</span></span>
- <span data-ttu-id="80d97-1940">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="80d97-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="80d97-1942">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="80d97-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="80d97-1943">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="80d97-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="80d97-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="80d97-1945">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="80d97-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="80d97-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="80d97-1947">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="80d97-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="80d97-1949">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="80d97-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="80d97-1950">Az.Monitor</span></span>
- <span data-ttu-id="80d97-1951">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="80d97-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="80d97-1952">Az.KeyVault</span></span>
- <span data-ttu-id="80d97-1953">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="80d97-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="80d97-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="80d97-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="80d97-1955">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="80d97-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="80d97-1956">Az.Media</span></span>
- <span data-ttu-id="80d97-1957">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="80d97-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="80d97-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-1958">Az.Network</span></span>
<span data-ttu-id="80d97-1959">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="80d97-1960">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="80d97-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="80d97-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="80d97-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="80d97-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d97-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="80d97-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d97-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="80d97-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80d97-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="80d97-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="80d97-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="80d97-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="80d97-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="80d97-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="80d97-1975">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="80d97-1976">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="80d97-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80d97-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="80d97-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80d97-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="80d97-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80d97-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="80d97-1980">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="80d97-1981">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="80d97-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="80d97-1983">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="80d97-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="80d97-1984">Az.Profile</span></span>
- <span data-ttu-id="80d97-1985">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="80d97-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="80d97-1987">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="80d97-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-1988">Az.Resources</span></span>
- <span data-ttu-id="80d97-1989">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="80d97-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="80d97-1991">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="80d97-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="80d97-1992">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="80d97-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="80d97-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="80d97-1994">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="80d97-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="80d97-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-1995">Az.Sql</span></span>
- <span data-ttu-id="80d97-1996">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="80d97-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="80d97-1997">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="80d97-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="80d97-1998">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="80d97-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-1999">Az.Storage</span></span>
- <span data-ttu-id="80d97-2000">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="80d97-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-2001">Az.Websites</span></span>
- <span data-ttu-id="80d97-2002">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="80d97-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="80d97-2003">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="80d97-2004">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-2004">General</span></span>

* <span data-ttu-id="80d97-2005">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="80d97-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="80d97-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-2006">Az.Compute</span></span>

* <span data-ttu-id="80d97-2007">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="80d97-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="80d97-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="80d97-2009">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="80d97-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="80d97-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="80d97-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="80d97-2011">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="80d97-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="80d97-2012">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="80d97-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="80d97-2013">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="80d97-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="80d97-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="80d97-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="80d97-2015">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="80d97-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="80d97-2016">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="80d97-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="80d97-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-2017">Az.Resources</span></span>

* <span data-ttu-id="80d97-2018">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="80d97-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="80d97-2019">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="80d97-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="80d97-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-2020">Az.Sql</span></span>

* <span data-ttu-id="80d97-2021">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="80d97-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="80d97-2022">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="80d97-2023">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="80d97-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="80d97-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-2024">Az.Storage</span></span>

* <span data-ttu-id="80d97-2025">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="80d97-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="80d97-2026">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="80d97-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="80d97-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="80d97-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="80d97-2028">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="80d97-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="80d97-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="80d97-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="80d97-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="80d97-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="80d97-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-2031">Az.Websites</span></span>

* <span data-ttu-id="80d97-2032">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d97-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="80d97-2033">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="80d97-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="80d97-2034">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="80d97-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="80d97-2035">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="80d97-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="80d97-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="80d97-2037">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="80d97-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="80d97-2038">Az.Automation</span></span>
* <span data-ttu-id="80d97-2039">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="80d97-2040">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="80d97-2041">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="80d97-2042">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="80d97-2043">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="80d97-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="80d97-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-2044">Az.Compute</span></span>
* <span data-ttu-id="80d97-2045">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="80d97-2046">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="80d97-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="80d97-2048">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="80d97-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="80d97-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="80d97-2050">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="80d97-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="80d97-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-2051">Az.Network</span></span>
* <span data-ttu-id="80d97-2052">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="80d97-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="80d97-2053">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="80d97-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="80d97-2054">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="80d97-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="80d97-2055">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="80d97-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="80d97-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="80d97-2057">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="80d97-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="80d97-2058">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="80d97-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="80d97-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="80d97-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="80d97-2060">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="80d97-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="80d97-2061">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="80d97-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="80d97-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="80d97-2062">Az.Relay</span></span>
* <span data-ttu-id="80d97-2063">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="80d97-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="80d97-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-2064">Az.Resources</span></span>
* <span data-ttu-id="80d97-2065">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="80d97-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="80d97-2066">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="80d97-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="80d97-2067">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="80d97-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="80d97-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-2069">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="80d97-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="80d97-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-2070">Az.Sql</span></span>
* <span data-ttu-id="80d97-2071">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="80d97-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="80d97-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="80d97-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="80d97-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="80d97-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="80d97-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="80d97-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="80d97-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="80d97-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="80d97-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="80d97-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="80d97-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="80d97-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="80d97-2080">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="80d97-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="80d97-2081">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="80d97-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="80d97-2082">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="80d97-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="80d97-2083">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="80d97-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="80d97-2084">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="80d97-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="80d97-2085">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="80d97-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="80d97-2086">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="80d97-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="80d97-2087">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="80d97-2088">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="80d97-2089">一般</span><span class="sxs-lookup"><span data-stu-id="80d97-2089">General</span></span>
* <span data-ttu-id="80d97-2090">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="80d97-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="80d97-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="80d97-2091">Az.Profile</span></span>
* <span data-ttu-id="80d97-2092">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="80d97-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="80d97-2093">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="80d97-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="80d97-2094">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="80d97-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="80d97-2095">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="80d97-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="80d97-2096">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="80d97-2097">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="80d97-2098">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-2100">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="80d97-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-2101">Az.Compute</span></span>
* <span data-ttu-id="80d97-2102">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="80d97-2103">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="80d97-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="80d97-2104">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-2106">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="80d97-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="80d97-2107">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="80d97-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="80d97-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="80d97-2108">Az.Insights</span></span>
* <span data-ttu-id="80d97-2109">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="80d97-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="80d97-2110">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="80d97-2111">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="80d97-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="80d97-2112">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="80d97-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-2113">Az.Network</span></span>
* <span data-ttu-id="80d97-2114">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="80d97-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="80d97-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="80d97-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="80d97-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="80d97-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="80d97-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="80d97-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="80d97-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="80d97-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="80d97-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="80d97-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="80d97-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="80d97-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="80d97-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="80d97-2122">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-2123">Az.Resources</span></span>
* <span data-ttu-id="80d97-2124">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="80d97-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="80d97-2125">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="80d97-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="80d97-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="80d97-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="80d97-2127">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="80d97-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="80d97-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80d97-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="80d97-2129">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="80d97-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="80d97-2130">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="80d97-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="80d97-2131">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="80d97-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="80d97-2132">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="80d97-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="80d97-2133">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="80d97-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="80d97-2134">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="80d97-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="80d97-2135">Az.Profile</span></span>
* <span data-ttu-id="80d97-2136">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="80d97-2137">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="80d97-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-2138">Az.Compute</span></span>
* <span data-ttu-id="80d97-2139">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="80d97-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="80d97-2140">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="80d97-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="80d97-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="80d97-2142">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="80d97-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="80d97-2143">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="80d97-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="80d97-2144">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="80d97-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="80d97-2145">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="80d97-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="80d97-2146">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="80d97-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-2147">Az.Network</span></span>
* <span data-ttu-id="80d97-2148">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="80d97-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="80d97-2149">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80d97-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-2150">Az.Resources</span></span>
* <span data-ttu-id="80d97-2151">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="80d97-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="80d97-2152">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="80d97-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="80d97-2153">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="80d97-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="80d97-2154">Azure.Storage</span></span>
* <span data-ttu-id="80d97-2155">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="80d97-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="80d97-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="80d97-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="80d97-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="80d97-2158">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="80d97-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="80d97-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="80d97-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="80d97-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="80d97-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="80d97-2161">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="80d97-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="80d97-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="80d97-2162">Az.Compute</span></span>
* <span data-ttu-id="80d97-2163">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="80d97-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="80d97-2164">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="80d97-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="80d97-2165">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="80d97-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="80d97-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="80d97-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="80d97-2167">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="80d97-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="80d97-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="80d97-2168">Az.Network</span></span>
* <span data-ttu-id="80d97-2169">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="80d97-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="80d97-2170">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2170">new cmdlets added</span></span>
    - <span data-ttu-id="80d97-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="80d97-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="80d97-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="80d97-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="80d97-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="80d97-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="80d97-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="80d97-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="80d97-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="80d97-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d97-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="80d97-2177">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="80d97-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="80d97-2178">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="80d97-2179">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80d97-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="80d97-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="80d97-2180">Az.RedisCache</span></span>
* <span data-ttu-id="80d97-2181">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="80d97-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="80d97-2182">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="80d97-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="80d97-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="80d97-2183">Az.Resources</span></span>
* <span data-ttu-id="80d97-2184">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="80d97-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="80d97-2185">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="80d97-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="80d97-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="80d97-2186">Az.Sql</span></span>
* <span data-ttu-id="80d97-2187">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="80d97-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="80d97-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="80d97-2188">Az.Websites</span></span>
* <span data-ttu-id="80d97-2189">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="80d97-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="80d97-2190">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="80d97-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="80d97-2191">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="80d97-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="80d97-2192">初始版本</span><span class="sxs-lookup"><span data-stu-id="80d97-2192">Initial Release</span></span>
