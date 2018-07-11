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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406197"
---
# <a name="release-notes"></a><span data-ttu-id="eea03-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="eea03-103">Release notes</span></span>

<span data-ttu-id="eea03-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="eea03-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="eea03-105">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="eea03-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eea03-106">一般</span><span class="sxs-lookup"><span data-stu-id="eea03-106">General</span></span>
* <span data-ttu-id="eea03-107">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="eea03-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="eea03-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eea03-108">AzureRM.Profile</span></span>
* <span data-ttu-id="eea03-109">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="eea03-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eea03-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eea03-110">AzureRM.Compute</span></span>
* <span data-ttu-id="eea03-111">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="eea03-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="eea03-112">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="eea03-113">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="eea03-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="eea03-114">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="eea03-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="eea03-115">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="eea03-116">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="eea03-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="eea03-117">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="eea03-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eea03-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="eea03-119">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="eea03-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="eea03-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eea03-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="eea03-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eea03-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="eea03-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="eea03-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eea03-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eea03-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eea03-124">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="eea03-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="eea03-125">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="eea03-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="eea03-126">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="eea03-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="eea03-127">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="eea03-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="eea03-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="eea03-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="eea03-129">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="eea03-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="eea03-130">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="eea03-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="eea03-131">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="eea03-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="eea03-132">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="eea03-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eea03-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eea03-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eea03-134">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="eea03-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eea03-135">AzureRM.Network</span></span>
* <span data-ttu-id="eea03-136">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="eea03-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="eea03-137">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="eea03-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="eea03-138">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eea03-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="eea03-139">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eea03-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="eea03-140">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eea03-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eea03-141">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eea03-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eea03-142">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eea03-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="eea03-143">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="eea03-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eea03-144">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="eea03-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eea03-145">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eea03-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eea03-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="eea03-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eea03-147">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eea03-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="eea03-148">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="eea03-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="eea03-149">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eea03-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eea03-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eea03-150">AzureRM.Resources</span></span>
* <span data-ttu-id="eea03-151">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="eea03-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="eea03-152">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="eea03-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="eea03-153">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="eea03-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="eea03-154">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="eea03-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="eea03-155">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="eea03-156">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="eea03-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="eea03-157">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="eea03-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="eea03-158">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="eea03-159">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="eea03-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="eea03-160">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="eea03-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="eea03-161">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="eea03-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="eea03-162">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="eea03-163">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="eea03-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eea03-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="eea03-165">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="eea03-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eea03-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eea03-166">AzureRM.Sql</span></span>
* <span data-ttu-id="eea03-167">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="eea03-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="eea03-168">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="eea03-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="eea03-169">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="eea03-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eea03-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eea03-170">AzureRM.Profile</span></span>
* <span data-ttu-id="eea03-171">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="eea03-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="eea03-172">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="eea03-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="eea03-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eea03-173">Azure.Storage</span></span>
* <span data-ttu-id="eea03-174">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="eea03-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eea03-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eea03-175">AzureRM.Compute</span></span>
* <span data-ttu-id="eea03-176">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="eea03-177">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="eea03-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eea03-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="eea03-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eea03-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="eea03-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eea03-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="eea03-181">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="eea03-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="eea03-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eea03-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="eea03-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eea03-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="eea03-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eea03-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="eea03-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eea03-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="eea03-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="eea03-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="eea03-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="eea03-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="eea03-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="eea03-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="eea03-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="eea03-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="eea03-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="eea03-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="eea03-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="eea03-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="eea03-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="eea03-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="eea03-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eea03-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="eea03-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="eea03-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="eea03-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eea03-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="eea03-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="eea03-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="eea03-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eea03-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="eea03-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eea03-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="eea03-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eea03-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="eea03-202">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="eea03-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="eea03-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eea03-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eea03-204">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="eea03-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="eea03-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eea03-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="eea03-206">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="eea03-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="eea03-207">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="eea03-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="eea03-208">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="eea03-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="eea03-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="eea03-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eea03-210">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eea03-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="eea03-211">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eea03-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eea03-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eea03-212">AzureRM.Sql</span></span>
* <span data-ttu-id="eea03-213">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="eea03-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eea03-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eea03-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eea03-215">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="eea03-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eea03-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eea03-216">AzureRM.Websites</span></span>
* <span data-ttu-id="eea03-217">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="eea03-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="eea03-218">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="eea03-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="eea03-219">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="eea03-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="eea03-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eea03-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="eea03-221">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="eea03-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="eea03-222">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="eea03-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eea03-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eea03-223">AzureRM.Profile</span></span>
* <span data-ttu-id="eea03-224">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="eea03-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="eea03-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="eea03-225">AzureRM.Compute</span></span>
* <span data-ttu-id="eea03-226">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="eea03-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="eea03-227">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="eea03-228">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="eea03-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="eea03-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eea03-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="eea03-230">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="eea03-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="eea03-231">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="eea03-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="eea03-232">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="eea03-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="eea03-233">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="eea03-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="eea03-234">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="eea03-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="eea03-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eea03-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="eea03-236">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="eea03-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="eea03-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eea03-237">AzureRM.Network</span></span>
* <span data-ttu-id="eea03-238">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="eea03-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="eea03-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="eea03-239">AzureRM.Resources</span></span>
* <span data-ttu-id="eea03-240">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="eea03-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="eea03-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="eea03-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="eea03-242">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="eea03-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eea03-243">AzureRM.Sql</span></span>
* <span data-ttu-id="eea03-244">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eea03-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="eea03-245">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eea03-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="eea03-246">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eea03-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="eea03-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="eea03-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="eea03-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eea03-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="eea03-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eea03-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="eea03-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="eea03-250">AzureRM.Websites</span></span>
* <span data-ttu-id="eea03-251">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="eea03-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="eea03-252">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="eea03-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="eea03-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="eea03-253">AzureRM.Profile</span></span>
* <span data-ttu-id="eea03-254">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="eea03-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="eea03-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eea03-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="eea03-256">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="eea03-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="eea03-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eea03-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="eea03-258">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="eea03-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="eea03-259">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="eea03-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="eea03-260">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="eea03-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="eea03-261">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="eea03-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="eea03-262">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="eea03-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="eea03-263">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="eea03-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="eea03-264">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="eea03-264">Added support for MSI identity</span></span>
* <span data-ttu-id="eea03-265">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="eea03-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="eea03-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="eea03-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="eea03-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="eea03-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="eea03-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="eea03-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="eea03-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="eea03-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="eea03-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="eea03-270">AzureRM.Batch</span></span>
* <span data-ttu-id="eea03-271">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="eea03-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="eea03-272">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="eea03-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="eea03-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="eea03-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="eea03-274">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="eea03-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="eea03-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eea03-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="eea03-276">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="eea03-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="eea03-277">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="eea03-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="eea03-278">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="eea03-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="eea03-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="eea03-279">AzureRM.Network</span></span>
* <span data-ttu-id="eea03-280">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="eea03-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="eea03-281">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="eea03-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="eea03-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="eea03-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="eea03-283">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="eea03-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="eea03-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea03-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="eea03-285">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="eea03-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="eea03-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea03-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="eea03-287">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="eea03-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="eea03-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="eea03-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="eea03-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eea03-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="eea03-290">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="eea03-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="eea03-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="eea03-291">AzureRM.Sql</span></span>
* <span data-ttu-id="eea03-292">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="eea03-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="eea03-293">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="eea03-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="eea03-294">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="eea03-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="eea03-295">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="eea03-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="eea03-296">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="eea03-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="eea03-297">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eea03-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="eea03-298">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eea03-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="eea03-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="eea03-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="eea03-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eea03-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="eea03-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eea03-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="eea03-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eea03-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="eea03-303">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="eea03-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>