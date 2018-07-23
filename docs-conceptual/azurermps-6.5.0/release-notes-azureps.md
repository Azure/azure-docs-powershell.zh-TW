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
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110478"
---
# <a name="release-notes"></a><span data-ttu-id="76916-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="76916-103">Release notes</span></span>

<span data-ttu-id="76916-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="76916-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="76916-105">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="76916-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76916-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76916-106">AzureRM.Profile</span></span>
* <span data-ttu-id="76916-107">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="76916-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="76916-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="76916-108">Azure.Storage</span></span>
* <span data-ttu-id="76916-109">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="76916-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="76916-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76916-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="76916-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76916-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="76916-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76916-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="76916-113">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="76916-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="76916-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="76916-114">AzureRM.Automation</span></span>
* <span data-ttu-id="76916-115">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="76916-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76916-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76916-116">AzureRM.Compute</span></span>
* <span data-ttu-id="76916-117">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76916-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="76916-118">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="76916-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="76916-119">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="76916-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="76916-120">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="76916-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="76916-121">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="76916-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76916-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76916-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="76916-123">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="76916-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76916-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76916-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76916-125">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="76916-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="76916-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76916-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="76916-127">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="76916-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76916-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76916-128">AzureRM.Network</span></span>
* <span data-ttu-id="76916-129">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="76916-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="76916-130">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="76916-131">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="76916-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="76916-132">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="76916-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="76916-133">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="76916-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="76916-134">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="76916-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="76916-135">AzureRM.Relay</span></span>
* <span data-ttu-id="76916-136">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="76916-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76916-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76916-137">AzureRM.Resources</span></span>
* <span data-ttu-id="76916-138">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="76916-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="76916-139">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="76916-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="76916-140">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="76916-141">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="76916-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="76916-142">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="76916-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76916-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76916-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76916-144">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="76916-145">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="76916-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="76916-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="76916-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76916-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="76916-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76916-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="76916-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76916-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="76916-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76916-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="76916-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="76916-151">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="76916-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="76916-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76916-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="76916-153">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="76916-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76916-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76916-154">AzureRM.Sql</span></span>
* <span data-ttu-id="76916-155">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="76916-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="76916-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="76916-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="76916-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="76916-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76916-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76916-158">AzureRM.Websites</span></span>
* <span data-ttu-id="76916-159">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="76916-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="76916-160">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="76916-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="76916-161">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="76916-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="76916-162">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="76916-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76916-163">一般</span><span class="sxs-lookup"><span data-stu-id="76916-163">General</span></span>
* <span data-ttu-id="76916-164">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="76916-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="76916-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76916-165">AzureRM.Profile</span></span>
* <span data-ttu-id="76916-166">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="76916-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76916-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76916-167">AzureRM.Compute</span></span>
* <span data-ttu-id="76916-168">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="76916-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="76916-169">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="76916-170">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="76916-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="76916-171">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="76916-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="76916-172">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="76916-173">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="76916-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="76916-174">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="76916-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="76916-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="76916-176">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="76916-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="76916-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="76916-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="76916-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="76916-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="76916-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="76916-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76916-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76916-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76916-181">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="76916-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="76916-182">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="76916-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="76916-183">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="76916-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="76916-184">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="76916-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76916-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76916-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="76916-186">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="76916-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="76916-187">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="76916-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="76916-188">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="76916-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="76916-189">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="76916-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76916-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76916-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76916-191">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="76916-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76916-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76916-192">AzureRM.Network</span></span>
* <span data-ttu-id="76916-193">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="76916-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="76916-194">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="76916-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="76916-195">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76916-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="76916-196">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76916-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="76916-197">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="76916-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76916-198">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="76916-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76916-199">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="76916-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76916-200">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="76916-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="76916-201">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="76916-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="76916-202">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76916-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="76916-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76916-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76916-204">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76916-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="76916-205">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="76916-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="76916-206">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="76916-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76916-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76916-207">AzureRM.Resources</span></span>
* <span data-ttu-id="76916-208">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="76916-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="76916-209">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="76916-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="76916-210">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="76916-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="76916-211">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="76916-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="76916-212">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="76916-213">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="76916-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="76916-214">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="76916-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="76916-215">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="76916-216">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="76916-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="76916-217">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="76916-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="76916-218">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="76916-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="76916-219">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="76916-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="76916-220">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="76916-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="76916-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76916-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76916-222">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="76916-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76916-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76916-223">AzureRM.Sql</span></span>
* <span data-ttu-id="76916-224">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="76916-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="76916-225">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="76916-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="76916-226">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="76916-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76916-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76916-227">AzureRM.Profile</span></span>
* <span data-ttu-id="76916-228">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="76916-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="76916-229">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="76916-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="76916-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="76916-230">Azure.Storage</span></span>
* <span data-ttu-id="76916-231">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="76916-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76916-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76916-232">AzureRM.Compute</span></span>
* <span data-ttu-id="76916-233">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="76916-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="76916-234">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="76916-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="76916-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="76916-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="76916-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="76916-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="76916-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="76916-238">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="76916-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="76916-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76916-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="76916-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76916-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="76916-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76916-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="76916-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76916-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="76916-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="76916-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="76916-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="76916-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="76916-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="76916-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="76916-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="76916-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="76916-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="76916-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="76916-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76916-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="76916-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="76916-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="76916-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="76916-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="76916-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="76916-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="76916-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="76916-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="76916-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="76916-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="76916-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="76916-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="76916-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76916-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="76916-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76916-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="76916-259">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="76916-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76916-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76916-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76916-261">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="76916-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="76916-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76916-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="76916-263">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="76916-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="76916-264">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="76916-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="76916-265">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="76916-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="76916-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76916-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76916-267">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76916-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="76916-268">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76916-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76916-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76916-269">AzureRM.Sql</span></span>
* <span data-ttu-id="76916-270">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="76916-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76916-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76916-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76916-272">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="76916-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76916-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76916-273">AzureRM.Websites</span></span>
* <span data-ttu-id="76916-274">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="76916-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="76916-275">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="76916-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="76916-276">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="76916-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="76916-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76916-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="76916-278">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="76916-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="76916-279">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="76916-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76916-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76916-280">AzureRM.Profile</span></span>
* <span data-ttu-id="76916-281">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="76916-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76916-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76916-282">AzureRM.Compute</span></span>
* <span data-ttu-id="76916-283">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="76916-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="76916-284">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="76916-285">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76916-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="76916-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76916-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="76916-287">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="76916-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="76916-288">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="76916-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="76916-289">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="76916-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="76916-290">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="76916-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="76916-291">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="76916-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="76916-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76916-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76916-293">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="76916-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="76916-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76916-294">AzureRM.Network</span></span>
* <span data-ttu-id="76916-295">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="76916-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76916-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76916-296">AzureRM.Resources</span></span>
* <span data-ttu-id="76916-297">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="76916-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="76916-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="76916-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="76916-299">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="76916-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="76916-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76916-300">AzureRM.Sql</span></span>
* <span data-ttu-id="76916-301">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76916-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="76916-302">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76916-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="76916-303">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76916-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="76916-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="76916-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="76916-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76916-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="76916-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76916-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76916-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76916-307">AzureRM.Websites</span></span>
* <span data-ttu-id="76916-308">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="76916-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="76916-309">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="76916-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76916-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76916-310">AzureRM.Profile</span></span>
* <span data-ttu-id="76916-311">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="76916-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="76916-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76916-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="76916-313">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="76916-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="76916-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76916-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="76916-315">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="76916-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="76916-316">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="76916-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="76916-317">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="76916-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="76916-318">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="76916-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="76916-319">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="76916-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="76916-320">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="76916-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="76916-321">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="76916-321">Added support for MSI identity</span></span>
* <span data-ttu-id="76916-322">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="76916-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="76916-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="76916-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="76916-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="76916-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="76916-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="76916-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="76916-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="76916-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="76916-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="76916-327">AzureRM.Batch</span></span>
* <span data-ttu-id="76916-328">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="76916-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="76916-329">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="76916-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="76916-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="76916-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="76916-331">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="76916-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76916-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76916-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76916-333">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="76916-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="76916-334">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="76916-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="76916-335">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="76916-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="76916-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76916-336">AzureRM.Network</span></span>
* <span data-ttu-id="76916-337">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="76916-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="76916-338">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="76916-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="76916-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="76916-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="76916-340">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="76916-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="76916-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="76916-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="76916-342">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="76916-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="76916-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="76916-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="76916-344">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="76916-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="76916-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="76916-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="76916-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76916-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="76916-347">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="76916-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76916-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76916-348">AzureRM.Sql</span></span>
* <span data-ttu-id="76916-349">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="76916-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="76916-350">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="76916-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="76916-351">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="76916-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="76916-352">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="76916-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="76916-353">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="76916-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="76916-354">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76916-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="76916-355">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76916-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="76916-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="76916-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="76916-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76916-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="76916-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76916-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76916-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76916-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76916-360">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="76916-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>